# 🔎 MDR Threat Hunting & Triage Platform

| Project Type | Core Discipline | Automation Level | Framework Core |
| :---: | :---: | :---: | :---: |
| **Cybersecurity Operations (SecOps)** | **Threat Hunting** | **Partial/Augmented** | **MITRE ATT&CK** |

A critical **Managed Detection and Response (MDR)** project focused on establishing a proactive threat hunting capability and optimizing the triage pipeline. This initiative significantly reduced dwell time, accelerated incident investigation, and integrated human expertise with automation platforms for highly contextualized security operations.

---

## 1. 🎯 Problem Statement & Project Goal

### Problem
Despite a functional SIEM/EDR stack, the organization's defenses were largely reactive. Threats were only identified after correlation rules fired, leading to significant **dwell time** and missed opportunities to detect sophisticated, low-and-slow attacks (e.g., Living off the Land techniques). Triage was inconsistent and often lacked the deep context necessary for rapid decision-making.

### Goal
To build a dedicated **Threat Hunting Program** that proactively identifies unknown threats using hypotheses derived from the **MITRE ATT&CK Framework**, and to implement a standardized, automated triage workflow that provides analysts with full context, **reducing investigation time by 30%**.

---

## 2. 🛠️ Technical Architecture & Hunting Stack

### Hunting Stack Components

| Category | Tool / Component | Role in Project |
| :--- | :--- | :--- |
| **Core Visibility** | **EDR Platform (e.g., SentinelOne/CrowdStrike)** | Provides rich endpoint telemetry (process activity, file changes) for hunting queries. |
| **Log Aggregation** | **Splunk/Elastic (SIEM)** | Centralized repository for correlation, behavioral analysis, and historical lookbacks. |
| **Automation** | **SOAR Tool (e.g., Phantom/XSOAR)** | Automates alert enrichment, case creation, and provides a standardized triage workflow interface. |
| **Intelligence** | **Threat Intel Feeds** | Ingests IOCs (Indicators of Compromise) and TTPs (Tactics, Techniques, and Procedures) to drive hunting hypotheses. |

### 🌐 Threat Hunting & Triage Workflow

| Step | Component | Action / Data Type |
| :--- | :--- | :--- |
| **1. Hypothesis** | Threat Hunting Team | Develops a query based on a **MITRE ATT&CK** technique (e.g., "Persistence: Scheduled Task"). |
| **2. Hunting Query** | EDR/SIEM | Executes query across the environment to identify suspicious, non-alerting activity. |
| **3. Detection & Alert** | Threat Hunter / Analyst | Confirms suspicious finding and submits it as a high-fidelity alert to the SOAR tool. |
| **4. Triage & Enrichment**| SOAR Playbook | Automatically enriches the alert with asset information, user details, and threat intel lookups. |
| **5. Response** | Analyst / SOAR | Human-driven investigation assisted by automated response actions (e.g., host isolation). |

---

## 3. 🚧 Key Challenges & Solutions

| Challenge | Solution Implemented | Impact |
| :--- | :--- | :--- |
| **High Hunting Noise** | Implemented **Analytic Stories** and developed hunting queries that focus exclusively on chained events and behavioral anomalies, not single events. | Significantly reduced false positives in hunting results, improving analyst efficiency. |
| **Manual Triage Inconsistency**| Standardized the triage process via a single **SOAR Triage Interface**, ensuring every alert followed the same enrichment and scoring steps. | Achieved a repeatable, auditable, and high-quality incident handling process. |
| **Measuring Hunting Value** | Created metrics focused on **"Time to Detect" (TTD)** for discovered threats and categorized findings by **ATT&CK Tactic** instead of traditional alert count. | Demonstrated direct business value by proving a reduction in overall threat dwell time. |

---

## 4. 🚀 Implementation & Methodology

The project was executed using a cyclical, intelligence-driven methodology (similar to the **Threat Hunting Loop**).

1.  **Phase I: Readiness & Integration (5 Weeks):** Ensured full log fidelity from EDR/SIEM tools. Integrated the hunting platform with the SOAR tool for seamless alert handoff.
2.  **Phase II: Hypothesis Development & Execution (7 Weeks):** Developed a core library of **25 high-priority hunting queries** based on organizational threat models (e.g., Ransomware/Espionage TTPs).
3.  **Phase III: Triage Automation & Standardization (5 Weeks):** Deployed a centralized, enriched triage playbook in SOAR, and trained SecOps staff on the new workflow and investigative tools.

---

## 5. 🛡️ Security Impact Snapshot (Key Accomplishments)

This MDR project established a proactive defense model, demonstrating immediate, quantifiable improvements in threat detection and response capabilities.

| Security Domain | Core Action & Technology | Quantifiable Impact |
| :--- | :--- | :--- |
| **Threat Hunting** | **Pioneered** a dedicated threat hunting program leveraging EDR telemetry and MITRE ATT&CK hypotheses. | **40%** reduction in average threat dwell time (time between compromise and detection). |
| **Triage & Response** | **Streamlined** and automated alert enrichment via SOAR integration into the Security Operations Center (SOC) process. | **30%** reduction in average incident investigation time, freeing up analyst capacity. |
| **Vulnerability Analysis** | **Integrated** hunting findings with vulnerability scanning results to prioritize high-risk, exploited paths. | **90%** of identified security vulnerabilities related to threat actor TTPs were remediated first. |
| **Compliance & Reporting** | **Standardized** all alert logging and incident documentation via the SOAR platform. | **20%** increase in the accuracy and speed of mandatory incident reporting metrics. |

## 6. 🔭 Future Scope & Roadmap

To ensure the MDR platform maintains its edge against increasingly sophisticated threats:

* **Advanced Analytics:** Integrate Machine Learning to automate the creation of new hunting hypotheses based on trending attacker behavior.
* **Proactive Defense:** Develop and deploy automated **Deception Technology** to lure and detect attackers who bypass initial controls.
* **Contextual Scoring:** Implement a **Risk Scoring Model** within the SOAR platform that automatically adjusts alert severity based on the business criticality of the affected asset.

---

## 📸 Snapshot (Example Hunting Dashboard)

*A visualization showing the hunting results, TTP coverage, or the SOAR triage flow.*

### 🖼️ Contextual Triage Dashboard

![A mock-up dashboard showing a security alert alongside critical contextual data: MITRE ATT&CK mapping, Asset Criticality, and GeoIP location.](screenshots/triage_contextual_dashboard.jpg)
