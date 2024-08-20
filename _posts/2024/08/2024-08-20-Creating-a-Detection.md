---
layout: blog
title: Creating a Detection
---


<div id="main" class="s-content__main large-8 column">
<article class="entry">

<header class="entry__header">

<h2 class="entry__title h1">
    Creating a Detection
</h2>        
</header>

<div class="entry__content">

<p>In our previous post, we introduced the concepts of Detection Engineering and Detection as Code (DaC), highlighting their importance in modern cybersecurity. Now, it’s time to dive into the practical side of things—specifically, how to write effective detection rules and implement them using Detection as Code principles.</p>

<h3>Understanding the Basics of Detection Rules</h3>
<p>At their core, detection rules are logic-based statements designed to identify specific patterns, behaviors, or anomalies that indicate a potential security threat. These rules can be used to detect everything from simple malware infections to complex, multi-stage attacks.</p>

<p>Detection rules typically consist of three key components:
<ol>
    <li><strong>Conditions</strong>: The specific criteria that must be met for the rule to trigger an alert. This could be anything from a particular IP address making a request to a server, to a series of failed login attempts within a short time frame.</li>
    <li><strong>Thresholds</strong>: Limits that define when a condition should be considered suspicious. For example, a rule might trigger if more than five failed login attempts occur within a minute.</li>
    <li><strong>Actions</strong>: The response the system should take when the rule is triggered, such as generating an alert, blocking traffic, or logging the event for further analysis.</li>
</ol></p>
<p>The effectiveness of a detection rule depends on its ability to accurately identify malicious activity while minimizing false positives. This requires a deep understanding of both the threat landscape and the environment being protected.</p>

<h3>Steps to Writing Effective Detection Rules</h3>
<p>Writing effective detection rules involves several steps:
<ol>
    <li><strong>Identify the Threat</strong>: Start by understanding the specific threat you want to detect. This could be based on known attack techniques, indicators of compromise (IoCs), or suspicious behaviors relevant to your environment.</li>
    <li><strong>Understand the Environment</strong>: Know the normal behavior of your systems, applications, and users. This helps in distinguishing between legitimate activities and potential threats, which is crucial for reducing false positives.</li>
    <li><strong>Define the Logic</strong>: Translate your understanding of the threat and environment into a logical condition that can be codified into a rule. This might involve specific IP addresses, user behaviors, network traffic patterns, or file activities.</li>
    <li><strong>Test the Rule</strong>: Before deploying, test the rule in a controlled environment to ensure it behaves as expected. This helps catch any issues that could lead to unnecessary alerts or missed detections.</li>
    <li><strong>Review and Refine</strong>: Detection rules should be continuously reviewed and refined as new information becomes available. This is where collaboration and peer reviews come in handy, ensuring the rule remains effective over time.</li>
</ol></p>
<h3>Implementing Detection Rules Using Detection as Code</h3>
<p>Once you have a well-crafted detection rule, the next step is implementing it using Detection as Code principles. Here’s how:
<ol>
    <li><strong>Version Control Your Rules</strong>: Store your detection rules in a version control system (e.g., Git). This allows you to track changes, collaborate with other team members, and maintain a history of modifications. Each rule should be treated like code, with meaningful commit messages explaining what has changed and why.</li>
    <li><strong>Automate Testing</strong>: Just like software, detection rules should be tested automatically before deployment. Create test cases that simulate both malicious and benign behaviors to ensure the rule triggers correctly. This helps catch false positives and negatives early.</li>
    <li><strong>Continuous Integration/Continuous Deployment (CI/CD)</strong>: Use CI/CD pipelines to automatically deploy your detection rules across your environment. This ensures that updates are rolled out consistently and quickly, reducing the window of vulnerability.</li>
    <li><strong>Monitor and Iterate</strong>: Once deployed, continuously monitor the performance of your detection rules. Collect feedback from the SOC team, analyze the alerts generated, and iterate on the rules as needed. The goal is to maintain high detection efficacy while minimizing noise.</li>
</ol></p>
<h3>Example: Writing a Detection Rule for Brute Force Attacks</h3>
<p>Let’s walk through a simple example: writing a detection rule to identify brute force attacks on a web application.
<ol>
    <li><strong>Identify the Threat</strong>: Brute force attacks involve repeated attempts to guess a username and password combination. These attacks often result in multiple failed login attempts within a short period.</li>
    <li><strong>Understand the Environment</strong>: In this scenario, normal login attempts typically do not exceed a few tries within a minute. A sudden spike in failed attempts is unusual and could indicate an attack.</li>
    <li><strong>Define the Logic</strong>:
    <ul>
        <li><strong>Condition</strong>: If more than 10 failed login attempts are detected from the same IP address within 60 seconds.</li>
        <li><strong>Threshold</strong>: Set at 10 attempts to balance between detecting real attacks and avoiding false positives.</li>
        <li><strong>Action</strong>: Generate an alert and potentially block the IP address temporarily.</li>
        <code class="yaml">
        rule:<br>
            &nbsp;&nbsp;name: "Detect Brute Force Attacks"<br>
            &nbsp;&nbsp;description: "Triggers when more than 10 failed login attempts are detected from the same IP within 60 seconds."<br>
            &nbsp;&nbsp;conditions:<br>
                &nbsp;&nbsp;&nbsp;&nbsp;- failed_login_attempts > 10<br>
                &nbsp;&nbsp;&nbsp;&nbsp;- timeframe: 60s<br>
            &nbsp;&nbsp;actions:<br>
            &nbsp;&nbsp;&nbsp;&nbsp;- alert: "Brute force attack detected"<br>
            &nbsp;&nbsp;&nbsp;&nbsp;- block_ip: true<br>
        </code>
    </ul>
    <li><strong>Test the Rule</strong>: Simulate both benign and malicious login attempts to ensure the rule triggers appropriately.</li>
    <li><strong>Implement Using DaC</strong>:
        <ul>
            <li><strong>Version Control</strong>: Commit the rule to a Git repository with a clear commit message.</li>
            <li><strong>Automate Testing</strong>: Set up automated tests within your CI/CD pipeline.</li>
            <li><strong>Deploy</strong>: Use the CI/CD pipeline to deploy the rule across your environment.</li>
        </ul>
    </li>
</ol></p>
<h3>Conclusion</h3>
<p>Writing detection rules is a critical skill for any Detection Engineer, and implementing these rules using Detection as Code principles ensures that your detection logic is robust, scalable, and easy to manage. By following a structured approach to rule creation, testing, and deployment, you can significantly improve your organization's ability to detect and respond to threats in real time.</p>
</div>
</article> <!-- end entry -->

</div> <!-- end main -->  