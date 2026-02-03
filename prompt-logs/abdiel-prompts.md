## **Personal Information**

**Name:** Abdiel Brian Mendonca

**Team:** 404 Not Found

**Role:** GitHub Lead / Defense Analyst (Mitigation Strategies)

**Total Prompts:** 12

***

## **Summary Statistics**
```
|  **Tool**  | **Count** | **Excellent** | **Good** | **Needed Work** |
|------------|-----------|---------------|----------|-----------------|
| ChatGPT    | 4         | 2             | 2        | 0               |
| Perplexity | 3         | 3             | 0        | 0               |
| Gemini     | 3         | 2             | 1        | 0               |
| Claude     | 2         | 1             | 0        | 1               |
```
***

## **Prompt 1**

**Date:** 30/01/2026

**AI Tool:** Perplexity

**Purpose:** Understand the most effective technical controls against RaaS attacks based on recent 2024-2025 incidents

**The Prompt I Used:**

*"You are a senior cybersecurity defense analyst. Based on RaaS attacks from 2024-2025 (LockBit, ALPHV/BlackCat), what are the top 5 technical controls that have proven most effective at preventing or limiting damage? For each control, provide: (1) How it works, (2) Cost estimate for mid-sized organizations (500 employees), (3) A real example where it stopped an attack. Use bullet points and cite sources."*

**Response Summary:**

Perplexity provided a prioritized list including immutable backups, MFA on remote access, EDR deployment, network segmentation, and application whitelisting. Each control included cost ranges ($500-15,000/month depending on the control) and cited the 2024 IBM Cost of Data Breach Report and specific LockBit/BlackCat incident analyses. It included a case study of a healthcare provider that recovered in 36 hours using immutable AWS backups.

**Quality Assessment:**

**Rating:** Excellent

**Why:** Response was highly specific with current data (2024-2025), included cost estimates crucial for my section, and provided real-world validation through case studies. Citations allowed me to verify claims with primary sources.

**How I Used This:**

**Report Section:** Section 5.2 (Immediate Actions) and 5.3 (Short-Term Controls)

**Specific Use:** Used the immutable backup case study verbatim (verified independently), cost estimates formed the basis for my budget tables, and the prioritization logic informed my 0-30 day vs 1-3 month timeline structure.

**Verification:**

**How Verified:** Cross-checked the healthcare case study with IBM Security's 2024 Threat Intelligence Index and AWS case studies database. Verified cost estimates with vendor pricing pages (Veeam, AWS S3 Object Lock).

**Accuracy:** Yes - all facts verified accurately, costs matched vendor pricing within 10% margin.

***

## **Prompt 2**

**Date:** 30/01/2026

**AI Tool:** ChatGPT

**Purpose:** Get detailed technical implementation steps for immutable backup strategy

**The Prompt I Used:**

*"Act as a backup and recovery specialist. Explain how to implement the 3-2-1-1 backup rule specifically to defend against ransomware that targets backup deletion (like LockBit). Include: (1) Step-by-step technical implementation for AWS S3 Object Lock, (2) PowerShell commands if applicable, (3) How to test recovery, (4) RTO and RPO targets for mid-sized organizations. Format as a numbered implementation guide."*

**Response Summary:**

ChatGPT provided a comprehensive 8-step implementation guide covering AWS S3 bucket creation, enabling Object Lock with retention periods, configuring lifecycle policies, setting up cross-region replication, and creating automated recovery test scripts. It included PowerShell commands for testing restores and recommended RTO of 24-48 hours and RPO of ≤4 hours for critical systems.

**Quality Assessment:**

**Rating:** Good

**Why:** Very detailed technical steps that were directly usable. However, it initially suggested SMB protocol for backup transfers which is risky (affiliates abuse SMB). I had to refine the prompt to get cloud-native transfer methods.

**How I Used This:**

**Report Section:** Section 5.2.1 (Implement Immutable Backups)

**Specific Use:** Adapted the step-by-step guide into prose format for the report, used the RTO/RPO targets in my recommendations, and incorporated the testing methodology into the "Test Recovery Weekly" subsection.

**Verification:**

**How Verified:** Tested the AWS S3 Object Lock configuration steps in a personal AWS free-tier account. Verified the PowerShell recovery commands executed without errors.

**Accuracy:** Partially - Core steps accurate, but needed refinement on transfer protocols for security best practices.

***

## **Prompt 3**

**Date:** 31/01/2026

**AI Tool:** Gemini

**Purpose:** Research EDR/XDR solutions suitable for mid-sized organizations with cost comparisons

**The Prompt I Used:**

*"You are a cybersecurity purchasing consultant. Create a comparison table of EDR solutions for a mid-sized organization (500 employees, $50K security budget). Include: Microsoft Defender for Endpoint, SentinelOne, CrowdStrike Falcon. For each, provide: (1) Cost per endpoint/month, (2) Key ransomware detection capabilities, (3) Pros and cons, (4) Best use case. Focus on ransomware-specific features like behavior monitoring and rollback."*

**Response Summary:**

Gemini generated a detailed comparison table with pricing ($5-15/endpoint/month range), highlighted behavioral detection features (process monitoring, credential theft detection, lateral movement alerts), and provided nuanced pros/cons (e.g., Defender's advantage for Office 365 shops vs. SentinelOne's offline autonomous response). It identified specific ransomware features like automated file rollback and shadow copy protection monitoring.

**Quality Assessment:**

**Rating:** Excellent

**Why:** The table format was perfect for direct inclusion in the report. Pricing was current (verified with vendor websites in January 2026), and the "best use case" column helped me write recommendation logic for different organization profiles.

**How I Used This:**

**Report Section:** Section 5.3.1 (Deploy EDR)

**Specific Use:** Used the comparison table almost verbatim with minor formatting adjustments. The "Detection Capabilities Required" bullet list came directly from features Gemini identified across all three solutions.

**Verification:**

**How Verified:** Visited Microsoft, SentinelOne, and CrowdStrike pricing pages. Checked Gartner EDR Magic Quadrant 2025 for feature validation.

**Accuracy:** Yes - pricing accurate within $1-2/endpoint variance (likely regional differences), features matched vendor datasheets.

***

## **Prompt 4**

**Date:** 31/01/2026

**AI Tool:** Perplexity

**Purpose:** Find recent case studies where EDR stopped ransomware mid-attack

**The Prompt I Used:**

*"Find 2-3 real-world incidents from 2024 where EDR/XDR solutions successfully stopped ransomware attacks in progress before full encryption occurred. For each incident, provide: (1) Victim organization type, (2) Ransomware family, (3) Specific EDR product used, (4) How it detected the attack, (5) Percentage of systems saved. Include source citations."*

**Response Summary:**

Perplexity found three cases: (1) A legal firm vs. BlackCat where SentinelOne isolated 47 endpoints in 90 seconds, limiting damage to 3% of files; (2) A manufacturing company vs. LockBit where CrowdStrike detected lateral movement via PsExec and contained the attack to a single department; (3) A university vs. Hive where Microsoft Defender flagged vssadmin.exe shadow copy deletion and triggered automated isolation. Each included source links to security vendor blogs and news articles.

**Quality Assessment:**

**Rating:** Excellent

**Why:** Exactly what I needed—recent, specific, quantified outcomes (3% damage, 90 seconds response time). The legal firm case was perfect because it showed measurable impact, which makes the mitigation recommendation compelling.

**How I Used This:**

**Report Section:** Section 5.3.1 (Deploy EDR) - Case Reference subsection

**Specific Use:** Used the BlackCat/legal firm case study verbatim (2024 BlackCat affiliate attack stopped at 3% file encryption in 90 seconds). The specific metrics (90 seconds, 3% damage) made the recommendation concrete and believable.

**Verification:**

**How Verified:** Followed Perplexity's source links to SentinelOne's blog post dated March 2024 and a Security Week article covering the incident.

**Accuracy:** Yes - case study verified through multiple independent sources, timeline and damage percentages matched across sources.

***

## **Prompt 5**

**Date:** 31/01/2026

**AI Tool:** ChatGPT

**Purpose:** Understand network segmentation implementation for ransomware defense

**The Prompt I Used:**

*"You are a network security architect. Explain how to implement network segmentation specifically to limit ransomware lateral movement. Provide: (1) VLAN design for a mid-sized company with user workstations, servers, databases, and backup infrastructure, (2) Firewall rules between VLANs, (3) Why backup infrastructure must be isolated, (4) A real example where segmentation limited ransomware damage. Use technical detail suitable for IT staff implementing this."*

**Response Summary:**

ChatGPT provided a 5-VLAN architecture (users, servers, databases, backups, guest/IoT) with detailed firewall rule recommendations (e.g., "VLAN 10 can access VLAN 20 on ports 445, 3389 only; deny all VLAN 10→VLAN 40 traffic"). It explained that backup infrastructure isolation prevents affiliates from deleting backups via compromised admin credentials. Included a manufacturing company example where segmentation prevented RaaS from reaching SCADA systems, reducing ransom from $5M to $400K.

**Quality Assessment:**

**Rating:** Good

**Why:** Very strong technical depth with actionable VLAN design. The manufacturing case study was compelling. However, it didn't initially address software-defined segmentation (micro-segmentation), which I added through a follow-up prompt.

**How I Used This:**

**Report Section:** Section 5.3.2 (Network Segmentation and Zero Trust)

**Specific Use:** The 5-VLAN design became my recommended segmentation strategy. The manufacturing case study (attack contained, ransom reduced from $5M to $400K) demonstrated ROI effectively. Added the micro-segmentation tools (Illumio, pfSense) from my follow-up research.

**Verification:**

**How Verified:** Consulted Cisco and Palo Alto Networks best practice guides for VLAN segmentation. Searched for the manufacturing incident and found it referenced in a 2024 Q1 Coveware Ransomware Report.

**Accuracy:** Yes - VLAN architecture aligns with industry standards, case study verified in Coveware's quarterly threat report.

***

## **Prompt 6**

**Date:** 01/02/2026

**AI Tool:** Gemini

**Purpose:** Research phishing training effectiveness and costs for mitigation section

**The Prompt I Used:**

*"You are a security awareness training specialist. Provide data on: (1) What percentage of RaaS attacks start with phishing (cite recent statistics), (2) Effectiveness of phishing simulation training (before/after click rates), (3) Cost comparison of training platforms (KnowBe4, Cofense, Proofpoint) for 500 employees, (4) Best practices for training programs including frequency and content. Use 2024-2025 data where possible."*

**Response Summary:**

Gemini cited that 67% of RaaS initial access involves phishing (2024 Verizon DBIR), baseline employee click rates average 30% but can be reduced to <5% with regular training. Provided pricing for KnowBe4 ($500-3,000/year for 500 users) and competitors. Recommended monthly simulations using RaaS-specific templates (fake DocuSign, password expiry notices) and micro-learning modules. Included a financial services case study showing 89% reduction in successful phishing over 12 months.

**Quality Assessment:**

**Rating:** Excellent

**Why:** Data-driven with specific statistics (67% phishing, 30%→5% click rate reduction) and realistic cost estimates. The financial services case study with quantified improvement (89% reduction) was exactly what I needed to justify the training investment.

**How I Used This:**

**Report Section:** Section 5.4.1 (Phishing Simulations and Security Awareness)

**Specific Use:** The 67% statistic became my opening line justifying why training matters. The training structure (baseline assessment, monthly simulations, micro-learning, gamification) became my 4-step program. Cost and case study used directly.

**Verification:**

**How Verified:** Downloaded the 2024 Verizon Data Breach Investigations Report to confirm the 67% phishing statistic. Checked KnowBe4 pricing calculator for 500 users.

**Accuracy:** Yes - Verizon DBIR confirmed phishing percentage, pricing matched vendor quotes within 15% (volume discounts variable).

***

## **Prompt 7**

**Date:** 01/02/2026

**AI Tool:** Perplexity

**Purpose:** Research incident response plan components specific to ransomware

**The Prompt I Used:**

*"You are an incident response consultant specializing in ransomware. Outline the essential components of a ransomware incident response plan for a mid-sized organization. Include: (1) Roles and responsibilities during an attack, (2) Immediate containment actions (0-1 hour), (3) Short-term response (1-6 hours), (4) How to conduct tabletop exercises, (5) Communication templates needed. Focus on practical, actionable steps not just theory."*

**Response Summary:**

Perplexity provided a detailed IR framework with 4 key roles (Incident Commander, Technical Lead, Communications Lead, Legal), specific containment playbook with time-boxed actions (isolate systems in first hour, identify patient zero in 1-6 hours), tabletop exercise scenarios (e.g., "2 AM Saturday, 200 endpoints encrypted, backups compromised"), and pre-drafted communication templates (customer notification, regulatory breach notice, media statement). Emphasized that organizations with tested IR plans recover 50% faster.

**Quality Assessment:**

**Rating:** Excellent

**Why:** Extremely practical and immediately usable. The time-boxed containment actions (0-1 hour vs 1-6 hours) gave structure to what could be chaotic. The tabletop exercise scenario was realistic and specific enough to use as an example.

**How I Used This:**

**Report Section:** Section 5.4.2 (Incident Response Plan)

**Specific Use:** The roles, containment playbook, and tabletop exercise structure became the subsections of my IR plan recommendation. Used the "50% faster recovery" statistic to justify the cost investment. The tabletop scenario ("2 AM Saturday, 200 endpoints encrypted") used verbatim.

**Verification:**

**How Verified:** Cross-referenced with NIST Computer Security Incident Handling Guide (SP 800-61) and SANS Incident Handler's Handbook for best practices alignment.

**Accuracy:** Yes - framework aligns with NIST and SANS standards, recovery speed statistic found in IBM Security report.

***

## **Prompt 8**

**Date:** 01/02/2026

**AI Tool:** ChatGPT

**Purpose:** Get technical details on Windows Defender Application Control and Controlled Folder Access

**The Prompt I Used:**

*"Act as a Windows systems administrator. Explain how to implement Windows Defender Application Control (WDAC) and Controlled Folder Access to prevent ransomware execution and file encryption. Provide: (1) Step-by-step deployment process, (2) PowerShell commands, (3) How to handle false positives, (4) Pros and cons compared to third-party application whitelisting. Keep it practical for IT teams with limited resources."*

**Response Summary:**

ChatGPT provided a phased deployment approach (Audit Mode → Whitelist Building → Enforce Mode), specific PowerShell commands for enabling Controlled Folder Access and adding protected folders, guidance on handling false positives through approval workflows, and honest pros/cons (Pro: Free with Windows 10/11; Con: Requires maintenance of whitelist, may block legitimate apps initially). Noted that this is a low-medium priority control suitable for organizations already using Microsoft ecosystem.

**Quality Assessment:**

**Rating:** Good

**Why:** Very practical implementation guide with actual PowerShell commands I could include. The phased approach (audit first, then enforce) was smart to avoid disrupting business. However, the response was Windows-heavy and didn't address cross-platform environments, which limited applicability.

**How I Used This:**

**Report Section:** Section 5.4.3 (Application Whitelisting)

**Specific Use:** Used the PowerShell commands directly in the report as code blocks. The phased deployment (Audit → Whitelist → Enforce) became my implementation steps. The "Operational Challenge" note about false positives came from ChatGPT's warning about legitimate apps being blocked.

**Verification:**

**How Verified:** Tested the PowerShell commands in a Windows 11 virtual machine. Verified the commands executed successfully and enabled Controlled Folder Access as described.

**Accuracy:** Yes - PowerShell commands worked as written, process aligned with Microsoft's official documentation.

***

## **Prompt 9**

**Date:** 02/02/2026

**AI Tool:** Claude

**Purpose:** Research Active Directory hardening and privileged access management best practices

**The Prompt I Used:**

*"You are an Active Directory security specialist. Explain how to harden Active Directory against ransomware attacks where affiliates steal Domain Admin credentials. Cover: (1) Why Domain Admin access is critical to RaaS attacks, (2) AD hardening best practices (reduce admin count, tiered administration, disable NTLM, enable Credential Guard), (3) Privileged Access Management (PAM) solutions with cost estimates, (4) Just-in-Time access implementation. Target audience: IT security teams at mid-sized companies."*

**Response Summary:**

Claude explained that Domain Admins are "keys to the kingdom" because they can disable EDR, delete backups, and encrypt entire networks. Provided AD hardening checklist (limit Domain Admins to ≤3 accounts, implement tiered administration with Tier 0 for DCs/backups, disable NTLM, enable Credential Guard). Compared PAM solutions (CyberArk at $10K-50K vs open-source alternatives at $3K-8K/year). Described JIT access where admins request temporary elevated privileges that auto-revoke after a time window.

**Quality Assessment:**

**Rating:** Needs Refinement

**Why:** Excellent technical depth on AD hardening, but the PAM cost estimates were very broad ranges without enough detail on what drives costs (number of privileged accounts, feature sets). I had to do follow-up research on specific PAM vendors to get tighter pricing.

**How I Used This:**

**Report Section:** Section 5.4.4 (Secure Active Directory and PAM)

**Specific Use:** The "keys to the kingdom" phrasing became my opening line. AD hardening best practices (≤3 Domain Admins, tiered administration, disable NTLM, Credential Guard) used as a numbered list. JIT access explanation used to describe PAM workflow. Refined cost estimates through independent research.

**Verification:**

**How Verified:** Consulted Microsoft's AD security documentation and CIS Active Directory Benchmark. Checked CyberArk and BeyondTrust pricing guides for PAM cost validation.

**Accuracy:** Partially - Technical practices accurate and aligned with CIS benchmarks, but cost estimates needed refinement through vendor research.

***

## **Prompt 10**

**Date:** 02/02/2026

**AI Tool:** Gemini

**Purpose:** Research cyber insurance requirements and coverage for ransomware in 2025

**The Prompt I Used:**

*"You are a cyber insurance broker. Explain what mid-sized organizations need to know about cyber insurance for ransomware in 2025. Include: (1) What minimum security controls insurers now require before issuing policies, (2) What's typically covered (ransom payment, forensics, legal, downtime), (3) What's excluded, (4) Cost estimates for a company with $10M-50M revenue, (5) Why organizations might still get denied claims. Use 2025 market data."*

**Response Summary:**

Gemini explained that 2025 policies now mandate MFA, EDR deployment, quarterly backup testing, and incident response plans as prerequisites. Coverage includes ransom payment (up to policy limits of $1M-5M), forensic investigation, legal fees, regulatory fines, business interruption, and PR crisis management. Exclusions include failure to patch known critical CVEs within 30 days and prior known vulnerabilities. Cost estimates: $1,500-15,000/year based on revenue and industry. Claims can be denied if organizations had unpatched critical vulnerabilities or failed to meet policy prerequisites.

**Quality Assessment:**

**Rating:** Good

**Why:** Very current information reflecting 2025 market changes (stricter prerequisites). The list of required controls aligned perfectly with my other mitigation recommendations, creating good internal consistency in the report. Cost range was realistic and useful.

**How I Used This:**

**Report Section:** Section 5.5.2 (Cyber Insurance)

**Specific Use:** The four required controls (MFA, EDR, backup testing, IR plan) became my bulleted prerequisite list. Coverage and exclusions used to explain what insurance does and doesn't protect against. Cost estimate ($1,500-15,000/year) included in the section. The 30-day patching exclusion reinforced my earlier patching recommendations.

**Verification:**

**How Verified:** Reviewed sample cyber insurance policies from Coalition, Corvus, and At-Bay for 2025 coverage terms. Checked industry reports on cyber insurance market trends.

**Accuracy:** Yes - Prerequisites and coverage matched actual 2025 policy terms from major carriers, cost estimates aligned with broker quotes.

***

## **Prompt 11**

**Date:** 02/02/2026

**AI Tool:** Perplexity

**Purpose:** Find statistics on average ransomware costs and recovery times to justify mitigation investments

**The Prompt I Used:**

*"Provide the most recent statistics (2024-2025) on: (1) Average ransom payment amount for mid-sized organizations, (2) Total cost of ransomware attacks including downtime and recovery, (3) Average recovery time with vs without backups, (4) Percentage of organizations that pay ransom but don't recover data. Cite authoritative sources like IBM, Verizon, Sophos. I need these numbers to justify security investment ROI in a threat report."*

**Response Summary:**

Perplexity cited: (1) Average ransom payment $1.54M for mid-sized orgs (Sophos State of Ransomware 2024), (2) Total attack cost including downtime averages $1.85M (IBM Cost of Data Breach Report 2024), (3) Organizations with tested backups recover in 8-14 days vs 30-60 days without (Veeam Ransomware Trends Report 2024), (4) 46% of organizations that pay ransom still don't fully recover their data (Cybereason). Sources were properly cited with publication dates.

**Quality Assessment:**

**Rating:** Excellent

**Why:** Exactly the authoritative statistics I needed to build the ROI case for mitigation investments. The sources were top-tier industry reports that readers would trust. The contrast between recovery with backups (8-14 days) vs without (30-60 days) was particularly compelling.

**How I Used This:**

**Report Section:** Section 5.6 (Prioritized Implementation Roadmap) - Total Year 1 Investment vs Avoided Cost

**Specific Use:** Used the $1.85M total attack cost as the "Avoided Cost" line in my roadmap table to show that spending $35K-110K on mitigation is justified by avoiding a much larger loss. The backup recovery time statistics reinforced my immediate action recommendations.

**Verification:**

**How Verified:** Downloaded and reviewed the actual IBM, Sophos, and Veeam reports cited by Perplexity to confirm statistics matched and were in context.

**Accuracy:** Yes - All statistics verified in original source reports, numbers matched exactly, context appropriate.

***

## **Prompt 12**

**Date:** 02/02/2026

**AI Tool:** ChatGPT

**Purpose:** Create key success metrics (KPIs) for measuring mitigation effectiveness

**The Prompt I Used:**

*"Act as a cybersecurity metrics analyst. Create 5-7 key performance indicators (KPIs) that a mid-sized organization should track quarterly to measure the effectiveness of their ransomware mitigation program. For each KPI, provide: (1) The metric name, (2) How to measure it, (3) Target/goal, (4) Why it matters for ransomware defense. Make them measurable and actionable, not vague."*

**Response Summary:**

ChatGPT provided 6 KPIs: (1) Backup Recovery Testing success rate (measure: quarterly test results, target: 100%), (2) MFA Adoption (measure: % of accounts with MFA enabled, target: 100% privileged/95% all users), (3) Patch Compliance (measure: % critical CVEs patched within 14 days, target: 95%+), (4) Phishing Click Rate (measure: % employees clicking simulated phishing, target: <5% within 6 months), (5) Mean Time to Detect (measure: average time to identify ransomware activity, target: <1 hour), (6) Mean Time to Respond (measure: average time to isolate infected systems, target: <4 hours). Each included clear measurement methodology and realistic targets.

**Quality Assessment:**

**Rating:** Excellent

**Why:** Metrics were specific, measurable, achievable, relevant, and time-bound (SMART). The targets were realistic based on industry benchmarks. Having both leading indicators (patch compliance, MFA adoption) and lagging indicators (MTTD, MTTR) provided balanced measurement.

**How I Used This:**

**Report Section:** Section 5.7 (Key Success Metrics)

**Specific Use:** Used all 6 KPIs verbatim as my quarterly tracking recommendations. The clear measurement methodology made the metrics actionable for readers. The targets gave readers concrete goals to aim for rather than vague "improve security" statements.

**Verification:**

**How Verified:** Cross-referenced targets with industry benchmarks from SANS, NIST, and Gartner reports on security metrics best practices.

**Accuracy:** Yes - Targets aligned with industry benchmarks, measurement methods were standard practices used by SOC teams.

***

## **My Best Prompts**

**Most Effective:** Prompt #4 (EDR case studies from Perplexity) - Provided exactly what I needed (recent, specific, quantified outcomes) with proper citations. The 90-second response time and 3% damage metrics made the mitigation recommendation compelling and credible.

**Most Improved:** Prompt #9 (Active Directory hardening from Claude) - Initial response had broad cost ranges that weren't useful. Learned to ask for "cost drivers" and "feature-based pricing tiers" in follow-up prompts to get more actionable pricing information.

***

## **Lessons Learned**

**What Worked:**

1. **Assigning specific roles** ("You are a senior cybersecurity defense analyst") consistently produced more expert-level, nuanced responses than generic prompts.

2. **Requesting structured output** (tables, numbered lists, bullet points) made AI responses directly usable in the report with minimal editing.

3. **Using Perplexity for case studies and statistics** - Its built-in web search and citation features saved hours of manual source verification.

4. **Asking for cost estimates upfront** - Including budget context in prompts ensured recommendations were practical for mid-sized organizations, not just enterprise-scale solutions.

**What Didn't Work:**

1. **Generic prompts like "tell me about X"** - Required multiple follow-up prompts to get useful detail, wasting time.

2. **Not specifying time ranges** - Early prompts without "2024-2025" or "recent" often returned outdated information requiring re-prompting.

3. **Trusting AI-generated statistics without verification** - Found 2 instances where Claude cited plausible-sounding statistics that I couldn't verify in source reports. Learned to always cross-check numbers with primary sources.

4. **Over-relying on a single AI tool** - Different tools have different strengths (Perplexity for research with citations, ChatGPT for technical implementation, Gemini for comparison tables). Using the right tool for each task improved efficiency significantly.

***

