## Personal Information

**Name:** Chandra Shekhar Kumawat  
**Team:** 404 Not Found  
**Role:** Threat Researcher  
**Total Prompts:** 10  

---

## Summary Statistics
```
| Tool        | Count | Excellent | Good | Needed Work |
|-------------|-------|-----------|------|-------------|
| ChatGPT     | 2     | 2         | 0    | 0           |
| Perplexity  | 2     | 2         | 0    | 0           |
| Gemini      | 2     | 1         | 1    | 0           |
| Mistral     | 1     | 1         | 0    | 0           |
| Claude      | 1     | 0         | 1    | 0           |
| Copilot     | 1     | 1         | 0    | 0           |
| DeepSeek    | 1     | 1         | 0    | 0           |
```
---

## Prompt 1

**Date:** 05/02/2026  
**AI Tool:** Mistral  

**Purpose:**  
To research the attack lifecycle of LockBit RaaS and map it to MITRE ATT&CK techniques for report technical depth.

**Prompt Used:**  
You are required to perform the role of a senior-level Threat Research Analyst. The purpose of this answer is to describe an overall model of LockBit 3.0 ransomware as a service attack lifecycle from initial access through to encryption and extortion. The goal is to connect each of these phases with MITRE ATT&CK's technique IDs. Here, various tools such as PsExec, Rclone, Mimikatz, and vssadmin will be discussed. Moreover, this answer will focus on 2023–2025 attack years and include various citations such as CISA, FBI, Microsoft, Mandiant with URLs.

**Response Summary:**  
LockBit 3.0 RaaS Attack Lifecycle (2023–2025): The attack begins with initial access via exploits (e.g., CVE-2023-4966) or brute-force RDP (T1190, T1133), followed by execution and persistence using PowerShell and Cobalt Strike (T1059, T1053). Privilege escalation leverages Mimikatz and GPO (T1068, T1003), while lateral movement uses PsExec/SMB (T1021, T1072). Data is exfiltrated via Rclone/StealBit (T1048, T1567), and encryption/extortion involves vssadmin and double extortion (T1486, T1490).

**Key Tools:** PsExec, Rclone, Mimikatz, vssadmin  
**Sources:** CISA, ACSC, Dark Web Report

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Output of Mistral is technically correct, along with validation sources and vulnerability IDs that allow direct search and verification.

**How I Used This:**  
**Report Section:** Attack Lifecycle (Technical Table)  
**Specific Use:** Used the lifecycle table as the base for my MITRE ATT&CK mapping section and expanded it with verified dwell-time statistics.

**Verification:**  
**How Verified:** Verified MITRE technique IDs using the official MITRE ATT&CK website and verified LockBit tooling and behavior using CISA/FBI advisories and Microsoft threat reports.  
**Accuracy:** Yes

---

## Prompt 2

**Date:** 06/02/2026  
**AI Tool:** Perplexity  

**Purpose:**  
To get real-world RaaS case studies (2023–2025) with confirmed details, timelines, and sources.

**Prompt Used:**  
You are required to perform the role of a senior-level Threat Intelligence Analyst. Your task is to provide five real-world Ransomware-as-a-Service (RaaS) case studies from 2023–2025, including ransomware group, target organization, initial access vector, attack steps, MITRE ATT&CK techniques, impact, and public sources with URLs.

**Response Summary:**  
LockBit, ALPHV/BlackCat, Cl0p, Black Basta, and others dominated the RaaS landscape from 2023 to 2025 with high-profile attacks on critical sectors.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Real victim names, verified sources, and direct URLs made it highly usable for academic writing.

**How I Used This:**  
**Report Section:** Real-World Case Studies (2023–2025)  
**Specific Use:** Converted case studies into a timeline-based narrative and used citations directly.

**Verification:**  
**How Verified:** Cross-verified each case using CISA advisories and Microsoft threat reports.  
**Accuracy:** Yes

---

## Prompt 3

**Date:** 06/02/2026  
**AI Tool:** ChatGPT  

**Purpose:**  
To generate a full technical narrative of a RaaS incident similar to a real incident response report.

**Prompt Used:**  
You are acting as a DFIR Incident Response Lead. Create a realistic technical incident report based on a Ransomware-as-a-Service attack (2024–2025), including timeline, execution, persistence, privilege escalation, MITRE ATT&CK IDs, and trusted URLs.

**Response Summary:**  
On 2025-11-19, the organization experienced a human-operated ransomware intrusion consistent with modern RaaS affiliate behavior, involving VPN access, LSASS credential dumping, SMB/RDP lateral movement, GPO-based deployment, and data exfiltration before encryption.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** DFIR-style output that was realistic and professionally written.

**How I Used This:**  
**Report Section:** Incident Walkthrough (Technical)  
**Specific Use:** Used the timeline and added screenshots and log references.

**Verification:**  
**How Verified:** Verified MITRE IDs and tooling references using Microsoft Security Blog and CISA.  
**Accuracy:** Yes

---

## Prompt 4

**Date:** 06/02/2026  
**AI Tool:** Gemini  

**Purpose:**  
To understand post-access behavior of human-operated RaaS attacks.

**Response Summary:**  
Highlighted reduced dwell time, heavy use of Living off the Land binaries, and structured attack flows from access to impact.

**Quality Assessment:**  
**Rating:** Good  

**How I Used This:**  
**Report Section:** Human-Operated RaaS Behavior  
**Specific Use:** Converted attacker actions into an attack flow model.

**Verification:**  
**How Verified:** Checked dwell-time statistics using CrowdStrike Global Threat Report 2025.  
**Accuracy:** Yes

---

## Prompt 5

**Date:** 06/02/2026  
**AI Tool:** Copilot  

**Purpose:**  
To identify common initial access vectors and exploited CVEs used by RaaS affiliates.

**Quality Assessment:**  
**Rating:** Excellent  

**How I Used This:**  
**Report Section:** Initial Access Methods (2023–2025)  
**Specific Use:** Built a table mapping access vector → CVE → MITRE → real-world example.

**Verification:**  
**How Verified:** Verified CVEs via CISA KEV and MITRE ATT&CK database.  
**Accuracy:** Yes

---

## Prompt 6

**Date:** 06/02/2026  
**AI Tool:** Claude  

**Purpose:**  
To research modern persistence techniques used by RaaS affiliates.

**Quality Assessment:**  
**Rating:** Good  

**How I Used This:**  
**Report Section:** Persistence and Defense Evasion  
**Specific Use:** Converted content into a structured persistence table.

**Verification:**  
**How Verified:** Verified MITRE IDs and tools using Microsoft and Sophos reports.  
**Accuracy:** Yes

---

## Prompt 7

**Date:** 06/02/2026  
**AI Tool:** DeepSeek  

**Purpose:**  
To generate privilege escalation and credential access techniques with MITRE mapping.

**Quality Assessment:**  
**Rating:** Excellent  

**How I Used This:**  
**Report Section:** Privilege Escalation & Credential Theft  
**Specific Use:** Created a step-by-step attacker flow diagram.

**Verification:**  
**How Verified:** Verified techniques via MITRE ATT&CK and Mandiant playbooks.  
**Accuracy:** Yes

---

## Prompt 8

**Date:** 06/02/2026  
**AI Tool:** Perplexity  

**Purpose:**  
To research data exfiltration and double extortion techniques.

**Quality Assessment:**  
**Rating:** Excellent  

**How I Used This:**  
**Report Section:** Data Exfiltration & Double Extortion  
**Specific Use:** Built the Exfiltration Toolkit subsection.

**Verification:**  
**How Verified:** Verified tooling using CISA and Microsoft intelligence reports.  
**Accuracy:** Yes

---

## Prompt 9

**Date:** 06/02/2026  
**AI Tool:** ChatGPT  

**Purpose:**  
To generate detection and threat-hunting guidance for RaaS attacks.

**Quality Assessment:**  
**Rating:** Excellent  

**How I Used This:**  
**Report Section:** Detection Methods & Threat Hunting  
**Specific Use:** Created a Blue Team Playbook with sample SIEM queries.

**Verification:**  
**How Verified:** Verified detections via MITRE ATT&CK and Microsoft Defender docs.  
**Accuracy:** Yes

---

## Prompt 10

**Date:** 07/02/2026  
**AI Tool:** Gemini  

**Purpose:**  
To research ransomware deployment and encryption execution patterns.

**Quality Assessment:**  
**Rating:** Excellent  

**How I Used This:**  
**Report Section:** Ransomware Execution & Impact Stage  
**Specific Use:** Built the Final Deployment & Encryption Phase section.

**Verification:**  
**How Verified:** Verified ESXi behavior via Sophos reports and MITRE ATT&CK database.  
**Accuracy:** Yes

---

## My Best Prompts

**Most Effective:** Prompt 2 – Real-World RaaS Case Studies  
**Most Improved:** Prompt 6 – Persistence Techniques

---

## Lessons Learned

**What Worked:**
- Clear analyst roles
- Structured prompts
- Asking for CVEs and MITRE IDs
- Using multiple AI tools
- Phase-based research approach

**What Didn’t Work:**
- Generic prompts
- Missing time ranges
- Unverified statistics
- Reliance on a single AI tool
