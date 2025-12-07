# The role of developer skills in agentic coding
**Authors:** Birgitta Böckeler

**Category:** Tooling & Technology

**Published:** 25 March 2025

---

## Key Points
- AI coding assistants require constant developer intervention, correction and steering even in successful coding sessions.
- AI missteps fall into three impact radiuses: time to commit, team flow disruption, and long-term maintainability issues.
- Developers need experience to catch issues like misdiagnosis of problems, brute-force fixes, and overly complex code that AI generates.
- The claim that AI will replace developers within a year is unrealistic, as autonomous AI coding for non-trivial tasks remains far from achievable.
- Teams need code quality monitoring, pre-commit hooks, custom rules, and cultures of trust to safely leverage AI coding assistants.

---

## Summary
This article examines the practical reality of using agentic coding assistants like Cursor, Windsurf and Cline through the lens of real development experience. Whilst these tools have made impressive progress in IDE integration and can execute tests, fix errors automatically, and conduct web research, they consistently require experienced developer oversight to produce quality code. The author categorises AI missteps into three impact radiuses based on feedback loop length: immediate issues affecting time to commit, problems creating team friction during an iteration, and insidious long-term maintainability concerns that may only surface weeks or months later.

The article provides concrete examples of where developer skills remain critical, including catching misdiagnosed problems (like Docker architecture issues), preventing brute-force fixes that mask root causes, avoiding overly broad implementations instead of incremental slices, and removing verbose or redundant code that AI generates. The most concerning category involves long-term maintainability issues where AI creates brittle, hard-to-change code through redundant tests, lack of code reuse, and overly complex implementations that experienced developers must catch and correct.

To mitigate these risks, the article recommends individual developers carefully review all AI-generated code and stop sessions when overwhelmed, whilst teams should implement code quality monitoring tools, shift-left practices like pre-commit hooks, custom rule configurations, and maintain cultures of trust that enable open communication about AI adoption challenges. The author concludes that whilst AI may assist in writing a large percentage of code, autonomous AI coding for non-trivial tasks remains far from reality, making developer experience and skills essential for the foreseeable future.

---
**Captured:** 22 November 2025

**Link:** https://martinfowler.com/articles/exploring-gen-ai/13-role-of-developer-skills.html

**Key Words:** AI; Coding Assistants; Developer Skills; Code Quality; Software Development
