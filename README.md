## Ransomware-as-a-Service **- Threat Intelligence Report**

Sprint 1 Project \| PG Certification in AI-Enabled Cybersecurity

IIT Roorkee x Futurense Technologies

---

## **Project Overview**

This repository contains a 2‑week Agile sprint project on **Ransomware-as-a-Service (RaaS)**.  
The main output is a threat intelligence report covering how RaaS works, real incidents, detection methods, and practical mitigation strategies for mid‑sized organizations.

---

## **Team Members**
```
  --------------------------------------------------------------------------
    Name            Role          GitHub             Contributions
  --------------- ------------- ------------------ -------------------------
  Vansh, Jay      Scrum Master  \@vaanshu,         Facilitation,
  Goyal                         \@JG10-WEB         documentation

  Jay Goyal,      Threat        \@JG10-WEB,        Attack research, case
  Chandra Shekar  Researcher    \@cskumawat-ui     studies

  N Ashwin Kumar  Defense       \@nashwinkumar96   Detection, mitigation
                  Analyst                          

  Abdiel B        GitHub Lead   \@Brian-Mendonca   Repository, diagrams
  Mendonca                                         
  --------------------------------------------------------------------------
```

---

## Key Findings

1. **RaaS is a mature cybercrime ecosystem, not just malware.**  
   The model separates roles between operators, affiliates, initial access brokers, negotiators, and money launderers, making ransomware scalable, repeatable, and profitable across sectors like healthcare, government, manufacturing, and critical infrastructure.

2. **Modern RaaS relies heavily on “double extortion” and human‑operated attacks.**  
   Affiliates use a full attack lifecycle—initial access via exposed services or stolen credentials, internal reconnaissance, privilege escalation, lateral movement, data exfiltration, and finally mass encryption plus leak‑site extortion.

3. **Detection must focus on behavior rather than signatures.**  
   Effective defense comes from monitoring anomalies such as suspicious use of PowerShell, vssadmin, PsExec, RDP brute forcing, impossible‑travel logins, unusual outbound data volume, and rapid file modification patterns, instead of relying only on static AV signatures.

4. **Resilience depends on immutable backups, strong identity security, and EDR.**  
   Controls like 3‑2‑1‑1 immutable backups, enforced MFA on all remote and admin paths, network segmentation, SIEM logging, and EDR with behavioral analytics significantly reduce impact, even when initial compromise occurs.

5. **AI is a powerful accelerator but requires careful verification.**  
   AI tools greatly sped up research, structuring, and drafting, but all outputs had to be cross‑checked against authoritative sources (CISA, Microsoft, DOJ, vendor reports) to avoid hallucinations and outdated information.

---

## CIA Triad Impact

| Component       | Impact | Summary                                                                                          |
|-----------------|--------|--------------------------------------------------------------------------------------------------|
| Confidentiality | HIGH   | Sensitive data is routinely exfiltrated before encryption, enabling doxxing, fraud, and resale.  |
| Integrity       | MEDIUM | Encryption and possible tampering make data untrusted even after decryption or restore.          |
| Availability    | HIGH   | Core systems and backups are encrypted, causing multi‑day outages and service disruption.        |

---

## **Repository Structure**

```
404-Not-Found-threat-analysis/
├── README.md
├── prompt-logs/
│   ├── abdiel-prompts.md
│   ├── ashwin-prompts.md
│   ├── jay-prompts.md
│   ├── shekar-prompts.md
│   └── vansh-prompts.md
├── report/
│   └── threat-report.pdf
└── sprint-docs/
    ├── backlog.md
    ├── meeting-notes.md
    └── retrospective.md
```

## AI Tools Used
```
| Tool        | Purpose                                      |
|------------|----------------------------------------------|
| ChatGPT    | Drafting, explanations, IR-style narratives  |
| Perplexity | Case studies, citations, source-backed intel |
| Gemini     | Technical details, detection logic, events   |
| Gemini Pro | Deep detection content, log/command details  |
| Mistral    | Attack lifecycle & MITRE ATT&CK mapping      |
| Claude     | DFIR-style narratives, AD/PAM depth          |
| Copilot    | CVE and initial access research              |
| DeepSeek   | Privilege escalation & credential theft flow |
```
---

## **Sprint Timeline**
```
  ------------------------------------------------------------------------
    Phase           Days            Activities
  --------------- --------------- ----------------------------------------
  Planning        Day 1           Roles, topic, backlog

  Research        Days 2-6        RaaS research & notes

  Mid-Review      Day 7           Feedback & adjustments

  Writing         Days 8-12       Report deafting

  Final           Days 13-14      Polish, export, Git push
  ------------------------------------------------------------------------
```
