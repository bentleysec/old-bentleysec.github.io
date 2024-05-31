---
layout: blog
title: Most Common MITRE Att&ck Techniques
---


<div id="main" class="s-content__main large-8 column">
<article class="entry">

<header class="entry__header">

<h2 class="entry__title h1">
    Most Common MITRE Att&ck Techniques
</h2>        
</header>

<div class="entry__content">
<p>In today's ever-evolving cybersecurity landscape, understanding the tactics and techniques employed by adversaries is crucial for effective defense. The MITRE ATT&CK framework has emerged as a comprehensive knowledge base, cataloging the various methods used by threat actors during cyber attacks.</p>

<p>This blog series will delve into the most prevalent techniques observed across various incidents and attack groups, shedding light on the modus operandi of cybercriminals. By gaining insights into these common tactics, security professionals can enhance their defensive posture and better prepare for potential threats.</p>

<p>The MITRE ATT&CK framework organizes adversary behavior into a matrix of tactics and techniques, covering the entire attack lifecycle, from initial access to exfiltration. While the framework encompasses a vast array of techniques, certain methods have gained notoriety due to their widespread adoption by attackers.</p>

<p>In this series, we will explore the following techniques that have become commonplace in the world of cyber attacks:
<ol>
    <li>Initial Access:</li>
    <ol>
        <li><a href="../26/Phishing.html">Phishing</a> (<a href="https://attack.mitre.org/techniques/T1566/">T1566</a>)</li>
        <li><a href="../27/Exploiting_Public-Facing_Apps.html">Exploiting Public-Facing Applications</a> (<a href="https://attack.mitre.org/techniques/T1190/">T1190</a>)</li>
        <li><a href="../28/Trusted_Relationship.html">Trusted Relationship</a> (<a href="https://attack.mitre.org/techniques/T1199/">T1199</a>)</li>
    </ol>
    <li>Execution:</li>
    <ol>
        <li><a href="../29/PowerShell.html">PowerShell</a> (<a href="https://attack.mitre.org/techniques/T1059/001/">T1059.001</a>)</li>
        <li><a href="../../04/01/Windows_Command_Shell.html">Windows Command Shell</a> (<a href="https://attack.mitre.org/techniques/T1059/003/">T1059.003</a>)</li>
        <li><a href="../../04/02/Command_and_Shell.html">Script Interpreter</a> (<a href="https://attack.mitre.org/techniques/T1059/">T1059</a>)</li>
    </ol>
    <li>Persistence:</li>
    <ol>
        <li><a href="../../04/03/Valid_Accounts.html">Valid Accounts</a> (<a href="https://attack.mitre.org/techniques/T1078/">T1078</a>)</li>
        <li><a href="../../04/09/Server_Software_Component.html">Server Software Component</a> (<a href="https://attack.mitre.org/techniques/T1505/">T1505</a>)</li>
        <li><a href="../../04/10/Scheduled_taks_Job.html">Scheduled Task/Job</a> (<a href="https://attack.mitre.org/techniques/T1053/">T1053</a>)</li>
    </ol>
    <li>Privilege Escalation:</li>
    <ol>
        <li><a href="../../04/11/Exploitation_for_Privilege_Escalation.html">Exploitation for Privilege Escalation</a> (<a href="https://attack.mitre.org/techniques/T1068/">T1068</a>)</li>
        <li><a href="../../04/15/Process_Injection.html">Process Injection</a> (<a href="https://attack.mitre.org/techniques/T1055/">T1055</a>)</li>
        <li><a href="../../04/16/Bypass_User_Account_Control.html">Bypass User Account Control</a> (<a href="https://attack.mitre.org/techniques/T1548/">T1548</a>)</li>
    </ol>
    <li>Defense Evasion:</li>
    <ol>
        <li><a href="../../04/17/Masquerading.html">Masquerading</a> (<a href="https://attack.mitre.org/techniques/T1036/">T1036</a>)</li>
        <li><a href="../../04/18/Obfuscated_Files_or_Information.html">Obfuscated Files or Information</a> (<a href="https://attack.mitre.org/techniques/T1027/">T1027</a>)</li>
        <li><a href="../../05/08/Disabling_Security_Tools.html">Disabling Security Tools</a> (<a href="https://attack.mitre.org/techniques/T1562/001/">T1089</a>)</li>
    </ol>
    <li>Credential Access:</li>
    <ol>
        <li><a href="../../05/13/OS_Credential_Dumping.html">OS Credential Dumping</a> (<a href="https://attack.mitre.org/techniques/T1003/">T1003</a>)</li>
        <li><a href="../../05/16/Brute_Force.html">Brute Force</a> (<a href="https://attack.mitre.org/techniques/T1110/">T1110</a>)</li>
        <li><a href="../../05/17/Unsecure_Credentials.html">Unsecured Credentials</a> (<a href="https://attack.mitre.org/techniques/T1552/">T1552</a>)</li>
    </ol>
    <li>Discovery:</li>
    <ol>
        <li><a href="../../05/21/Account_Discovery.html">Account Discovery</a> (<a href="https://attack.mitre.org/techniques/T1087/">T1087</a>)</li>
        <li><a href="../../05/22/System_Information_Discovery.html">System Information Discovery</a> (<a href="https://attack.mitre.org/techniques/T1082/">T1082</a>)</li>
        <li><a href="../../05/23/Network_Share_Discovery.html">Network Share Discovery</a> (<a href="https://attack.mitre.org/techniques/T1135/">T1135</a>)</li>
    </ol>
    <li>Lateral Movement:</li>
    <ol>
        <li><a href="../../05/24/Remote_Services.html">Remote Services</a> (<a href="https://attack.mitre.org/techniques/T1021/">T1021</a>)</li>
        <li><a href="../../05/28/Windows_Admin_Shares.html">Windows Admin Shares</a> (<a href="https://attack.mitre.org/techniques/T1021/002/">T1077</a>)</li>
        <li><a href="../../05/29/Exploitation_of_Remote_Services.html">Exploitation of Remote Services</a> (<a href="https://attack.mitre.org/techniques/T1210/">T1210</a>)</li>
    </ol>
    <li>Collection:</li>
    <ol>
        <li>Data from Local System (<a href="https://attack.mitre.org/techniques/T1005/">T1005</a>)</li>
        <li>Data from Network Shared Drive (T1039)</li>
        <li>Email Collection (T1114)</li>
    </ol>
    <li>Exfiltration:</li>
    <ol>
        <li>Exfiltration Over C2 Channel (T1041)</li>
        <li>Exfiltration Over Alternative Protocol (T1048)</li>
        <li>Automated Exfiltration (T1020)</li>
    </ol>
</ol></p>
<p>By understanding these common techniques, organizations can implement effective countermeasures, enhance their security posture, and stay ahead of potential threats. Join us as we dive deep into each category, dissecting the tactics and providing actionable insights for defending against these pervasive cyber attack methods.</p>

<p>Stay tuned for the upcoming blog posts, where we will explore each technique in detail, empowering you with the knowledge to fortify your defenses and protect your organization from cyber threats.</p>

</div>
</article> <!-- end entry -->

</div> <!-- end main -->  