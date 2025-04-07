# Log-Analysis-Threat-Hunting-with-Splunk


Objective

The goal of log analysis and threat hunting with Splunk is to centralize logs from servers, firewalls, and endpoints so we can detect suspicious activity—like strange logins or data leaks—that automated tools might miss. By correlating events (e.g., tracing a phishing email to malware spread), we uncover attack patterns and respond faster. Splunk helps prioritize critical alerts, automate investigations, and generate compliance reports while reducing false positives. Over time, we refine searches and integrate threat intelligence to catch hidden risks before they escalate, keeping defenses proactive and sharp.

Skills Learned 

- **Splunk Basics** – Navigating the interface, running searches, and using SPL (Search Processing Language) to dig through logs.  
- **Log Collection & Normalization** – Setting up data inputs, parsing raw logs, and making sure everything’s in a usable format.  
- **Detecting Anomalies** – Writing queries to spot weird behavior—failed logins, unusual file access, or unexpected network traffic.  
- **Threat Hunting Techniques** – Proactively searching for signs of compromise (IOCs, TTPs) instead of just waiting for alerts.  
- **Correlating Events** – Connecting the dots between different logs (e.g., firewall + endpoint + auth logs) to reconstruct attacks.  
- **Building Dashboards & Alerts** – Creating real-time visualizations and automated alerts for faster detection.  
- **Incident Investigation** – Using Splunk to trace attack timelines, pivot on suspicious activity, and gather evidence.  
- **Reducing False Positives** – Fine-tuning searches and rules to cut through noise and focus on real threats.  
- **Threat Intelligence Integration** – Enriching searches with external threat feeds (like MITRE ATT&CK) for better context.  
- **Reporting & Compliance** – Generating security reports for audits (PCI DSS, HIPAA, etc.) to prove you’re on top of risks.  

Tools Used 

- **Splunk Search** – The core tool for digging through logs with simple searches or complex SPL queries.  
- **Dashboards & Visualizations** – Built custom views to track security events in real time (like login attempts or suspicious traffic).  
- **Alerts & Scheduled Reports** – Set up automated alerts for weird activity (e.g., brute-force attacks) and scheduled reports for trends.  
- **Enterprise Security (ES)** – Used Splunk’s SIEM for threat detection, risk scoring, and case management.  
- **Threat Intelligence Framework (TIF)** – Added external threat feeds (like known bad IPs) to enrich investigations.  
- **Notable Events & Investigations** – Tracked high-priority alerts, assigned cases, and documented findings.  
- **Pivot & Correlation Searches** – Connected different log sources to find attack patterns (e.g., malware + lateral movement).  
- **Machine Learning Toolkit (MLTK)** – Ran anomaly detection models to spot outliers in user behavior or network traffic.  
- **Splunk UBA (User Behavior Analytics)** – Monitored for insider threats and compromised accounts.  
- **TA (Technology Add-ons) & Apps** – Installed add-ons for specific data sources (Windows logs, firewalls, cloud services).  
- **MITRE ATT&CK Integration** – Mapped findings to real-world attack techniques for better context.  
- **Splunk Phantom (SOAR)** – Automated responses (like blocking IPs or isolating endpoints) when threats were confirmed.  

Steps

Example below.

Image 1

![count by source](https://github.com/user-attachments/assets/3962b998-35c4-4535-8d42-9f3cded02c74)

Now we can see event log CCSV file is here so it means that the logs are Successfully Generated and we can view these logs by clicking on view events and analyze them.

Image 2

![count by entrytype](https://github.com/user-attachments/assets/c0acc484-11e7-457e-84b0-30ff0f34a454)

This Query will show us how many Event falls under each category and Error information etc.
we can see how many Events each category is containning.

Image 3 

![count by timechart ](https://github.com/user-attachments/assets/f0bd493a-92d2-463c-bf12-53c06300ca56)

This Query Dispalys a timeline of how different count types Error Information vary over time.

Image 4 

![top messsage eroor](https://github.com/user-attachments/assets/0ed3dd5b-bb59-49f3-931b-f3b1519b6096)

Here You can see the most Common Error Messages in the Logs.

Image 5 

![category ](https://github.com/user-attachments/assets/65fdbd3c-6a02-447d-984c-2b916471f253)

Here you can see and break down how many logs belongs to each category.

Image 6

![isp](https://github.com/user-attachments/assets/6bf7eacf-bf48-4d6f-b44d-fce99e94c1f4)

You can see and Analyze which ISPs are Linked to Error logs helpful for identifying network related issues.

Image 7 

![login  failure](https://github.com/user-attachments/assets/c04fd27b-6eef-4620-bc71-e909ab775390)

![evnt alert](https://github.com/user-attachments/assets/fc7a2449-0b0f-425f-ae51-52030d0e4b5d)

![alert](https://github.com/user-attachments/assets/98835ef7-afb5-4116-af8e-a5870be6617e)

As you can we are Creating a Alerts for Login Failure 

You can Analyze log events with different queries, you can Analyze to find failed login attempts by running Query as ( Index+maddy_logs event_type=login Status=failed | stats count by user )

You can also identify unusual IP activities, you can detect brute force and malware.








