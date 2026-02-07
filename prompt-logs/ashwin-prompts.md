## Personal Information

**Name:** N ASHWIN KUMAR

**Team:** 404 NOT FOUND

**Role:** Defense Analyst

**Total Prompts:** 12

---

## Summary Statistics
```
|    Tool    | Count | Excellent | Good | Needed Work |
| ---------- | ----- | --------- | ---- | ----------- |
| Gemini pro | 12    | 7         | 5    | -           |
```
---


## Prompt 1

**Date:** 01/02/2026
**AI Tool:** Gemini pro
**Purpose:** To differentiate RaaS from traditional malware for the introduction.
**The Prompt I Used:** "Explain the key differences between traditional signature-based malware detection and modern Ransomware-as-a-Service (RaaS). Focus on 'living off the land' techniques."
**Response Summary:** Gemini explained that RaaS relies on human affiliates using legitimate tools (PowerShell, WMI) rather than just malicious binaries. It highlighted that signature detection fails because unique encryption keys and obfuscation are used for each victim.
**Quality Assessment:** Excellent.
**Why:** It provided the exact terminology ("Living off the Land", "Affiliates") I needed for Section 4.1.
**How I Used This:**
    **Report Section:** 4.1 The Paradigm Shift.
    **Specific Use:** Drafted the explanation of why static file hashes are ineffective against polymorphic threats.
**Verification:**
    **How Verified:** Cross-referenced with MITRE ATT&CK framework.
    **Accuracy:** Yes.

## Prompt 2

**Date:** 02/02/2026
**AI Tool:** Gemini pro
**Purpose:** To identify specific network indicators before encryption ("Left of Boom").
**The Prompt I Used:** "What are specific network anomalies indicating a ransomware attack in the staging phase? Include Event IDs for RDP brute force."
**Response Summary:** Gemini listed Event ID 4625 for RDP brute force and mentioned C2 beaconing patterns. It advised looking for high-frequency failures followed by a success.
**Quality Assessment:** Good.
**Why:** Gave specific Event IDs which made the section technical and accurate.
**How I Used This:**
    **Report Section:** 4.2.1 Network Anomalies.
    **Specific Use:** Used the "Event ID 4625" details to define RDP attacks.
**Verification:**
    **How Verified:** Checked Microsoft Security documentation.
    **Accuracy:** Yes.

## Prompt 3

**Date:** 02/02/2026
**AI Tool:** Gemini pro
**Purpose:** To refine RDP detection and reduce false positives.
**The Prompt I Used:** "For Event ID 4625, which Logon Types should I filter for to specifically catch remote RDP or SMB attacks and avoid local service failures?"
**Response Summary:** Gemini recommended filtering for **Logon Type 10 (Remote Interactive)** and **Logon Type 3 (Network)** to isolate external threats.
**Quality Assessment:** Excellent.
**Why:** This added critical technical accuracy to the "RDP Brute Force" section, preventing alert fatigue.
**How I Used This:**
    **Report Section:** 4.2.1 Network Anomalies.
    **Specific Use:** Added the specific Logon Type filtering rule.
**Verification:**
    **How Verified:** Verified against Microsoft auditing categories.
    **Accuracy:** Yes.

## Prompt 4

**Date:** 03/02/2026
**AI Tool:** Gemini pro
**Purpose:** To understand "Impossible Travel" as an indicator.
**The Prompt I Used:** "What is 'Impossible Travel' in the context of identity security and ransomware initial access?"
**Response Summary:** Gemini defined it as a user account authenticating from two geographically distant locations within a timeframe that is physically impossible (e.g., NY to Moscow in 15 mins).
**Quality Assessment:** Good.
**Why:** Provided a clear definition for a high-fidelity indicator.
**How I Used This:**
    **Report Section:** 4.2.1 Network Anomalies.
    **Specific Use:** Added "Impossible Travel" as a key identity anomaly.
**Verification:**
    **How Verified:** N/A (Standard security concept).
    **Accuracy:** Yes.

## Prompt 5

**Date:** 03/02/2026
**AI Tool:** Gemini pro
**Purpose:** To find specific command-line indicators for the behavioral table.
**The Prompt I Used:** "Provide the exact command line arguments attackers use to delete shadow copies using vssadmin, and the PowerShell command to disable Windows Defender."
**Response Summary:** Provided vssadmin.exe delete shadows /all /quiet and Set-MpPreference -DisableRealtimeMonitoring $true.
**Quality Assessment:** Excellent.
**Why:** I needed the exact syntax to make the "Suspicious Behavior" table credible.
**How I Used This:**
    **Report Section:** 4.3 Behavioral Indicators.
    **Specific Use:** Copied commands directly into the "Technical Command / Artifact" column.
**Verification:**
    **How Verified:** Verified command syntax in a virtual machine.
    **Accuracy:** Yes.

## Prompt 6

**Date:** 04/02/2026
**AI Tool:** Gemini pro
**Purpose:** To compare free detection tools for the stack.
**The Prompt I Used:** "Compare Sysmon vs Zeek for ransomware detection. Which one is better for endpoint visibility and which for network? Can they be used together?"
**Response Summary:** Clarified that Sysmon is for endpoint (process creation, arguments) while Zeek is for network traffic (lateral movement). Confirmed they are complementary.
**Quality Assessment:** Excellent.
**Why:** Helped me distinguish between endpoint and network visibility tools.
**How I Used This:**
    **Report Section:** 4.5 Detection Tooling Stack.
    **Specific Use:** Wrote sections 4.5.1 (Sysmon) and 4.5.2 (Zeek).
**Verification:**
    **How Verified:** Checked official tool documentation.
    **Accuracy:** Yes.

## Prompt 7

**Date:** 05/02/2026
**AI Tool:** Gemini pro
**Purpose:** To generate the Sysmon configuration XML.
**The Prompt I Used:** "Write a Sysmon XML configuration block to detect 'vssadmin delete shadows' and 'Set-MpPreference' commands."
**Response Summary:** Generated the valid XML code block used in Appendix A, specifically targeting the commands I identified earlier.
**Quality Assessment:** Good.
**Why:** Provided the practical code snippet added to the report appendix.
**How I Used This:**
    **Report Section:** Appendix A: Practical Implementation.
    **Specific Use:** Copied the XML code block for the "Practical Lab" section.
**Verification:**
    **How Verified:** Reviewed XML structure against Sysmon schema.
    **Accuracy:** Yes.

## Prompt 8

**Date:** 05/02/2026
**AI Tool:** Gemini pro
**Purpose:** To explain File Integrity Monitoring (FIM).
**The Prompt I Used:** "What is File Integrity Monitoring (FIM) and how does it detect ransomware encryption? Suggest open-source tools."
**Response Summary:** Defined FIM as monitoring checksums of files. Suggested OSSEC/Wazuh. Explained that rapid modification of many files is the trigger.
**Quality Assessment:** Good.
**Why:** Connected the concept of "Rapid File Modifications" to a specific tool category.
**How I Used This:**
    **Report Section:** 4.5.4 File Integrity Monitoring.
    **Specific Use:** Added OSSEC/Wazuh as the recommended tools.
**Verification:**
    **How Verified:** Checked Wazuh features list.
    **Accuracy:** Yes.

## Prompt 9

**Date:** 06/02/2026
**AI Tool:** Gemini pro
**Purpose:** To research User and Entity Behavior Analytics (UEBA).
**The Prompt I Used:** "Explain User and Entity Behavior Analytics (UEBA) in the context of ransomware. How does it detect 'living off the land' attacks?"
**Response Summary:** Described UEBA as creating a "baseline" of normal activity. It detects intent (e.g., unusual data volume transfer) even if the user credentials are valid.
**Quality Assessment:** Excellent.
**Why:** Provided the logic for the "Future-Proofing" section.
**How I Used This:**
    **Report Section:** 4.6 Future-Proofing: AI & UEBA.
    **Specific Use:** Wrote the explanation of "AI-Driven Anomaly Detection".
**Verification:**
    **How Verified:** Cross-referenced with industry standard definitions.
    **Accuracy:** Yes.

## Prompt 10

**Date:** 07/02/2026
**AI Tool:** Gemini pro
**Purpose:** To detail Data Exfiltration signs.
**The Prompt I Used:** "What are the network signs of data exfiltration in a double extortion ransomware attack? What times are most suspicious?"
**Response Summary:** Highlighted "Unusual Outbound Traffic" spikes, specifically during off-hours (2 AM - 4 AM) or weekends. Mentioned use of tools like Rclone.
**Quality Assessment:** Good.
**Why:** Provided specific details on timing (off-hours) to make the detection rule more realistic.
**How I Used This:**
    **Report Section:** 4.2.1 Network Anomalies.
    **Specific Use:** Added the "Unusual Outbound Traffic" bullet point.
**Verification:**
    **How Verified:** N/A.
    **Accuracy:** Yes.

## Prompt 11

**Date:** 06/02/2026
**AI Tool:** Gemini
**Purpose:** To solve the "False Positive" issue with backup software (Section 4.6.1).
**The Prompt I Used:** "How do I reduce false positives for vssadmin delete shadows alerts caused by legitimate backup solutions like Veeam? Explain the logic for whitelisting by parent process."
**Response Summary:** Gemini advised creating a suppression rule that checks if the **Parent Image** is a known backup executable (e.g., veeam\_agent.exe) AND if the **User** is a specific Service Account. It warned to alert immediately if the parent is cmd.exe.
**Rating:** **Excellent**
**Why:** This provided the specific logic for the "Filtering Operational Noise" section, moving beyond simple detection to actual tuning.
**How I Used This:**
    **Report Section:** 4.6.1 Filtering Operational Noise.
    **Specific Use:** Wrote the strategy for "Whitelisting by Parent Process".
**Verification:**
    **How Verified:** Checked SIEM logic documentation.
    **Accuracy:** Yes.

## Prompt 12

**Date:** 07/02/2026
**AI Tool:** Gemini
**Purpose:** To understand how to detect C2 despite encryption (Section 4.6.2).
**The Prompt I Used:** "Can Zeek detect C2 traffic if it uses HTTPS? Explain how JA3 fingerprinting and beaconing jitter analysis work for this."
**Response Summary:** Gemini explained that **JA3** fingerprints the SSL client application (identifying non-standard tools) and **Jitter** analysis detects the mechanical timing (0% variance) of C2 beacons, neither of which requires decrypting the payload.
**Rating:** **Excellent**
**Why:** It debunked the myth that HTTPS hides everything and gave me two specific technical methods (JA3 and Jitter) to defend the use of Zeek.
**How I Used This:**
    **Report Section:** 4.6.2 Analyzing Encrypted Traffic.
    **Specific Use:** Drafted the "JA3 Fingerprinting" and "Beaconing Jitter" explanations.
**Verification:**
    **How Verified:** N/A (Standard Network Security concept).
    **Accuracy:** Yes.

### My Best Prompts:

**Most Effective:** Prompt #7 - Sysmon Configuration
    **Why it worked well:** Instead of asking for a general explanation of how to detect threats, I asked for the **exact XML configuration block** targeting specific commands (vssadmin, Set-MpPreference). This provided an immediately usable, practical artifact for the "Appendix" section of my report, moving beyond theory to implementation.
**Most Improved:** Prompt #3 - RDP Logon Types
    **How it evolved:** My initial research (Prompt #2) into RDP attacks gave me the generic Event ID 4625, which generates too many false positives. I refined Prompt #3 to specifically ask for **"Logon Types"** (Type 10 and Type 3) to filter out local noise. This evolution from a broad query to a constraint-based query resulted in a much higher-fidelity detection rule for the report.

### 

### 

### 

### 

### Lessons Learned:

**What Worked:**

**Requesting Specific "Artifacts":** Asking Gemini for concrete details like **Event IDs** (4625), **Command Line arguments** (-DisableRealtimeMonitoring), and **Logon Types** produced far better technical content than asking for general concepts.
**Comparative Prompts:** Asking Gemini to "Compare Sysmon vs Zeek" (Prompt #5) was more effective than asking about them individually. It forced the AI to articulate the _differences_ (Endpoint vs. Network), which directly helped me structure the "Detection Tooling Stack" section of the report.

**What Didn't Work:**

**Broad "Discovery" Questions:** Initial broad queries like "What are network anomalies?" (Prompt #2) returned lists that were correct but too generic. I learned I had to specify the _phase_ of the attack (e.g., "Left of Boom" or "Staging phase") to get indicators that are actually useful for early detection.
**Ignoring False Positives:** Early prompts didn't ask how to _filter_ data. I learned that asking "How do I detect X?" is less useful than "How do I detect X _and avoid false positives_?" (as seen in the RDP example). Without this constraint, the AI provides detection logic that is often too noisy for a real SOC environment.
