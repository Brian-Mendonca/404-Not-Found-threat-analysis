## Personal Information

**Name:** Jay Goyal

**Team:** 404 Not Found

**Role:** Threat Researcher/Scrum Master

**Total Prompts:** 10

---

## Summary Statistics
```
|  Tool  | Count | Excellent | Good | Needed Work |
| ------ | ----- | --------- | ---- | ----------- |
| Gemini | 10    | 7         | 2    | 1           |
```

### Prompt 1

**Date:** 01/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To understand the high-level operational phases of a RaaS attack and the division of labor between operators and affiliates.

**The Prompt I Used:** "Act as a Threat Researcher. Explain the end-to-end technical lifecycle of a Ransomware as a Service (RaaS) attack. Distinguish between the responsibilities of the 'RaaS Operator' and the 'Affiliate'. Use a step-by-step breakdown."

**Response Summary:** The AI provided a six-stage lifecycle starting from Reconnaissance to Impact. It clearly distinguished that Operators provide the malware/infrastructure while Affiliates handle the "boots on the ground" tactical execution.

**Quality Assessment:** **Rating:** Excellent

**Why:** It provided a logical flow that differentiates RaaS from traditional ransomware, which is crucial for my report.

**How I Used This:** **Report Section:** Attack Lifecycle (Introduction)

**Specific Use:** Used the "Operator vs. Affiliate" distinction to define the threat ecosystem in the first paragraph.

**Verification:** **How Verified:** Cross-referenced with Microsoft’s "Cyber Signals" report on RaaS.

**Accuracy:** Yes

---

### Prompt 2

**Date:** 01/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To map the RaaS lifecycle specifically to the MITRE ATT&CK framework for technical depth.

**The Prompt I Used:** "For the RaaS lifecycle, identify the specific MITRE ATT&CK techniques used at each stage (e.g., Initial Access, Persistence, Lateral Movement). Include estimated durations for how long an attacker typically stays in the network before triggering encryption."

**Response Summary:** The AI mapped specific codes like T1566 (Phishing) and T1486 (Data Encrypted for Impact) to each phase. It also provided "dwell time" estimates, suggesting that attackers often stay 2–5 days for lateral movement.

**Quality Assessment:** **Rating:** Good

**Why:** The techniques were accurate, though I had to double-check the dwell times against recent Mandiant M-Trends reports to ensure they weren't outdated.

**How I Used This:** **Report Section:** Attack Lifecycle (Stage-by-stage breakdown table)

**Specific Use:** Populated the "Techniques" and "Duration" columns of the technical breakdown table.

**Verification:** **How Verified:** Checked the MITRE ATT&CK official website for the technique descriptions.

**Accuracy:** Yes

---

### Prompt 3

**Date:** 01/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To generate a narrative-based scenario and a CIA Triad impact analysis for the report.

**The Prompt I Used:** "Create a detailed attack scenario called 'Operation Health-Lock' involving a healthcare provider. Explain the end-to-end flow and then provide a CIA Triad Impact Analysis in a table format with High/Medium/Low ratings."

**Response Summary:** The AI generated a scenario where a hospital was hit via a Citrix vulnerability. It then accurately mapped why Confidentiality and Availability are "High" impact while Integrity is "Medium."

**Quality Assessment:** **Rating:** Excellent

**Why:** The scenario was realistic and directly addressed the "Double Extortion" tactic which is the most important part of modern RaaS.

**How I Used This:** **Report Section:** Attack Lifecycle (Scenario and CIA Impact Analysis)

**Specific Use:** This became the final two paragraphs and the core impact table of the section.

**Verification:** **How Verified:** Compared the scenario to the real-world 2024 Change Healthcare ransomware attack.

**Accuracy:** Yes

---

### Prompt 4

**Date:** 02/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To analyze the economic and business model of RaaS (Revenue sharing vs. Subscriptions).

**The Prompt I Used:** "Analyze the business model of Ransomware as a Service. Explain the difference between 'Subscription-based RaaS' and 'Affiliate-based profit sharing'. Specifically, how do Initial Access Brokers (IABs) monetize their role in this ecosystem?"

**Response Summary:** The AI explained that most modern RaaS uses an 80/20 profit split. It highlighted that IABs act as the 'supply chain' by selling pre-compromised credentials for a flat fee.

**Quality Assessment:** **Rating:** Excellent

**Why:** It provided a clear financial perspective which is necessary for the 'Threat Overview' section.

**How I Used This:** **Report Section:** Threat Overview (The RaaS Business Model)

**Specific Use:** Created a subsection explaining the financial incentive for affiliates.

**Verification:** **How Verified:** Cross-referenced with a KELA Cyber Intelligence report on IAB pricing.

**Accuracy:** Yes

---

### Prompt 5

**Date:** 02/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To gather detailed technical data on a specific case study (LockBit 3.0).

**The Prompt I Used:** "Provide a technical case study of the LockBit 3.0 attack on a major organization. What were the specific indicators of compromise (IoCs), and what was the unique 'Double Extortion' tactic used in this instance?"

**Response Summary:** The AI detailed the LockBit 3.0 (LockBit Black) variant, focusing on its use of the 'StealBit' exfiltration tool and its specialized leak site.

**Quality Assessment:** **Rating:** Good

**Why:** It gave specific tool names, though I had to search separately for the exact file hashes (IoCs).

**How I Used This:** **Report Section:** Case Studies (LockBit 3.0)

**Specific Use:** Used as the primary example for the 'Double Extortion' mechanics.

**Verification:** **How Verified:** Checked against the FBI/CISA Joint Cybersecurity Advisory on LockBit.

**Accuracy:** Yes

---

### Prompt 6

**Date:** 03/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To develop defensive strategies and mitigation controls for the Defense Analyst role.

**The Prompt I Used:** "Act as a Defense Analyst. Based on the RaaS attack lifecycle, suggest 5 high-impact mitigation strategies. Map these to the NIST Cybersecurity Framework (Identify, Protect, Detect, Respond, Recover)."

**Response Summary:** The AI suggested Multi-Factor Authentication (MFA), Network Segmentation, EDR deployment, Immutable Backups, and Employee Training, mapping each to a NIST function.

**Quality Assessment:** **Rating:** Excellent

**Why:** The NIST mapping makes the report look professional and industry-standard.

**How I Used This:** **Report Section:** Defense & Mitigation

**Specific Use:** Formed the core of the 'Recommended Security Controls' table.

**Verification:** **How Verified:** Compared with NIST SP 800-53 controls.

**Accuracy:** Yes

---

### Prompt 7

**Date:** 03/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To research the role of AI and LLMs in modern RaaS development.

**The Prompt I Used:** "How are RaaS affiliates currently using Generative AI or LLMs to enhance their attacks? Focus on automated phishing and polymorphic code generation."

**Response Summary:** The AI explained that LLMs are used to create perfect, error-free phishing emails in multiple languages and to help "re-skin" malware code to avoid signature-based detection.

**Quality Assessment:** **Rating:** Good

**Why:** It provided a forward-looking perspective, though it noted that most 'AI-generated' malware is still in early stages.

**How I Used This:** **Report Section:** Future Trends / AI Connection

**Specific Use:** Added a paragraph on how AI lowers the barrier to entry for low-skill affiliates.

**Verification:** **How Verified:** Read a blog post from SlashNext on "WormGPT" and adversarial AI.

**Accuracy:** Yes

---

### Prompt 8

**Date:** 04/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To draft the Executive Summary after all research was completed.

**The Prompt I Used:** "I have researched RaaS mechanics, the LockBit case study, and NIST mitigations. Act as a CISO and write a 250-word Executive Summary for a board of directors explaining the urgency of the RaaS threat."

**Response Summary:** The AI produced a high-level summary focusing on business continuity, financial risk, and the necessity of 'Zero Trust' architecture.

**Quality Assessment:** **Rating:** Excellent

**Why:** The tone was perfectly suited for executives—less technical, more risk-focused.

**How I Used This:** **Report Section:** Executive Summary (Section 1)

**Specific Use:** Used as the final draft for the very first page of the report.

**Verification:** **How Verified:** Self-edited to ensure it matched the specific healthcare scenario used earlier.

**Accuracy:** Yes

---

### Prompt 9

**Date:** 04/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To generate content for the Sprint Retrospective (Agile requirement).

**The Prompt I Used:** "Act as a Scrum Master. Help me write a Sprint Retrospective for a 2-week cybersecurity research project. What are typical 'What went well' and 'What could be improved' points for a team using AI for the first time?"

**Response Summary:** Suggested points included "High speed of research using AI" as a win, and "Difficulty in verifying AI hallucinations" as a challenge.

**Quality Assessment:** **Rating:** Good

**Why:** Provided the structure needed for the 'Retrospective' section of the Agile documentation.

**How I Used This:** **Report Section:** Agile Documentation (Retrospective)

**Specific Use:** Used these points as a template for our team's final meeting notes.

**Verification:** **How Verified:** Verified against the 'Retrospective Template' in the project guide.

**Accuracy:** Yes

---

### Prompt 10

**Date:** 05/02/2026

**AI Tool:** Gemini 3 Flash

**Purpose:** To understand the MITRE ATT&CK "Detection" aspect for SIEM/EDR.

**The Prompt I Used:** "For the RaaS technique 'Data Encrypted for Impact' (T1486), provide 3 specific detection logic ideas for a SIEM (e.g., monitoring for vssadmin.exe usage or high-volume file renaming)."

**Response Summary:** The AI suggested monitoring for the deletion of volume shadow copies and the mass modification of file extensions within a short timeframe.

**Quality Assessment:** **Rating:** Excellent

**Why:** It gave actionable "Logic" that a SOC analyst could actually use.

**How I Used This:** **Report Section:** Defense & Mitigation (Detection Logic)

**Specific Use:** Added a table of 'Detection Rules' to supplement the general mitigations.

**Verification:** **How Verified:** Checked the MITRE ATT&CK 'Detection' suggestions for T1486.

**Accuracy:** Yes

---

### My Best Prompts

**Most Effective: Prompt #3 - \[Why it worked well\]**

*   **Reasoning:** This prompt was the most effective because it applied the **SCOPE Framework** by providing a specific "Situation" (a healthcare breach) and a clear "Output Format" (narrative scenario followed by a High/Medium/Low CIA impact table). It forced the AI to synthesize technical RaaS mechanics into a realistic business impact, which directly met the project's learning objective of connecting Module 1-2 concepts to real threats.

**Most Improved: Prompt #2 - \[How it evolved\]**

*   **Evolution:** This prompt started as a general inquiry about attack stages (Prompt #1) but was evolved through **Iterative Refinement**. By adding specific constraints like "map to MITRE ATT&CK codes" and "include estimated dwell times," the output shifted from a generic overview to a professional-grade technical analysis suitable for a Tier-1 SOC brief.  

---

### Lessons Learned

#### What Worked:

*   **Adopting the SCOPE Framework:** Using **Specificity, Context, Output format, Parameters, and Examples** ensured that the AI acted as a "senior threat analyst" rather than a general-purpose chatbot. This led to more accurate technical details like specific tool names (e.g., Mimikatz, Rclone) instead of vague descriptions.  
    
*   **Iterative Prompting (3-5 iterations):** Planning for multiple turns rather than expecting a perfect "one-shot" answer allowed for better depth. For example, getting a general mitigation list first and then asking the AI to "map these specifically to the NIST Cybersecurity Framework" resulted in a much higher quality report section.  
    

#### What Didn't Work:

*   **Vague Initial Prompts:** Early attempts using broad queries like "tell me about ransomware" resulted in generic content that lacked the technical depth required by the project's **Quality Benchmarks**. These responses often missed the "Double Extortion" nuances critical to modern RaaS.  
    
*   **Over-reliance on AI "Freshness":** AI tools sometimes struggled with very recent 2024 group data or specific new CVEs. We learned that AI-generated facts—especially statistics and CVE numbers—must be **verified with a second source** like CISA or Mandiant before being committed to the report to avoid "hallucinations".
