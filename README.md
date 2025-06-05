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
![Image1](![count by source](https://github.com/user-attachments/assets/c26102ad-7c52-45b9-944f-650d2fa91ba1)

> 📌 **Image 2:** *Event types count (Error, Information, etc.)*
![Image2](![count by entrytype](https://github.com/user-attachments/assets/8cf4a74c-4591-47f8-a01e-88f16487d4a1)

> 📌 **Image 3:** *Timechart of event counts over time*
![Image3](![count by timechart ](https://github.com/user-attachments/assets/f308fd14-f042-48a7-ad9e-9283ecef6c64)

> 📌 **Image 4:** *Top occurring error messages*
![Image4] ![top messsage eroor](https://github.com/user-attachments/assets/5c1ad330-c8a5-48b2-bd16-e00353f47e89)

> 📌 **Image 5:** *Event categories breakdown*
![Image5] ![category ](https://github.com/user-attachments/assets/51a8ab6c-dea2-4092-a32d-a70a28d8dcab)

> 📌 **Image 6:** *ISP analysis for error logs*
![Image6](![isp](https://github.com/user-attachments/assets/2d254764-e935-4441-8c7d-926783f970f1)

> 📌 **Image 7:** *Login failure alerts*
![Image7](![login  failure](https://github.com/user-attachments/assets/520ccb72-c81c-45f5-a5a6-c3359bc75e79)


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


**📊 Notable Events & Use Cases**

- Created real-time alerts for login failure spikes.
- Mapped event categories to MITRE ATT&CK techniques.
- Correlated firewall, endpoint, and Windows logs to identify multi-stage attacks.
- Integrated threat intelligence to flag suspicious IPs.
- Reduced noise by refining SPL queries and detection thresholds.


**🎓 Learnings**

- Mastered log ingestion, normalization, and threat detection using Splunk.
- Developed expertise in writing effective SPL queries.
- Enhanced investigative workflows via event correlation and dashboards.
- Integrated external threat intelligence feeds.
- Gained insights into incident response and reporting for security audits.

**📚 References**

- Splunk Documentation
- MITRE ATT&CK Framework
- Splunk Security Essentials
- Windows Sysmon Documentation


🚀 Author: Manoj Mothukuru
