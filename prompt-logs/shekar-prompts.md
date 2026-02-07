## Personal Information

**Name:** Chandra Shekhar Kumawat  
**Team:** 404 Not Found  
**Role:** Threat Researcher  
**Total Prompts:** 10  

---

## Summary Statistics
```
| Tool       | Count | Excellent | Good | Needed Work |
|------------|-------|-----------|------|-------------|
| ChatGPT    | 2     | 2         | 0    | 0           |
| Perplexity | 2     | 2         | 0    | 0           |
| Gemini     | 2     | 1         | 1    | 0           |
| Mistral    | 1     | 1         | 0    | 0           |
| Claude     | 1     | 0         | 1    | 0           |
| Copilot    | 1     | 1         | 0    | 0           |
| DeepSeek   | 1     | 1         | 0    | 0           |
```
---

## Prompt 1

**Date:** 05/02/2026  
**AI Tool:** Mistral  

**Purpose:**  
To research the attack lifecycle of LockBit RaaS and map it to MITRE ATT&CK techniques for report technical depth.

**The Prompt I Used:**  
You are required to perform the role of a senior-level Threat Research Analyst. The purpose of this answer is to describe an overall model of LockBit 3.0 ransomware as a service attack lifecycle from initial access through to encryption and extortion. The goal is to connect each of these phases with MITRE ATT&CK's technique IDs. Here, various tools such as PsExec, Rclone, Mimikatz, and vssadmin will be discussed. Moreover, this answer will focus on 2023-2025 attack years and include various citations such as CISA, FBI, Microsoft, Mandiant) with URLs.

**Response Summary:**  
LockBit 3.0 RaaS Attack Lifecycle (2023–2025): The attack begins with initial access via exploits (e.g., CVE-2023-4966) or brute-force RDP (T1190, T1133), followed by execution/persistence using PowerShell and Cobalt Strike (T1059, T1053). Privilege escalation leverages Mimikatz and GPO (T1068, T1003), while lateral movement uses PsExec/SMB (T1021, T1072). Data is exfiltrated via Rclone/StealBit (T1048, T1567), and encryption/extortion involves vssadmin and double extortion (T1486, T1490).

**Key Tools:**  
PsExec, Rclone, Mimikatz, vssadmin.  

**Sources:**  
CISA, ACSC, Dark Web Report.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Output of Mistral is technically correct, Along with output we get validation source and Vulnerability ID which allow Direct search and Verify source so this is treated as Excellent.

**How I Used This:**  
**Report Section:** Attack Lifecycle (Technical Table)  
**Specific Use:** Used the lifecycle table as the base for my MITRE ATT&CK mapping section and expanded it with verified dwell-time statistics.

**Verification:**  
**How Verified:** Verified MITRE technique IDs using the official MITRE ATT&CK website and Verified LockBit tooling and behavior using CISA/FBI advisory and Microsoft threat reports.  
**Accuracy:** Yes

---

## Prompt 2

**Date:** 06/02/2026  
**AI Tool:** Perplexity  

**Purpose:**  
To get real-world RaaS case studies (2023–2025) with confirmed details, how and when, and sources for report.

**The Prompt I Used:**  
You are required to perform the role of a senior-level Threat Intelligence Analyst. Your task is to provide 5 real-world Ransomware-as-a-Service (RaaS) case studies from 2023–2025. Each case study must include: Ransomware group name (example: LockBit, ALPHV, Cl0p, Black Basta), Target organization name and industry, 2. Initial access vector (VPN exploit, phishing, RDP brute force, etc.), 3. Key attack steps (privilege escalation, etc), 4. MITRE ATT&CK technique used for major steps, 5. Impact (downtime, data leak, etc.), 6. Public sources with URLs (CISA, FBI, trusted news etc)

**Response Summary:**  
LockBit, ALPHV/BlackCat, Cl0p, Black Basta, and others dominated the RaaS landscape from 2023 to 2025 with high-profile attacks on critical sectors. Below are five detailed case studies drawn from verified threat intelligence.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** We get Real victim names, verified sources, direct URLs made it highly usable for academic writing.

**How I Used This:**  
**Report Section:** Real-World Case Studies (2023–2025)  
**Specific Use:** Converted case studies into a timeline-based narrative and used citations directly.

**Verification:**  
**How Verified:** Cross-verified each case using official CISA advisory and Microsoft threat reports and also check that given URL are actual or working.  
**Accuracy:** Yes

---

## Prompt 3

**Date:** 06/02/2026  
**AI Tool:** ChatGPT  

**Purpose:**  
To generate a full technical narrative of a RaaS incident showing attacker behaviour like a real incident response report.

**The Prompt I Used:**  
You are acting as a DFIR Incident Response Lead. Create a realistic technical incident report based on a Ransomware-as-a-Service attack (2024–2025) similar to LockBit or Black Basta. The report should have Timeline, Execution & Persistence methods, Privilege escalation tools (Mimikatz, LSASS dumping, token theft), MITRE ATT&CK technique IDs, URLs from CISA, FBI, Microsoft, etc. The response look like a professional IR report.

**Response Summary:**  
On 2025-11-19, the organization experienced a human-operated ransomware intrusion consistent with modern RaaS affiliate behavior (similar to LockBit and Black Basta). The attacker gained access using valid VPN credentials, escalated privileges using credential dumping (LSASS), moved laterally via SMB and RDP, and deployed ransomware payloads using Group Policy and PsExec-style remote execution. The threat actor conducted data exfiltration prior to encryption and left a ransom note demanding cryptocurrency payment. The actor also attempted to encrypt VMware ESXi workloads.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Very good DFIR-style output and professionally written.

**How I Used This:**  
**Report Section:** Incident Walkthrough (Technical)  
**Specific Use:** Used the timeline and added screenshots/log references.

**Verification:**  
**How Verified:** Verified MITRE IDs and confirmed tooling references from Microsoft Security Blog and CISA.  
**Accuracy:** Yes

---

## Prompt 4

**Date:** 06/02/2026  
**AI Tool:** Gemini  

**Purpose:**  
To understand how human organized RaaS attacks behave inside a network after getting access.

**The Prompt I Used:**  
Explain how ransomware as a service (RaaS) works after initial access (2023–2025). That Includes how they choose targets, do internal recon (discovery, BloodHound, net commands), detection, move laterally (PsExec, RDP, WMI, SMB), and decide when to deploy ransomware. Also include time trends, MITRE ATT&CK IDs, and sources with URLs (Microsoft, Sophos, CISA).

**Response Summary:**  
Recent reports from Microsoft, Sophos, CISA, and other threat intelligence firms highlight a significant shift in Ransomware-as-a-Service (RaaS) operations between 2023 and 2025. The current landscape is defined by decreased dwell time (the time from compromise to encryption) and a heavy reliance on "Living off the Land" (LotL) binaries to evade modern EDR (Endpoint Detection and Response) systems.

**Quality Assessment:**  
**Rating:** Good  

**How Used:**  
Used for “attacker mindset” and human-operated ransomware behavior section.

**How I Used This:**  
**Report Section:** Human-Operated RaaS Behavior (Attacker Mindset)  
**Specific Use:** Converted the described attacker steps into an attack flow for the report (Initial Access → Recon → Credential Access → Lateral Movement → Impact).

**Verification:**  
**How Verified:** Checked dwell time stats using CrowdStrike Global Threat Report 2025.  
**Accuracy:** Yes

---

## Prompt 5

**Date:** 06/02/2026  
**AI Tool:** Copilot  

**Purpose:**  
To identify the common initial access used by modern RaaS affiliates and map them with real exploited vulnerabilities and MITRE ATT&CK techniques.

**The Prompt I Used:**  
You are required to perform the role of a senior-level Threat Intelligence Analyst and your task is to analyze the common initial access techniques used by RaaS affiliates during 2023–2025. Your answer must include: 1. Top 5 initial access, 2. Real-world exploited CVEs 3. How attackers operationalize these vectors, 4. MITRE ATT&CK techniques for each access method, 5. Real-world examples where these access vectors were used, 6. Trusted sources with URLs from CISA KEV catalog, Microsoft, Mandiant, CrowdStrike, FBI.

**Response Summary:**  
Copilot identified that RaaS affiliates heavily rely on exploiting edge devices (Citrix NetScaler, Ivanti VPN, Fortinet, SonicWall), abusing exposed RDP, and leveraging stolen credentials purchased from IABs (Initial Access Brokers). The response included CVE references such as CVE-2023-4966 (Citrix Bleed) and CVE-2024-1709 (ConnectWise ScreenConnect), mapping them to MITRE techniques like External Remote Services (T1133) and Exploit Public-Facing Application (T1190). It also highlighted the trend that credential-based access has increased due to infostealer malware.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Output provided CVEs, exact access vectors, and direct mapping to MITRE IDs which makes it very easy to verify using CISA KEV and threat reports.

**How I Used This:**  
**Report Section:** Initial Access Methods (2023–2025)  
**Specific Use:** Used the Top 5 initial access vectors list to create a table showing Vector → CVE → MITRE Technique → Real Case Example.

**Verification:**  
**How Verified:** Verified CVE in the official CISA KEV and validated MITRE IDs from MITRE ATT&CK official database. Cross-checked access patterns using Microsoft Security Intelligence blogs.  
**Accuracy:** Yes

---

## Prompt 6

**Date:** 06/02/2026  
**AI Tool:** Claude  

**Purpose:**  
To research modern RaaS persistence techniques used after initial compromise and map them with MITRE ATT&CK and real tooling examples.

**The Prompt I Used:**  
You are required to behave like a senior-level DFIR analyst. Your task is to explain the most common persistence mechanisms used by RaaS affiliates in 2023–2025 attacks. Your response includes: Common methods (Scheduled Tasks, Registry Run Keys, Services etc), Tools used (PowerShell, AnyDesk, RMM tools), MITRE ATT&CK techniques for each method, and How defenders detect each method using logs / EDR, in last Sources with URLs from Microsoft, CISA, Sophos etc.

**Response Summary:**  
Claude explained that modern RaaS affiliates often maintain persistence using scheduled tasks, registry modifications, service creation, and legitimate remote management tools like AnyDesk, Atera, ScreenConnect, and TeamViewer. It mapped persistence behavior to MITRE techniques such as Scheduled Task/Job (T1053), Registry Run Keys/Startup Folder (T1547), Create or Modify System Process (T1543), and WMI Event Subscription (T1546.003). It also emphasized that attackers prefer stealthy persistence through legitimate admin tooling to avoid triggering EDR alerts.

**Quality Assessment:**  
**Rating:** Good  
**Why:** Strong mapping of methods with MITRE technique IDs and realistic tools used by ransomware affiliates, but required manual validation of some sources.

**How I Used This:**  
**Report Section:** Persistence and Defense Evasion  
**Specific Use:** Converted persistence techniques into a structured table: “Technique → Tool Used → Detection Method → MITRE ID”.

**Verification:**  
**How Verified:** Verified MITRE technique IDs on official MITRE ATT&CK and validated persistence tooling references from Microsoft incident response blogs and Sophos ransomware reports.  
**Accuracy:** Yes

---

## Prompt 7

**Date:** 06/02/2026  
**AI Tool:** DeepSeek  

**Purpose:**  
To generate detailed privilege escalation and credential access methods used in RaaS intrusions with tools and MITRE mapping.

**The Prompt I Used:**  
You are required to act as a senior threat hunting analyst. Your task is to explain how Ransomware-as-a-Service affiliates perform privilege escalation and credential access after initial compromise. Your response includes: Common privilege escalation methods, Credential dumping methods, Tools used, MITRE ATT&CK technique IDs for each method, Defensive detections and Windows event logs, and Trusted sources with URLs from Microsoft, CISA, FBI, Mandiant.

**Response Summary:**  
The most modern RaaS affiliates escalate privileges by stealing tokens, abusing UAC bypass techniques, and dumping credentials from LSASS memory. It included credential theft approaches such as comsvcs.dll MiniDump, Procdump execution, and Impacket secretsdump.py for extracting NTDS.dit. The response mapped activities to MITRE techniques such as OS Credential Dumping (T1003), LSASS Memory (T1003.001), Credential Access via SAM (T1003.002), and Token Impersonation/Theft (T1134). It also highlighted that ransomware affiliates often attempt domain admin compromise before deploying ransomware via GPO.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Output contained exact tools, correct technical steps, and strong MITRE mapping. Very useful for a DFIR-level report.

**How I Used This:**  
**Report Section:** Privilege Escalation & Credential Theft  
**Specific Use:** Used the explanation to create a step-by-step attacker flow chart: “Dump creds → Escalate privileges → Gain Domain Admin → Lateral spread”.

**Verification:**  
**How Verified:** Verified technique IDs from MITRE ATT&CK official database and confirmed tool usage through Microsoft incident response guidance and Mandiant ransomware playbooks.  
**Accuracy:** Yes

---

## Prompt 8

**Date:** 06/02/2026  
**AI Tool:** Perplexity  

**Purpose:**  
To research data ex-filtration methods used by RaaS affiliates (double extortion) and document tools, protocols, and MITRE mapping.

**The Prompt I Used:**  
You are required to act as a senior-level Threat Intelligence Analyst. Your task is to explain how Ransomware-as-a-Service (RaaS) affiliates perform data exfiltration and double extortion operations during 2023–2025. Your answer must include: Common exfiltration tools, Protocols used, MITRE ATT&CK technique IDs for exfiltration, How attackers prepare data before exfiltration (compression, encryption), Real-world case examples and Trusted sources with URLs from CISA, Microsoft, Mandiant, FBI, Sophos.

**Response Summary:**  
Perplexity explained that double extortion is now the dominant ransomware model, where attackers steal sensitive data before encryption and threaten public leaks. It highlighted common tools such as Rclone, WinSCP, Mega, and StealBit (LockBit’s exfiltration tool). The response mapped activity to MITRE techniques such as Exfiltration Over Web Service (T1567), Exfiltration Over C2 Channel (T1041), and Archive Collected Data (T1560). It also described that affiliates often compress data using 7zip or WinRAR before transfer and store it temporarily on staging servers.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Response contained strong case-study context, tools, protocols, and multiple URLs that could be directly verified.

**How I Used This:**  
**Report Section:** Data Exfiltration & Double Extortion  
**Specific Use:** Used the tool list and MITRE mapping to build an “Exfiltration Toolkit” subsection and included StealBit as a LockBit-specific highlight.

**Verification:**  
**How Verified:** Verified exfiltration tooling references using CISA ransomware advisories and Microsoft threat intelligence reports. Confirmed MITRE IDs from MITRE ATT&CK official database.  
**Accuracy:** Yes

---

## Prompt 9

**Date:** 06/02/2026  
**AI Tool:** ChatGPT  

**Purpose:**  
To generate detection and threat hunting guidance for RaaS attacks, including log sources, SIEM queries, and MITRE technique mapping.

**The Prompt I Used:**  
You are required to act as a senior Threat Hunting Analyst. Your task is to provide detection strategies for Ransomware-as-a-Service (RaaS) attacks from 2023–2025. Your answer must include: 1. Key indicators of compromise (IOCs) and attacker behavior, 2. Detection opportunities across Windows logs, Sysmon, firewall logs, EDR telemetry, and Active Directory logs, 3. Suggested threat hunting queries (Sigma/KQL-style examples), 4. Mapping detections to MITRE ATT&CK technique IDs, 5. Focus on detecting tools like PsExec, Rclone, Mimikatz, vssadmin, net commands, BloodHound, 6. Provide trusted sources with URLs from Microsoft Defender, CISA, Mandiant, CrowdStrike, and FBI.

**Response Summary:**  
We get a structured threat hunting guide focusing on early-stage detection such as unusual authentication attempts, new scheduled tasks, suspicious PowerShell usage, LSASS dumping attempts, and abnormal SMB/RDP lateral movement. It included example detection logic for Sysmon Event IDs, Windows Security logs, and Defender telemetry. The response mapped each detection category to MITRE techniques such as Command and Scripting Interpreter (T1059), Remote Services (T1021), OS Credential Dumping (T1003), and Inhibit System Recovery (T1490). It also included practical hunting tips like detecting vssadmin delete shadows and monitoring for abnormal Rclone user agents.

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Output was highly actionable with realistic hunting logic, MITRE mapping, and SIEM detection examples.

**How I Used This:**  
**Report Section:** Detection Methods & Threat Hunting  
**Specific Use:** Converted the detection methods into a “Blue Team Playbook” section and included sample KQL/Sigma queries in the appendix.

**Verification:**  
**How Verified:** Verified MITRE IDs using MITRE ATT&CK official website and validated detection ideas using Microsoft Defender documentation and CISA ransomware guidance.  
**Accuracy:** Yes

---

## Prompt 10

**Date:** 07/02/2026  
**AI Tool:** Gemini  

**Purpose:**  
To research ransomware deployment techniques and encryption execution patterns used by RaaS affiliates, including ESXi targeting, backup deletion, and mass deployment methods.

**The Prompt I Used:**  
You are required to act as a senior Incident Response and Threat Intelligence Analyst. Your task is to explain how Ransomware-as-a-Service (RaaS) affiliates deploy ransomware payloads at scale during 2023–2025 intrusions. Your answer must include: How attackers prepare the environment before encryption, Common deployment methods and VMware ESXi targeting trends and Linux ransomware execution methods, MITRE ATT&CK technique IDs for encryption stage, Tools and commands used and Sources with URLs from CISA, Microsoft, Sophos, Mandiant, and FBI.

**Response Summary:**  
Gemini Advanced explained that ransomware deployment is usually performed only after affiliates achieve domain-level control and confirm successful data exfiltration. It highlighted that attackers disable defenses using Group Policy changes, stop backup services, and delete shadow copies using vssadmin and wbadmin. The response described mass ransomware deployment via PsExec, GPO scheduled tasks, and remote execution using WMI/SMB. It also covered the 2024–2025 increase in ESXi targeting where attackers directly encrypt virtual machine files and backups. The activity was mapped to MITRE techniques such as Data Encrypted for Impact (T1486), Inhibit System Recovery (T1490), and Remote Services (T1021).

**Quality Assessment:**  
**Rating:** Excellent  
**Why:** Output was realistic, detailed, and included both Windows and ESXi ransomware deployment patterns with correct technical tooling.

**How I Used This:**  
**Report Section:** Ransomware Execution & Impact Stage  
**Specific Use:** Used this content to build the “Final Deployment & Encryption Phase” section and included a mini checklist of attacker preparation actions.

**Verification:**  
**How Verified:** Verified ESXi targeting behavior from Sophos ransomware reports and confirmed commands (vssadmin, wbadmin, bcdedit) in Microsoft incident response references. Verified MITRE IDs using MITRE ATT&CK official database.  
**Accuracy:** Yes

---

## My Best Prompts

**Most Effective:** Prompt #2 (Perplexity – Real-World RaaS Case Studies)  
It provided real victim names, clear attack vectors, MITRE mapping, and verified URLs (CISA/Microsoft/FBI). The citations were directly usable in the report and required minimal editing.

**Most Improved:** Prompt #6 (Claude – Persistence Techniques)  
The technical explanation was strong, but some sources needed manual validation. I learned to demand official references and include stricter citation requirements in the prompt.

---

## Lessons Learned

### What Worked

- Using clear roles (Threat Intelligence Analyst, DFIR Lead, Threat Hunter) produced expert-level responses.  
- Structured formats (tables, bullet points, timelines) made outputs report-ready.  
- Perplexity worked best for case studies and citations (Prompt #2, #8).  
- Asking for CVEs + MITRE IDs improved accuracy and verification (Prompt #5).  
- Splitting research into phases (access → persistence → escalation → exfiltration → detection → encryption) improved depth and clarity.

### What Didn’t Work

- Generic prompts gave broad and outdated results.  
- Missing time range (2023–2025) caused irrelevant older information.  
- Some statistics required verification and could not be trusted directly.  
- Relying on one AI tool reduced quality; using multiple tools improved results.
