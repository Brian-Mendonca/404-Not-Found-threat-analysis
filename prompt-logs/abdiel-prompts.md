## Personal Information

**Name:** Abdiel Brian Mendonca
**Team:** 404 Not Found  
**Role:** GitHub Lead / Defense Analyst (Mitigation Strategies)  
**Total Prompts:** 6  

---

## Summary Statistics
```
| Tool       | Count | Excellent | Good | Needed Work |
|------------|-------|-----------|------|-------------|
| Perplexity | 3     | 3         | 0    | 0           |
| Gemini     | 2     | 2         | 0    | 0           |
| ChatGPT    | 1     | 0         | 1    | 0           |
```
---

## Prompt 1

**Date:** 30/01/2026  
**AI Tool:** Perplexity  

**Purpose:** Identify top technical controls against RaaS based on 2024–2025 incidents  

**The Prompt I Used:**

*You are a senior cybersecurity defense analyst. Based on RaaS attacks from 2024-2025 (LockBit, ALPHV/BlackCat), what are the top 5 technical controls that have proven most effective at preventing or limiting damage? For each control, provide: (1) How it works, (2) Cost estimate for mid-sized organizations (500 employees), (3) A real example where it stopped an attack. Use bullet points and cite sources.*

**Response Summary:**

The response listed immutable backups, MFA, EDR, network segmentation, and application whitelisting as the most effective RaaS mitigations, with cost ranges (around a few hundred to low five figures per month depending on control). It also referenced a healthcare provider that recovered in roughly 36 hours using immutable cloud backups, and cited recent ransomware reports and vendor case studies.

**Quality Assessment:**

- **Rating:** Excellent  
- **Why:** The answer was up to date, included realistic costs, and mapped each control to real incidents, which made it directly usable in my mitigation roadmap.

**How I Used This:**

- **Report Section:** Section 5.1 (Immediate Actions), Section 5.2 (Short-Term Controls)  
- **Specific Use:** I used this to decide which controls go into the “Immediate” vs “Short-Term” buckets and to justify emphasizing immutable backups and MFA as critical.

**Verification:**

- **How Verified:** Cross-checked the examples and cost ranges against recent public ransomware reports and vendor pricing pages.  
- **Accuracy:** Yes  

---

## Prompt 2

**Date:** 30/01/2026  
**AI Tool:** ChatGPT  

**Purpose:** Get implementation steps for the 3-2-1-1 immutable backup strategy  

**The Prompt I Used:**

*Act as a backup and recovery specialist. Explain how to implement the 3-2-1-1 backup rule to defend against ransomware that targets backup deletion (like LockBit). Include: (1) Step-by-step for AWS S3 Object Lock, (2) How to test recovery, (3) RTO and RPO targets for mid-sized organizations. Format as a numbered implementation guide.*

**Response Summary:**

The response outlined how to configure cloud storage with immutability, set retention periods, schedule regular backup jobs, and run periodic restore tests. It proposed recovery time objectives of roughly one to two days and recovery point objectives of a few hours for critical systems.

**Quality Assessment:**

- **Rating:** Good  
- **Why:** The steps were detailed and practical, but some initial suggestions around transfer protocols needed tightening from a security perspective.

**How I Used This:**

- **Report Section:** Section 5.1.1 (Implement Immutable Backups)  
- **Specific Use:** I adapted the high-level steps and the RTO/RPO target ranges into concise recommendations that fit the report’s page limits.

**Verification:**

- **How Verified:** Checked against official cloud provider documentation and ran a basic test configuration in a lab environment.  
- **Accuracy:** Partially (concepts accurate, some implementation details refined)  

---

## Prompt 3

**Date:** 31/01/2026  
**AI Tool:** Gemini  

**Purpose:** Compare EDR solutions with costs and ransomware-specific features  

**The Prompt I Used:**

*You are a cybersecurity purchasing consultant. Create a comparison table of EDR solutions for 500 employees: Microsoft Defender for Endpoint, SentinelOne, CrowdStrike Falcon. For each, provide: (1) Cost per endpoint/month, (2) Key ransomware detection capabilities, (3) Best use case. Focus on behavioral detection features.*

**Response Summary:**

The response produced a table with approximate per-endpoint pricing and highlighted capabilities like behavior-based detection, credential theft detection, lateral movement visibility, and rollback features. It also suggested which solution fits best depending on whether an organization is already invested in a particular ecosystem.

**Quality Assessment:**

- **Rating:** Excellent  
- **Why:** The tabular format and level of detail matched what I needed for a short EDR subsection without going over page limits.

**How I Used This:**

- **Report Section:** Section 5.2.1 (Deploy Endpoint Detection and Response)  
- **Specific Use:** I compressed the full comparison into a small table and summarized the common ransomware-relevant behaviors across all three tools.

**Verification:**

- **How Verified:** Compared listed capabilities and price ranges with public product documentation and pricing calculators.  
- **Accuracy:** Yes  

---

## Prompt 4

**Date:** 31/01/2026  
**AI Tool:** Perplexity  

**Purpose:** Get recent EDR case studies where attacks were stopped mid-execution  

**The Prompt I Used:**

*Find 2-3 real incidents from 2024 where EDR successfully stopped ransomware before full encryption. For each case, provide: (1) Victim type, (2) Ransomware family, (3) EDR product used, (4) How it detected the attack, (5) Approximate percentage of systems or data saved. Include citations to public reports or blogs.*

**Response Summary:**

The answer described several incidents, including one involving a legal firm targeted by a modern ransomware family where an EDR rapidly isolated affected endpoints so only a small fraction of files were encrypted. It also mentioned a manufacturing environment where lateral movement was detected and contained early.

**Quality Assessment:**

- **Rating:** Excellent  
- **Why:** The case descriptions included clear, quantitative outcomes (like small percentages of impacted data), which made the EDR recommendation much stronger in the report.

**How I Used This:**

- **Report Section:** Section 5.2.1 (EDR – Case Example)  
- **Specific Use:** I used one of the legal firm examples, trimmed down to a couple of sentences, to show how fast isolation can drastically limit damage.

**Verification:**

- **How Verified:** Read the underlying vendor blog posts and news articles that were referenced.  
- **Accuracy:** Yes  

---

## Prompt 5

**Date:** 01/02/2026  
**AI Tool:** Gemini  

**Purpose:** Get phishing training effectiveness and cost for the awareness subsection  

**The Prompt I Used:**

*You are a security awareness specialist. Provide: (1) Recent statistics on what percentage of ransomware or RaaS attacks start with phishing, (2) Typical change in click rates before vs after phishing simulation training, (3) Rough annual cost for phishing training platforms (like KnowBe4 or Cofense) for 500 employees, and (4) Best-practice structure for such a program. Use data from 2024–2025.*

**Response Summary:**

The response indicated that a large share of ransomware campaigns still begin with phishing, gave example click-rate reductions from roughly one-third of users to low single digits after sustained training, and provided realistic pricing bands for awareness platforms. It also described a program structure involving baseline assessment, recurring simulations, and short learning modules.

**Quality Assessment:**

- **Rating:** Excellent  
- **Why:** It combined statistics, cost, and program design in a compact way, so I could justify including awareness training without adding too much length.

**How I Used This:**

- **Report Section:** Section 5.3.1 (Security Awareness Training)  
- **Specific Use:** I used a single percentage for how often phishing is involved, plus the “30% down to under 5%” improvement and a simple four-step training structure.

**Verification:**

- **How Verified:** Cross-checked phish-derived-incident percentages against a recent public breach report, and checked a vendor’s pricing estimator.  
- **Accuracy:** Yes  

---

## Prompt 6

**Date:** 01/02/2026  
**AI Tool:** Perplexity  

**Purpose:** Outline practical ransomware incident response plan components  

**The Prompt I Used:**

*You are an incident response consultant. Outline the essential elements of a ransomware incident response plan for a mid-sized organization. Include: (1) Core roles, (2) Immediate containment actions in the first hour, (3) Key steps over the next few hours, and (4) How to design a simple tabletop exercise scenario. Focus on concise, practical guidance that can fit in a short report section.*

**Response Summary:**

The answer listed four key roles (overall lead, technical lead, communications, legal), then described first-hour actions like isolating suspected systems and disabling compromised accounts. It also showed how to structure a short tabletop exercise around a weekend ransomware scenario.

**Quality Assessment:**

- **Rating:** Excellent  
- **Why:** It was concise and already close to the level of detail needed for a short IR subsection, which helped keep the report within page limits.

**How I Used This:**

- **Report Section:** Section 5.3.2 (Incident Response Plan)  
- **Specific Use:** I compressed the role list and first-hour actions into a few bullets, and reused a simplified version of the tabletop scenario.

**Verification:**

- **How Verified:** Compared the structure to commonly referenced guidance for handling security incidents.  
- **Accuracy:** Yes  

---

## My Best Prompts

**Most Effective:** Prompt 4 – it produced recent, concrete EDR case examples with numbers, which made the mitigation section more convincing without needing long explanations.

**Most Improved:** Prompt 2 – initially I didn’t constrain transport and security details enough and had to refine the request to avoid weaker practices; this taught me to include security constraints directly in technical prompts.

---

## Lessons Learned

**What Worked:**

1. Being explicit about the **role** of the assistant (defense analyst, consultant, specialist) improved the technical depth and relevance of answers.  
2. Asking for **specific formats** (tables, numbered lists, short program structures) reduced editing effort and helped stay within page limits.  
3. Including **organization size and budget** in prompts led to recommendations that felt realistic for a mid-sized environment instead of enterprise-only solutions.

**What Didn’t Work:**

1. Broad prompts without time ranges sometimes returned older data and needed follow-up questions.  
2. Assuming any statistic is correct without checking the cited sources was risky; verification always took a few extra minutes but increased confidence in the final report.  

