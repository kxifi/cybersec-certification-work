# 🛡️ Cybersecurity Incident Analysis: DDoS Attack Mitigation Plan

This repository contains the analysis and mitigation plan for a simulated Distributed Denial of Service (DDoS) incident, structured according to the **National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF)**.

## 🎯 Project Goal

To apply the five core functions of the NIST CSF—**Identify, Protect, Detect, Respond, and Recover**—to a specific network security event. The primary objective is to transition from incident response actions to a comprehensive, long-term security strategy.

---

## 💻 Incident Scenario Summary

| Detail | Description |
| :--- | :--- |
| **Organization** | Multimedia company offering web design, graphic design, and social media marketing. |
| **Attack Type** | Distributed Denial of Service (DDoS) via **ICMP Flood**. |
| **Impact** | Internal network compromised for **two hours**; all network services stopped. |
| **Root Cause** | Vulnerability due to an **unconfigured firewall**. |
| **Initial Response** | Blocking incoming ICMP packets; stopping non-critical services; restoring critical services. |

---

## 📊 NIST CSF Application Summary

The following plan outlines the strategic and tactical measures required to address the DDoS incident and improve the organization’s security posture.

| CSF Function | Focus | Key Actions in Plan |
| :--- | :--- | :--- |
| **1. Identify** | **Risk Management & Asset Inventory** | Focus shifts to **regular audits** of all network systems and firewall configurations to proactively identify and close security gaps before they are exploited. |
| **2. Protect** | **Long-Term Safeguards & Policies** | Implementation of **permanent controls** including a new firewall rule to **limit ICMP packet rates**, an **IDS/IPS system for filtering**, and establishing new **policies and training** for secure firewall configuration. |
| **3. Detect** | **Monitoring & Alerting** | Implementation of tools designed for surveillance: **Source IP address verification** (to check for spoofing) and **network monitoring software** to continuously detect and flag abnormal traffic patterns. |
| **4. Respond** | **Containment & Investigation** | Procedures for **isolating affected systems** (Mitigation), **analyzing network logs** (Analysis) for forensic data, and **reporting** all incidents to management and legal authorities (Communications). |
| **5. Recover** | **Service Restoration & Business Continuity** | A systematic process for restoring operations, prioritizing the restoration of **critical network services first**, followed by non-critical services once the threat has subsided. Includes communication plans for restoration updates. |

---

## 💡 Key Learnings and Framework Distinction

The exercise highlighted a critical concept in cybersecurity analysis: the distinction between the five NIST CSF functions, particularly separating **proactive** from **reactive** measures.

| Incorrect Placement (Common Error) | Correct Placement (NIST Principle) |
| :--- | :--- |
| Placing firewall rules and IDS/IPS filtering in **Detect** or **Respond**. | These are **Protect**ive measures; they actively block or prevent the attack. |
| Placing "blocking traffic" or "stopping non-critical services" in **Protect**. | These are **Respond** (Mitigation) or **Recover** actions; they are performed *during* or *immediately after* an active attack. |
| Including data loss or phishing advice in the **Recover** section of a DDoS report. | **Recover** must focus strictly on **restoring the affected asset** (network service restoration in this case), not speculative, unrelated data issues. |

---

## 🗂️ Files and Resources

* `Incident-report-analysis.docx`: Blank template for the report.
* `Incident-report-analysis-final.docx`: Completed report (Your Draft).
* `Incident-report-analysis-exemplar.docx`: Exemplar showing the NIST CSF applied to a similar DDoS incident.
* `Applying-the-NIST-CSF-.docx`: Documentation of the five core NIST CSF functions.