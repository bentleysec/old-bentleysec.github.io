---
layout: blog
title: Account Discovery
---


<div id="main" class="s-content__main large-8 column">
<article class="entry">

<header class="entry__header">

<h2 class="entry__title h1">
    Account Discovery
</h2>        
</header>

<div class="entry__content">

<p>As a cybersecurity engineer, understanding the tactics and techniques employed by adversaries is crucial to fortifying our defenses. One such technique within the MITRE ATT&CK framework that plays a pivotal role in many attacks is Account Discovery (T1087). This post will delve into what Account Discovery entails, provide real-world examples, discuss detection methods, and outline mitigation strategies to help protect your organization.</p>

<h5>Understanding Account Discovery (T1087)</h5>

<p>Account Discovery involves adversaries attempting to enumerate user and service accounts on a system or network. This technique is often a precursor to further malicious activities, such as lateral movement or privilege escalation, as it helps attackers identify accounts with elevated privileges or those that are otherwise valuable targets.</p>

<p>Attackers can leverage various tools and commands to gather information about accounts, including local and domain accounts. On Windows systems, commands like <code>net user</code> and <code>net group</code> are commonly used, while on Unix-based systems, commands such as <code>cat /etc/passwd</code> can reveal a list of user accounts.</p>

<h5>Real-World Examples</h5>
<p><ol>
<li><strong>Windows Environment Enumeration:</strong> Attackers who gain initial access to a Windows system often use commands like <code>net user</code> to list all user accounts. They may also use <code>net group "Domain Admins" /domain</code> to identify high-value accounts in a domain environment.</li>

<li><strong>Linux System Enumeration:</strong> On Linux systems, adversaries might read the <code>/etc/passwd</code> file to list user accounts or use the <code>getent passwd</code> command. This can provide valuable information about existing users and their roles on the system.</li>

<li><strong>Active Directory (AD) Enumeration:</strong> In Active Directory environments, attackers use tools like <code>BloodHound</code> or <code>PowerView</code> to map out users, groups, and their relationships. This detailed mapping helps attackers identify potential targets for privilege escalation or lateral movement.</li>
</ol></p>

<h5>Detection Methods</h5>

<p>Detecting Account Discovery activities involves monitoring system commands and network activity for signs of enumeration. Key detection strategies include:
<ol>
<li><strong>Command Monitoring:</strong></li>
<ul>
<li><strong>Windows Event Logs:</strong> Monitor for the execution of commands like <code>net user</code>, <code>net group</code>, and <code>net localgroup</code>. Windows Event ID 4688 (a new process has been created) can be used to track these commands.</li>
<li><strong>Linux Audit Logs:</strong> Use tools like <code>auditd</code> to log and alert on access to sensitive files such as <code>/etc/passwd</code> or the execution of commands like <code>cat</code> and <code>getent</code>.</li>
</ul>
<li><strong>Network Traffic Analysis:</strong></li>
<ul>
<li><strong>Network Monitoring Tools:</strong> Use network monitoring tools to detect unusual LDAP queries or SMB traffic that may indicate enumeration of Active Directory accounts.</li>
<li><strong>SIEM Integration:</strong> Integrate detection rules into your Security Information and Event Management (SIEM) system to correlate suspicious activities and generate alerts.</li>
</ul>
<li><strong>Anomaly Detection:</strong></li>
<ul>
<li><strong>Behavioral Analytics:</strong> Implement User and Entity Behavior Analytics (UEBA) to establish baselines for normal account enumeration activities and detect deviations that may indicate malicious intent.</li>
</ul>
</ol></p>
<h5>Mitigation Methods</h5>

<p>Mitigating Account Discovery requires a combination of preventive measures and active defenses. Effective strategies include:
<ol>
<li><strong>Principle of Least Privilege:</strong></li>
<ul>
<li><strong>Access Controls:</strong> Ensure that users and service accounts have the minimum privileges necessary to perform their tasks. Regularly review and audit permissions to prevent privilege creep.</li>
<li><strong>Network Segmentation:</strong> Segment your network to limit the visibility of sensitive account information and restrict access to critical systems.</li>
</ul>
<li><strong>Hardening Systems:</strong></li>
<ul>
<li><strong>Disable Unnecessary Services:</strong> Disable services and protocols that are not needed, reducing the attack surface for enumeration.</li>
<li><strong>Secure Configuration:</strong> Harden system configurations by applying security best practices, such as using strong password policies and disabling guest accounts.</li>
</ul>
<li><strong>Monitoring and Response:</strong></li>
<ul>
<li><strong>Active Monitoring:</strong>Continuously monitor for signs of account enumeration and other suspicious activities. Implement automated responses to quickly address detected threats.</li>
<li><strong>Incident Response Plans:</strong> Develop and regularly update incident response plans to handle potential breaches effectively. Ensure that your team is trained to recognize and respond to Account Discovery attempts.</li>
</ul>
</ol></p>
<h5>Conclusion</h5>

<p>Account Discovery (T1087) is a critical technique used by adversaries to gather information about user and service accounts, setting the stage for more advanced attacks. By understanding this technique, implementing robust detection methods, and adopting comprehensive mitigation strategies, organizations can significantly reduce their risk of compromise. As cybersecurity professionals, staying vigilant and proactive in our defense strategies is essential to safeguarding our digital environments from persistent threats.</p>

<p><a href="../../03/25/MITRE_Att&ck_Intro.html">Most Common MITRE Att&ck Techniques</a></p>

</div>
</article> <!-- end entry -->

</div> <!-- end main -->  