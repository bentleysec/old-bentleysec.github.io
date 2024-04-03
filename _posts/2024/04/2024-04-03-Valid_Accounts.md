---
layout: blog
title: Valid Accounts
---


<div id="main" class="s-content__main large-8 column">
<article class="entry">

<header class="entry__header">

<h2 class="entry__title h1">
    The Dangers of Account Misuse: Valid Accounts Technique
</h2>        
</header>

<div class="entry__content">

<p>As cyber defenders, we have to watch for attackers leveraging legitimate tools and permissions in devious ways. One sneaky technique hackers rely on is called "Valid Accounts" - let's dive into what this is.</p>

<h4>What Are Valid Accounts?</h4>

<p>Valid accounts refer to user accounts that are meant for actual employees, contractors, or system processes. These accounts have approved permissions to access resources on a network or system.</p>

<p>For example, a finance department employee has a valid account to log into accounting applications. A backup service has a valid system account to run automated backup jobs.</p>

<h4>How Attackers Abuse Valid Accounts</h4>

<p>The danger is that attackers may compromise and misuse these valid accounts to move around and cause damage, while blending in with normal activity.</p>

<p>Some ways hackers abuse valid accounts:
<ul>
<li>Stealing credentials to take over user accounts</li>
<li>Hijacking accounts of legitimate system processes</li>
<li>Creating new fake "valid" accounts by exploiting misconfigurations</li>
</ul></p>
<p>With a foothold as a valid account, attackers can more easily conduct reconnaissance, escalate privileges, move laterally, and access sensitive data - all while impersonating normal activity.</p>

<h4>Mitigating Valid Account Risks</h4>

<p>To limit valid account abuse, cybersecurity teams should:
<ul>
<li>Enforce the principle of least privilege for user accounts</li>
<li>Remove/disable unnecessary accounts and permissions</li>
<li>Use multi-factor authentication for sensitive accounts</li>
<li>Require separate management accounts from user accounts</li>
</ul></p>
<h4>Detecting Valid Account Misuse</h4>

<p>Signs that a valid account may be compromised include:
<ul>
<li>Account logging in from unusual locations/IP addresses</li>
<li>Accounts accessing resources they shouldn't need</li>
<li>Multiple accounts used simultaneously in a short period</li>
<li>Accounts used at strange hours outside work schedule</li>
</ul></p>
<p>Monitoring tools can alert on these indicators. Solutions like user behavior analytics can also baseline normal activity to spot deviations.</p>

<p>Valid accounts provide attackers with cover and increased access - which is why this technique is so dangerous. Adopting a least privilege model and vigilant monitoring is critical.</p>

<p>Let me know if any part of this needs clarification or expansion when it comes to explaining the Valid Accounts technique!</p>

<p><a href="../../03/25/MITRE_Att&ck_Intro.html">Most Common MITRE Att&ck Techniques</a></p>

</div>
</article> <!-- end entry -->

</div> <!-- end main -->  