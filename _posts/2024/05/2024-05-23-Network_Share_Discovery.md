---
layout: blog
title: Network Share Discovery
---


<div id="main" class="s-content__main large-8 column">
<article class="entry">

<header class="entry__header">

<h2 class="entry__title h1">
    Network Share Discovery
</h2>        
</header>

<div class="entry__content">

<p>Let's talk about the MITRE ATT&CK Framework technique Network Share Discovery (T1135). This technique allows attackers to identify shared network resources, which they can then exploit for further malicious activities. In this post, we’ll delve into what Network Share Discovery entails, provide real-world examples, discuss detection methods, and outline effective mitigation strategies.</p>

<h5>Understanding Network Share Discovery (T1135)</h5>

<p>Network Share Discovery involves adversaries probing a network to find accessible shared directories or files. By identifying these network shares, attackers can determine valuable targets for data exfiltration, lateral movement, or further exploitation. This technique is commonly used in the reconnaissance phase after gaining initial access to a network.</p>

<p>On Windows systems, attackers might use commands like <code>net view</code> and <code>net share</code> to list network shares. Similarly, tools like <code>smbclient</code> can be used in Unix-based environments to discover shared resources.</p>

<h5>>Real-World Examples</h5>
<ol>
<li><strong>EternalBlue Exploit:</strong> The EternalBlue exploit, used in the WannaCry ransomware attack, scanned for vulnerable network shares to propagate itself across infected networks. Once a share was found, the ransomware encrypted files and spread to other systems.</li>

<li><strong>Emotet Malware:</strong> Emotet, a notorious banking Trojan turned modular malware, has used network share discovery to locate and infect other systems within a compromised network. By identifying accessible shares, Emotet can move laterally and deploy additional payloads.</li>

<li><strong>APT34 Campaigns:</strong> APT34 (also known as OilRig) has utilized network share discovery during its operations to identify critical file shares and directories. This information helps them to steal sensitive data and facilitate lateral movement within targeted organizations.</li>
</ol>
<h5>Detection Methods</h5>

<p>Detecting Network Share Discovery activities requires vigilant monitoring of network and system activities. Here are some effective detection strategies:
<ol>
<li><strong>Command Monitoring:</strong></li>
<ul>
<li><strong>Windows Event Logs:</strong> Monitor for the execution of commands like <code>net view</code>, <code>net share</code>, and <code>net use</code>. Use Windows Event ID 5140 (a network share object was accessed) to track access to network shares.</li>
<li><strong>Linux Audit Logs:</strong> Use tools like <code>auditd</code> to log and alert on the execution of commands like <code>smbclient</code> and other file-sharing tools.</li>
</ul>
<li><strong>Network Traffic Analysis:</strong></li>
<ul>
<li><strong>SMB Traffic Monitoring:</strong> Monitor network traffic for unusual SMB (Server Message Block) protocol activity. Unusual patterns or high volumes of SMB traffic can indicate network share discovery or exploitation attempts.</li>
<li><strong>Anomaly Detection:</strong> Implement network anomaly detection systems to flag unexpected access to network shares, particularly from non-standard users or devices.</li>
</ul>
<li><strong>File Access Monitoring:</strong></li>
<ul>
<li><strong>File Integrity Monitoring (FIM):</strong> Use FIM tools to monitor critical directories and files for unauthorized access. Detecting unauthorized access attempts can indicate malicious reconnaissance.</li>
</ul></ol></p>

<h5>Mitigation Methods</h5>

<p>Mitigating the risks associated with Network Share Discovery requires a combination of preventive measures and active defenses. Here are key mitigation strategies:
<ol>
<li><strong>Principle of Least Privilege:</strong></li>
<ul>
<li><strong>Restrict Share Access:</strong> Ensure that network shares are only accessible to users who absolutely need access. Implement role-based access controls (RBAC) to enforce this principle.</li>
<li><strong>Regular Access Reviews:</strong> Periodically review access permissions for network shares and remove unnecessary permissions.</li>
</ul>
<li><strong>Network Segmentation:</strong></li>
<ul>
<li><strong>Isolate Sensitive Data:</strong> Segment your network to isolate sensitive data and critical systems. Use VLANs and subnetting to limit the exposure of network shares.</li>
<li><strong>Firewall Rules:</strong> Implement strict firewall rules to control and restrict access to network shares.</li>
</ul>
<li><strong>System Hardening:</strong></li>
<ul>
<li><strong>Disable Unnecessary Shares:</strong> Disable and remove unnecessary network shares. Ensure that critical shares are properly secured and monitored.</li>
<li><strong>Strong Authentication:</strong> Implement strong authentication mechanisms for accessing network shares. Use multi-factor authentication (MFA) to add an additional layer of security.</li>
</ul>
<li><strong>Monitoring and Incident Response:</strong></li>
<ul>
<li><strong>Active Monitoring:</strong> Continuously monitor for signs of network share discovery and other reconnaissance activities. Implement automated responses to quickly address detected threats.</li>
<li><strong>Incident Response Plans:</strong> Develop and regularly update incident response plans to handle potential breaches effectively. Train your team to recognize and respond to network share discovery attempts.</li>
</ul>

<li><strong>User Training and Awareness:</strong></li>
<ul>
<li><strong>Security Training:</strong> Educate users about the risks associated with network shares and the importance of securing sensitive information. Encourage best practices for data storage and sharing.</li>
</ul></ol></p>
<h5>Conclusion</h5>

<p>Network Share Discovery (T1135) is a critical technique used by adversaries to identify and exploit shared resources within a network. By understanding this technique, implementing robust detection methods, and adopting comprehensive mitigation strategies, organizations can significantly reduce their risk of compromise. As cybersecurity professionals, it is our duty to stay vigilant, proactive, and informed to effectively safeguard our digital environments against persistent threats.</p>

<p><a href="../../03/25/MITRE_Att&ck_Intro.html">Most Common MITRE Att&ck Techniques</a></p>

</div>
</article> <!-- end entry -->

</div> <!-- end main -->  