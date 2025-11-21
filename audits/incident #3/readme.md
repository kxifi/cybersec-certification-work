# README: Cybersecurity Incident Analysis - Denial-of-Service (DoS)

## 1. Overview
This README summarizes the findings regarding a recent network interruption that caused the company website to display a timeout error message to users[cite: 1]. The incident has been identified as a Denial-of-Service (DoS) attack, specifically a SYN flood, that overloaded the company servers and halted internet-based business operations.

## 2. Key Findings

| Detail | Value | Source |
| :--- | :--- | :--- |
| **Attack Type** | Denial-of-Service (DoS) Attack | [cite: 1] |
| **Specific Technique** | Persistent SYN requests (SYN Flood) | [cite: 1] |
| **Attacker IP Address** | `203.0.113.0` | [cite: 1, 2, 3] |
| **Target/Company Server IP** | `192.0.2.1` (Port 443) | [cite: 2, 3] |
| **Impact** | Website connection timeout errors, servers throttled/overloaded, inability to respond to legitimate users, halting of all business operations[cite: 1]. | [cite: 1, 2, 3] |

## 3. Technical Attack Mechanism

The attack exploits the TCP (Transmission Control Protocol) three-way handshake process used to establish a connection between a user (client) and the web server[cite: 1].

* [cite_start]**Normal Connection:** A legitimate user sends a **SYN** (synchronize) request, the server responds with a **SYN-ACK**, and the user finalizes the connection with an **ACK** (acknowledge) request[cite: 1].
* [cite_start]**Attack Action:** The attacker's IP address (`203.0.113.0`) persistently sends a high volume of **SYN** requests—approximately 2-3 per second—to the company website (`192.0.2.1`)[cite: 1].
* **Result (DoS):** This flood of SYN requests quickly consumes the network's bandwidth and overloads the server. [cite_start]Because the server is throttled and busy processing the malicious requests, it is unable to complete the handshake process (send SYN-ACK) to legitimate users, resulting in a denial of service for all normal traffic[cite: 1].

## 4. Data Source Reference

The analysis and conclusions are based on the following files in this folder:

**`Cybersecurity-incident-report-2.docx`**: Provides the primary analysis, attack identification, explanation of the mechanism, and identification of the attacker IP (`203.0.113.0`)
**`HTTP-log.xlsx - TCP log.csv` / `HTTP-log.xlsx - Color coded TCP log.csv`**: Contains the raw network traffic log data confirming the attack activity.
Log entries colored **red** indicate the attack activity.
The logs show persistent `[SYN]` requests from the source IP `203.0.113.0` to the destination IP `192.0.2.1`.
Log entries colored **yellow** indicate normal TCP connections failing due to the attack.