## Personal Information

**Name:** N ASHWIN KUMAR  
**Team:** 404 NOT FOUND  
**Role:** Defense Analyst  
**Total Prompts:** 12  

---

## Summary Statistics
```
| Tool       | Count | Excellent | Good | Needed Work |
|------------|-------|-----------|------|-------------|
| Gemini Pro | 12    | 7         | 5    | -           |
```
---

## Prompt 1

**Date:** 01/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To differentiate RaaS from traditional malware for the introduction.

**Prompt Used:**  
Explain the key differences between traditional signature-based malware detection and modern Ransomware-as-a-Service (RaaS). Focus on “living off the land” techniques.

**Response Summary:**  
Gemini explained that RaaS relies on human affiliates using legitimate tools (PowerShell, WMI) rather than just malicious binaries. It highlighted that signature detection fails because unique encryption keys and obfuscation are used for each victim.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** It provided the exact terminology (“Living off the Land”, “Affiliates”) I needed for Section 4.1.

**How I Used This:**  
**Report Section:** 4.1 The Paradigm Shift  
**Specific Use:** Drafted the explanation of why static file hashes are ineffective against polymorphic threats.

**Verification:**  
**How Verified:** Cross-referenced with MITRE ATT&CK framework  
**Accuracy:** Yes

---

## Prompt 2

**Date:** 02/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To identify specific network indicators before encryption (“Left of Boom”).

**Prompt Used:**  
What are specific network anomalies indicating a ransomware attack in the staging phase? Include Event IDs for RDP brute force.

**Response Summary:**  
Gemini listed Event ID 4625 for RDP brute force and mentioned C2 beaconing patterns. It advised looking for high-frequency failures followed by a success.

**Quality Assessment:**  
**Rating:** Good  
**Why:** Gave specific Event IDs which made the section technical and accurate.

**How I Used This:**  
**Report Section:** 4.2.1 Network Anomalies  
**Specific Use:** Used the Event ID 4625 details to define RDP attacks.

**Verification:**  
**How Verified:** Checked Microsoft Security documentation  
**Accuracy:** Yes

---

## Prompt 3

**Date:** 02/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To refine RDP detection and reduce false positives.

**Prompt Used:**  
For Event ID 4625, which Logon Types should I filter for to specifically catch remote RDP or SMB attacks and avoid local service failures?

**Response Summary:**  
Gemini recommended filtering for **Logon Type 10 (Remote Interactive)** and **Logon Type 3 (Network)** to isolate external threats.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** This added critical technical accuracy to the RDP brute-force section, preventing alert fatigue.

**How I Used This:**  
**Report Section:** 4.2.1 Network Anomalies  
**Specific Use:** Added the specific Logon Type filtering rule.

**Verification:**  
**How Verified:** Verified against Microsoft auditing categories  
**Accuracy:** Yes

---

## Prompt 4

**Date:** 03/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To understand “Impossible Travel” as an indicator.

**Prompt Used:**  
What is “Impossible Travel” in the context of identity security and ransomware initial access?

**Response Summary:**  
Gemini defined it as a user account authenticating from two geographically distant locations within a timeframe that is physically impossible (e.g., NY to Moscow in 15 minutes).

**Quality Assessment:**  
**Rating:** Good  
**Why:** Provided a clear definition for a high-fidelity indicator.

**How I Used This:**  
**Report Section:** 4.2.1 Network Anomalies  
**Specific Use:** Added “Impossible Travel” as a key identity anomaly.

**Verification:**  
**How Verified:** N/A (Standard security concept)  
**Accuracy:** Yes

---

## Prompt 5

**Date:** 03/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To find specific command-line indicators for the behavioral table.

**Prompt Used:**  
Provide the exact command-line arguments attackers use to delete shadow copies using vssadmin, and the PowerShell command to disable Windows Defender.

**Response Summary:**  
Provided `vssadmin.exe delete shadows /all /quiet` and  
`Set-MpPreference -DisableRealtimeMonitoring $true`.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** I needed the exact syntax to make the Suspicious Behavior table credible.

**How I Used This:**  
**Report Section:** 4.3 Behavioral Indicators  
**Specific Use:** Copied commands directly into the Technical Command / Artifact column.

**Verification:**  
**How Verified:** Verified command syntax in a virtual machine  
**Accuracy:** Yes

---

## Prompt 6

**Date:** 04/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To compare free detection tools for the stack.

**Prompt Used:**  
Compare Sysmon vs Zeek for ransomware detection. Which one is better for endpoint visibility and which for network? Can they be used together?

**Response Summary:**  
Clarified that Sysmon is for endpoint visibility (process creation, arguments) while Zeek is for network traffic (lateral movement). Confirmed they are complementary.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Helped me distinguish between endpoint and network visibility tools.

**How I Used This:**  
**Report Section:** 4.5 Detection Tooling Stack  
**Specific Use:** Wrote Sections 4.5.1 (Sysmon) and 4.5.2 (Zeek).

**Verification:**  
**How Verified:** Checked official tool documentation  
**Accuracy:** Yes

---

## Prompt 7

**Date:** 05/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To generate the Sysmon configuration XML.

**Prompt Used:**  
Write a Sysmon XML configuration block to detect `vssadmin delete shadows` and `Set-MpPreference` commands.

**Response Summary:**  
Generated the valid XML code block used in Appendix A, targeting the identified commands.

**Quality Assessment:**  
**Rating:** Good  
**Why:** Provided the practical code snippet added to the report appendix.

**How I Used This:**  
**Report Section:** Appendix A: Practical Implementation  
**Specific Use:** Copied the XML code block for the Practical Lab section.

**Verification:**  
**How Verified:** Reviewed XML structure against Sysmon schema  
**Accuracy:** Yes

---

## Prompt 8

**Date:** 05/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To explain File Integrity Monitoring (FIM).

**Prompt Used:**  
What is File Integrity Monitoring (FIM) and how does it detect ransomware encryption? Suggest open-source tools.

**Response Summary:**  
Defined FIM as monitoring checksums of files and explained that rapid modification of many files is the trigger. Suggested OSSEC/Wazuh.

**Quality Assessment:**  
**Rating:** Good  
**Why:** Connected rapid file modification to a concrete tool category.

**How I Used This:**  
**Report Section:** 4.5.4 File Integrity Monitoring  
**Specific Use:** Added OSSEC/Wazuh as recommended tools.

**Verification:**  
**How Verified:** Checked Wazuh features list  
**Accuracy:** Yes

---

## Prompt 9

**Date:** 06/02/2026  
**AI Tool:** Gemini Pro  

**Purpose:**  
To research User and Entity Behavior Analytics (UEBA).

**Prompt Used:**  
Explain User and Entity Behavior Analytics (UEBA) in the context of ransomware. How does it detect living-off-the-land attacks?

**Response Summary:**  
Described UEBA as creating a baseline of normal activity and detecting intent even when credentials are valid.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Provided the logic for the Future-Proofing section.
