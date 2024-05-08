---
layout: blog
title: Disabling Security Tools
---


<div id="main" class="s-content__main large-8 column">
<article class="entry">

<header class="entry__header">

<h2 class="entry__title h1">
    Disabling Security Tools
</h2>        
</header>

<div class="entry__content">
<p>
As cybersecurity professionals, we rely on a robust set of security tools to safeguard our organizations from threats. However, adversaries are constantly devising ways to circumvent these defenses, and one particularly concerning tactic is disabling security tools, tracked as T1089 in the Mitre ATT&CK framework.
</p>
<p>
What Is Disabling Security Tools? This technique involves an attacker taking actions to neutralize or render ineffective the security software deployed on a system or network. By disabling or tampering with security tools like antivirus, firewalls, host-based sensors, and other protective measures, adversaries can gain a foothold and operate more freely without detection.
</p>
<p>
Common Methods Adversaries employ various methods to disable security tools, including:
<ol>
<li>Killing security software processes</li>
<li>Modifying configuration files or registry keys</li>
<li>Uninstalling or deleting security software components</li>
<li>Exploiting vulnerabilities in security tools</li>
<li>Tampering with security tool updates</li>
<li>Disabling security services or scheduled tasks</li>
</ol>
</p>
<p>
Real-World Examples
<ul>
<li>The notorious Emotet malware disables Windows Defender and other security products by modifying registry keys and terminating processes.</li>
<li>The SamSam ransomware was found killing security processes like those of Symantec and CylancePROTECT.</li>
<li>The FIN7 threat group used a tool called BITSADMIN to disable Windows Defender on targeted systems.</li>
</ul>
</p>
<p>
<strong>Detecting Security Tool Tampering</strong> - While disabling security tools aims to evade detection, there are still ways to identify such activity:
<ol>
<li>Monitor process creation and termination events for signs of security software being killed.</li>
<li>Watch for unauthorized modifications to configuration files, registry keys, or scheduled tasks related to security tools.</li>
<li>Leverage security information and event management (SIEM) solutions to correlate and analyze logs for suspicious patterns.</li>
<li>Implement application control policies to restrict execution of unauthorized binaries or scripts targeting security tools.</li>
</ol>
</p>
<p>
<strong>Mitigating the Threat</strong> - To mitigate the risk of security tools being disabled, organizations should consider the following measures:
<ol>
<li>Deploy security solutions with tamper protection, self-healing capabilities, and robust update mechanisms.</li>
<li>Implement application whitelisting and strict execution policies to prevent unauthorized modification or termination of security processes.</li>
<li>Leverage virtualization or containerization to isolate and protect security tools from the main operating environment.</li>
<li>Regularly audit and review security tool configurations, logs, and update status for anomalies.</li>
<li>Provide security awareness training to educate users on the risks of disabling security tools and the potential consequences.</li>
</ol>
</p>
<p>
By adopting a defense-in-depth approach and staying vigilant against attempts to disable security tools, organizations can enhance their resilience against this evasive attack technique and maintain a strong security posture.
</p>

<p><a href="../../03/25/MITRE_Att&ck_Intro.html">Most Common MITRE Att&ck Techniques</a></p>

</div>
</article> <!-- end entry -->

</div> <!-- end main -->  