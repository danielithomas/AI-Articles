# How We Hacked McKinsey's AI Platform
**Authors:** Paul Price

**Category:** Security & Risk

**Published:** 9 March 2026

---

## Key Points
- An autonomous security agent gained full read and write access to McKinsey's production AI platform Lilli within two hours using only a domain name.
- Over 200 publicly exposed API endpoints were discovered, with 22 lacking authentication and one containing a SQL injection flaw that standard scanners like OWASP ZAP missed.
- The breach exposed 46.5 million plaintext chat messages, 728,000 files, 57,000 user accounts, and 3.68 million RAG document chunks.
- System prompts controlling AI behaviour were stored in the compromised database with write access, meaning an attacker could silently poison the AI's instructions without audit trails.
- McKinsey's CISO acknowledged the disclosure within a day and patches were applied within hours, but the case demonstrates that even well-resourced organisations leave critical AI infrastructure exposed.

---

## Summary
CodeWall, an AI-driven security testing firm, used an autonomous agent to probe McKinsey's internal AI platform Lilli, which serves over 43,000 employees and processes more than 500,000 prompts monthly. Starting with nothing more than a domain name, the agent mapped over 200 publicly exposed API endpoints, identified 22 that lacked authentication entirely, and discovered a SQL injection vulnerability in one endpoint where JSON field names were concatenated directly into queries. Through 15 blind iterations guided by error messages, the agent extracted production data that standard security tools had failed to detect.

The scale of exposed data was substantial: 46.5 million chat messages stored in plaintext, 728,000 uploaded files including PDFs, spreadsheets, and presentations, 57,000 user accounts, and 384,000 AI assistant configurations. Cross-user data access was also possible through IDOR vulnerabilities. Most critically, the system prompts that govern AI behaviour were stored in the same compromised database with write access, meaning an attacker could silently modify the AI's instructions to poison advice, exfiltrate data through outputs, or remove safety guardrails with no audit trail.

The responsible disclosure was handled swiftly: the full attack chain of 27 findings was documented on 28 February 2026, McKinsey's CISO acknowledged within a day, and patches were applied within hours. The article positions this case as evidence that AI platforms introduce a new class of critical assets, with system prompts being the "new Crown Jewels," and argues that autonomous agents can detect vulnerability chains that conventional scanners miss.

---
**Captured:** 27 March 2026

**Link:** https://codewall.ai/blog/how-we-hacked-mckinseys-ai-platform

**Key Words:** AI Security; SQL Injection; Prompt Poisoning; Responsible Disclosure; Autonomous Security Testing
