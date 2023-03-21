---
layout: blog
title: OS Credential Dumping LSASS Memory Dump  
---


<div id="main" class="s-content__main large-8 column">
    <article class="entry">

        <header class="entry__header">

            <h2 class="entry__title h1">
                OS Credential Dumping: LSASS Memory Dump
            </h2>        
        </header>
        
        <div class="entry__content">
            <h4>Explanation</h4>
            <p>A good resource from <a href="https://www.microsoft.com/en-us/security/blog/2022/10/05/detecting-and-preventing-lsass-credential-dumping-attacks/">Microsoft</a> covering this tactic. The Local Security Authority Subsystem Service (LSASS) is a critical component of the Windows operating system. It is responsible for authenticating users, managing security policies, and maintaining user credentials. LSASS credential dumping attacks are a type of cyberattack that targets the LSASS process to extract sensitive information such as passwords, hashes, and other authentication credentials.</p>

            <h4>Attack</h4>
            <p>These attacks are from <a href="https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1003.001/T1003.001.md">Atomic Red Team</a></p>
            <h5>ProcDump</h5>
            <p><a href="https://learn.microsoft.com/en-us/sysinternals/downloads/procdump">ProcDump</a> is a Sysinternals tool released by Microsoft which is a utility whose main purpose is to monitor an application for CPU spikes and generating crash dumps. It can also be used as a general process dump utility, like with this attack. To perform this attack, download <a href="https://learn.microsoft.com/en-us/sysinternals/downloads/procdump">ProcDump</a> from this link and run this command:<br>
            <code>procdump.exe -accepteula -ma lsass.exe [Dump_Location]</code></p>

            <h5>comsvcs.dll</h5>
            <p>This built-in dll can be used to dump the LSASS memory. When the command completes there will be a new file $env:TEMP\lsass-comsvcs.dmp. Run this command with PowerShell and elevated privileges:<br>
            <code>C:\Windows\System32\rundll32.exe C:\windows\System32\comsvcs.dll, MiniDump (Get-Process lsass).id $env:TEMP\lsass-comsvcs.dmp full</code></p>

            <h5>Dumpert</h5>
            <p>This method uses direct system calls and API unhooking, <a href="https://github.com/outflanknl/Dumpert">dumpert</a></p>


            <h4>Defend</h4>
            <p>Detecting LSASS credential dumping attacks can be challenging as attackers can use a variety of methods to carry out the attack. However, there are some indicators of compromise (IOCs) that can help detect LSASS credential dumping attacks. Microsoft has a <a href="https://www.microsoft.com/en-us/security/blog/2022/10/05/detecting-and-preventing-lsass-credential-dumping-attacks/">blog post</a> on detecting and preventing LSASS credential dumping.</p>

            <h5>Detecting</h5>
            <p>To detect LSASS credential dumping attacks, organizations can use a combination of network monitoring, endpoint detection and response (EDR) tools, and security information and event management (SIEM) systems.
            <ul>
            <li>Suspicious processes or services running on the system</li>
            <li>Unusual network traffic or connections to external systems</li>
            <li>Large amounts of data being transferred to external systems</li>
            <li>System logs that show suspicious activity or failed authentication attempts</li>
            </ul></p>

            <h5>Preventing</h5>
            <p>Preventing LSASS credential dumping attacks requires a combination of proactive security measures and best practices. Here are some steps that organizations can take to prevent LSASS credential dumping attacks:
            <ul>
                <li>Keep the operating system and security software up to date with the latest security patches.</li>
                <li>Limit user privileges to reduce the attack surface.</li>
                <li>Use endpoint detection and response (EDR) tools that can detect malicious activity and block unauthorized access to the LSASS process.</li>
                <li>Use multifactor authentication (MFA) to reduce the risk of credential theft.</li>
                <li>Monitor and analyze network traffic to detect unusual activity.</li>
                <li>Use anti-malware and intrusion detection and prevention (IDP) software to prevent malware infections</li>
            </ul></p>
        

            <p>Return to <a href="/subjects/AttackDefend/Credential_Access.html">Credential Access</a></p>
        </div> 

    </article> <!-- end entry -->

</div> <!-- end main -->  