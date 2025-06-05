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
![Image1](images/image1.png)

> 📌 **Image 2:** *Event types count (Error, Information, etc.)*
![Image2](images/image2.png)

> 📌 **Image 3:** *Timechart of event counts over time*
![Image3](images/image3.png)

> 📌 **Image 4:** *Top occurring error messages*
![Image4](images/image4.png)

> 📌 **Image 5:** *Event categories breakdown*
![Image5](images/image5.png)

> 📌 **Image 6:** *ISP analysis for error logs*
![Image6](images/image6.png)

> 📌 **Image 7:** *Login failure alerts*
![Image7](images/image7.png)

---

## 🔍 Example SPL Queries

- **Count events by source:**
  ```spl
  index=maddy_logs | stats count by source
