# 1️⃣ Introduction

**Tester(s):**  
- Name: Jose Flores Vargas 

**Purpose:**  
- The purpose of this test was to find anomalies and vulnerabilities, as many as possible, in the user registration functionality of the booking system and to categorize the findings.

**Scope:**  
- Tested components: Registration page, users and passwords creation.  
- Exclusions:  All the other functions of the booking system. 
- Test approach: Gray-box (some knowledge of the booking system)

**Test environment & dates:**  
- Start:  19.11.2025
- End:  19.11.2025
- Test environment details (OS, runtime, DB, browsers):
  - OS: Windows 11 
  - Runtime: Docker container
  - DB: PostgreSQL
  - Browser: Firefox 145.0.1

**Assumptions & constraints:**  
- The test was done in one day. 
- Test was limited stricly only to the registration functionality.  
---

# 2️⃣ Executive Summary

**Short summary:**  The penetration test of the booking system discovered some critical and medium vulnerabilities, for example, the possibility of been attack by SQL injection. Some of the founded weaknesses required an immediate remediation. 

**Overall risk level:** Critical

**Top 5 immediate actions:**  
1.  
2.  
3.  
4.  
5.  

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | SQL Injection in registration | Input field allows `' OR '1'='1` injection | Screenshot or sqlmap result |
| F-02 | 🟠 Medium | Session fixation | Session ID remains unchanged after login | Burp log or response headers |
| F-03 | 🟡 Low | Weak password policy | Accepts passwords like "12345" | Screenshot of registration success |

---

> [!NOTE]
> Include up to 5 findings total.   
> Keep each description short and clear.

---

# 5️⃣ OWASP ZAP Test Report (Attachment)

**Purpose:**  
- Attach or link your OWASP ZAP scan results (Markdown format preferred).

---

**Instructions (CMD version):**
1. Run OWASP ZAP baseline scan:  
   ```bash
   zap-baseline.py -t https://example.com -r zap_report_round1.html -J zap_report.json
   ```
2. Export results to markdown:  
   ```bash
   zap-cli report -o zap_report_round1.md -f markdown
   ```
3. Save the report as `zap_report_round1.md` and link it below.

---
> [!NOTE]
> 📁 **Attach full report:** → `check itslearning` → **Add a link here**

---
