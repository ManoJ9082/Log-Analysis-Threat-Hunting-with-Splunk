# 🛡️ Log Analysis & Threat Hunting with Splunk

A practical cybersecurity project focusing on centralized log management, threat hunting, and anomaly detection using Splunk.

---

## 📖 Table of Contents

- [🎯 Objective](#-objective)
- [🧠 Skills Learned](#-skills-learned)
- [🛠️ Tools Used](#-tools-used)
- [🚀 Project Workflow](#-project-workflow)
- [📸 Screenshots](#-screenshots)
- [🔍 Example SPL Queries](#-example-spl-queries)
- [📊 Notable Events & Use Cases](#-notable-events--use-cases)
- [🎓 Learnings](#-learnings)
- [📚 References](#-references)

---

## 🎯 Objective

The goal of this project was to centralize logs from servers, firewalls, and endpoints to detect suspicious activity such as unusual logins, data leaks, or malware propagation. By correlating events across different log sources, we aimed to uncover attack patterns, automate investigations, reduce false positives, and proactively hunt for threats using Splunk’s powerful analytics, alerting, and reporting capabilities.

---

## 🧠 Skills Learned

- Splunk Basics: Interface navigation, searches, and SPL (Search Processing Language)
- Log Collection & Normalization: Data input setup and log parsing
- Anomaly Detection: Writing detection queries for failed logins, unusual activity, etc.
- Threat Hunting: Proactively identifying Indicators of Compromise (IOCs) and Tactics, Techniques, and Procedures (TTPs)
- Event Correlation: Linking events across log sources to identify attack chains
- Dashboard & Alert Creation: Real-time visualizations and automated alerts
- Incident Investigation & Timeline Analysis
- False Positive Reduction through query fine-tuning
- Threat Intelligence Integration (MITRE ATT&CK mappings, external feeds)
- Reporting & Compliance automation

---

## 🛠️ Tools Used

- **Splunk Enterprise**
- **Splunk Search & SPL Queries**
- **Dashboards & Visualizations**
- **Alerts & Scheduled Reports**
- **Splunk Enterprise Security (ES)**
- **Threat Intelligence Framework (TIF)**
- **Pivot & Correlation Searches**
- **Splunk MLTK (Machine Learning Toolkit)**
- **Splunk UBA (User Behavior Analytics)**
- **MITRE ATT&CK Navigator Integration**
- **Splunk Phantom (SOAR)**
- **Technology Add-ons (TA) for data sources**

---

## 🚀 Project Workflow

1. **Set up log collection** from endpoints, servers, and firewalls.
2. **Ingest logs into Splunk**, ensuring normalization and parsing.
3. **Create detection use cases** for anomalies like failed logins and error messages.
4. **Correlate multiple log sources** (Windows, Firewall, Auth logs).
5. **Build custom dashboards** for real-time event monitoring.
6. **Set up alerts and automated responses** for high-priority events.
7. **Integrate threat intelligence feeds** and map findings to MITRE ATT&CK.
8. **Generate reports** for audits and compliance tracking.

---

## 📸 Screenshots

> 📌 **Image 1:** *Event log source count*
![count by source](https://github.com/user-attachments/assets/712f880a-6213-4f0b-a44d-e7f5a2d34524)

> 📌 **Image 2:** *Event types count (Error, Information, etc.)*
![count by entrytype](https://github.com/user-attachments/assets/4c53fde1-9d5f-49ef-8c1b-7fa9ef616cec)


> 📌 **Image 3:** *Timechart of event counts over time*
![count by timechart ](https://github.com/user-attachments/assets/2b966ab6-285e-4241-8ee7-1405b904263f)


> 📌 **Image 4:** *Top occurring error messages*
 ![top messsage eroor](https://github.com/user-attachments/assets/764819c1-f900-4b81-b165-477660ba6fb3)


> 📌 **Image 5:** *Event categories breakdown*
 ![category ](https://github.com/user-attachments/assets/5d08ebba-1f90-4c7e-94d7-0226c6ad565b)


> 📌 **Image 6:** *ISP analysis for error logs*
![isp](https://github.com/user-attachments/assets/5c68d00b-7dcf-4761-b29f-4c1efd5d64ca)


> 📌 **Image 7:** *Login failure alerts*
![login  failure](https://github.com/user-attachments/assets/465a0ad6-3529-45c9-a633-06e67c9be6fd)

> 📌 **Image 8:** *Event alert *
![evnt alert](https://github.com/user-attachments/assets/ed799210-87c8-465d-867a-01c17236695e)

> 📌 **Image 9:** * Login Failure alert *
![alert](https://github.com/user-attachments/assets/f9d25ae8-b61a-4547-b217-3db01acecfa6)



## 🔍 Example SPL Queries

- **Count events by source:**
  index=maddy_logs | stats count by source

  **Event types count:**
  index=maddy_logs | stats count by entryType

  **Timechart of event counts:**
  index=maddy_logs | timechart count by entryType

  **Top error messages:**
  index=maddy_logs | top message

  **Login failure detection:**
  index=maddy_logs event_type=login status=failed | stats count by user

  **ISP activity analysis:**
  index=maddy_logs | stats count by isp


## 📊 Notable Events & Use Cases

- Created real-time alerts for login failure spikes.
- Mapped event categories to MITRE ATT&CK techniques.
- Correlated firewall, endpoint, and Windows logs to identify multi-stage attacks.
- Integrated threat intelligence to flag suspicious IPs.
- Reduced noise by refining SPL queries and detection thresholds.


## 🎓 Learnings

- Mastered log ingestion, normalization, and threat detection using Splunk.
- Developed expertise in writing effective SPL queries.
- Enhanced investigative workflows via event correlation and dashboards.
- Integrated external threat intelligence feeds.
- Gained insights into incident response and reporting for security audits.

## 📚 References

- Splunk Documentation
- MITRE ATT&CK Framework
- Splunk Security Essentials
- Windows Sysmon Documentation


🚀 Author: Manoj Mothukuru
