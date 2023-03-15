---
layout: blog
title: Important Windows Logs
---


<div id="main" class="s-content__main large-8 column">
    <article class="entry">

        <header class="entry__header">

            <h2 class="entry__title h1">
                Important Windows Logs
            </h2>        
        </header>
        
        <div class="entry__content">
        
        <p>As a cybersecurity professional, monitoring Windows logs is a critical part of identifying and responding to security threats. Windows logs record all kinds of system activity, including user logins, network connections, and application usage. However, not all Windows logs are equally important for security monitoring. In this blog post, we will discuss the most critical Windows logs to monitor for security.</p>

        <p><b>Security Log</b></p>

        <p>The Security log is one of the most important logs for security monitoring. This log records security-related events, such as user logon attempts, account lockouts, and changes to security policies. By monitoring the Security log, you can identify potential security breaches, such as failed login attempts from unauthorized users.</p>

        <p>Some critical event IDs to monitor in the Security log include:
        <ul>
            <li>Event ID 4624: Successful account logon.</li>
            <li>Event ID 4625: Failed account logon.</li>
            <li>Event ID 4768: Kerberos authentication ticket request.</li>
            <li>Event ID 4769: Kerberos service ticket request.</li>
            <li>Event ID 4776: Account authentication failed.</li>
        </ul></p>

        <p><b>Application Log</b></p>

        <p>The Application log is another critical log to monitor for security. This log records events related to application usage, such as application crashes, errors, and warnings. By monitoring the Application log, you can identify potential security vulnerabilities and exploits, such as errors or crashes caused by malware.</p>

        <p>Some critical event IDs to monitor in the Application log include:
        <ul>
            <li>Event ID 1000: Application crash.</li>
            <li>Event ID 1001: Application error.</li>
            <li>Event ID 1002: Application hang.</li>
            <li>Event ID 1003: Application failed to start.</li>
            <li>Event ID 1010: Application failed to start due to side-by-side configuration error.</li>
        </ul></p>

        <p><b>System Log</b></p>


        <p>The System log is another critical log to monitor for security. This log records events related to system activity, such as device driver installation, system startup and shutdown, and changes to system settings. By monitoring the System log, you can identify potential security breaches, such as unauthorized changes to system settings.</p>

        <p>Some critical event IDs to monitor in the System log include:
        <ul>
            <li>Event ID 7035: Service control manager event.</li>
            <li>Event ID 7045: Service installed.</li>
            <li>Event ID 7040: Service changed start type.</li>
            <li>Event ID 7024: Service started.</li>
            <li>Event ID 7036: Service stopped.</li>
        </ul></p>

        <p><b>Summary</b></p>

        <p>In conclusion, monitoring Windows logs is essential for identifying and responding to security threats. The Security, Application, and System logs are the most critical logs to monitor for security. By monitoring these logs and identifying critical event IDs, you can identify potential security breaches and vulnerabilities, and take appropriate action to protect your organization's IT infrastructure.</p>


        </div> 

    </article> <!-- end entry -->

</div> <!-- end main -->  