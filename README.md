<img width="1280" height="800" alt="Screen Shot 2025-08-05 at 1 00 24 PM" src="https://github.com/user-attachments/assets/0b241bc8-512c-40b7-a134-50e5c92edca3" />
<h1>Overview</h1>
Garuda Firewall is an advanced PHP web application firewall designed to protect web applications from various types of attacks. It includes features such as Geo-IP filtering, DDoS protection, and prevention against XSS and SQL injection attacks. The firewall covers over 80 attack vectors.

<h1>Features</h1>
<h3>Geo-IP Filtering</h3>Restricts access based on geographical location.
<h3>DDoS Protection</h3>Mitigates distributed denial-of-service attacks.
<h3>XSS/SQL Injection Prevention</h3> Protects against cross-site scripting and SQL injection attacks.
<h3>Logging and Monitoring</h3>Logs events and provides debugging options.
<h3>Rate Limiting</h3>Controls the number of requests from a single IP address.
<h1>Installation</h1>
Clone the Repository:

bash

Run
Copy code
git clone https://github.com/yourusername/garuda-firewall.git
<h2>Configure the Firewall:</h2>

Open the GarudaFirewall.php file.
Adjust the configuration settings as needed, such as allowed countries and logging paths.
Include the Firewall in Your Application:

php
2 lines
Click to expand
require 'path/to/GarudaFirewall.php';
new GarudaFirewall();
Configuration
The firewall can be configured through the $config array in the GarudaFirewall class. Key configuration options include:

<h3>enable:</h3> Set to true to enable the firewall.
<h3>debug:</h3> Set to true to enable debug mode for logging.
<h3>allowed_countries:</h3> An array of country codes that are allowed access.
<h3>block_tor:</h3> Set to true to block requests from Tor exit nodes.
<h3>logging_path:</h3> Path to the log file.
<h3>rate_limit:</h3> Configuration for rate limiting requests.
<h3>Threat Intelligence</h3>
The firewall uses a set of threat intelligence databases to identify and block malicious requests. Key components include:

<h3>bad_ips:</h3> List of known bad IP addresses.
<h3>bad_user_agents:</h3> User agents that are known to be associated with malicious activity.
<h3>attack_patterns:</h3> Regular expressions that match common attack patterns, including SQL injection and XSS.
<h3>Usage
Once the firewall is initialized, it will automatically perform the following checks:

<h3>Session Security:</h3> Initializes secure session parameters.
<h3>Request Validation:</h3> Validates incoming requests against known threats.
<h3>Geo-IP Check:</h3> Verifies the geographical location of the request.
<h3>Rate Limiting:</h3> Monitors and limits the number of requests from a single IP.
<h3>Input Sanitization: </h3>Sanitizes user input to prevent injection attacks.
<h3>Logging</h3>
The firewall logs all blocked requests and events. Logs can be viewed by accessing the log file specified in the configuration. If debug mode is enabled, logs will also be output to the PHP error log.

<h2>Conclusion</h2>
Garuda Firewall is a powerful tool for securing PHP web applications against a wide range of threats. By configuring the firewall appropriately and integrating it into your application, you can significantly enhance your web application's security posture.

<h2>License</h2>
This project is licensed under the MIT License. See the LICENSE file for more details.


