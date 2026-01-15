# Lessons from Red Teaming 100 Generative AI Products
**Authors:** Blake Bullwinkel, Amanda Minnich, Shiven Chawla, Gary Lopez, Martin Pouliot, Whitney Maxwell, Joris de Gruyter, Katherine Pratt, Saphir Qi, Nina Chikanov, Roman Lutz, Raja Sekhar Rao Dheekonda, Bolor-Erdene Jagdagdorj, Eugenia Kim, Justin Song, Keegan Hines, Daniel Jones, Giorgio Severi, Richard Lundeen, Sam Vaughan, Victoria Westerhoff, Pete Bryan, Ram Shankar Siva Kumar, Yonatan Zunger, Chang Kawaguchi, Mark Russinovich (Microsoft AI Red Team)

**Category:** Security & Risk

**Published:** 2024

---

## Key Points
- AI red teaming requires understanding both system capabilities and deployment contexts to prioritise testing against real-world risks, starting from potential impacts and working backwards to attack strategies
- Simple attacks often outperform sophisticated gradient-based methods in practice; real-world adversaries prioritise practical techniques like jailbreaks and multi-turn prompting over academic exploits
- Automation tools like PyRIT help scale testing coverage, but human expertise remains essential for subject matter knowledge, cultural competence, and emotional intelligence assessments
- LLMs amplify existing security vulnerabilities (e.g. SSRF, improper error handling) while introducing new attack vectors like prompt injection and cross-prompt injection attacks (XPIA)
- AI security is an ongoing economic challenge rather than a solvable technical problem, requiring continuous break-fix cycles, defence-in-depth measures, and regulatory frameworks

---

## Summary
The Microsoft AI Red Team (AIRT) shares insights from red teaming over 100 generative AI products since 2018, presenting their internal threat model ontology and eight key lessons learned. The ontology models vulnerabilities through five components: System (the application being tested), Actor (adversarial or benign user being emulated), TTPs (Tactics, Techniques, Procedures mapped to MITRE ATT&CK and ATLAS), Weakness (the exploitable vulnerability), and Impact (downstream harm such as data exfiltration or harmful content generation). This framework accommodates both security risks and responsible AI (RAI) harms.

The eight lessons address: (1) understanding system capabilities and deployment contexts before scoping attacks; (2) prioritising simple attacks over gradient-based methods since real attackers use practical techniques; (3) distinguishing red teaming from safety benchmarking as the former discovers novel harms while the latter measures known risks; (4) leveraging automation through their open-source PyRIT framework while maintaining human oversight; (5) preserving essential human elements including subject matter expertise, cultural competence, and emotional intelligence; (6) recognising that RAI harms are pervasive but subjective and difficult to measure; (7) addressing how LLMs both amplify existing security risks and introduce new attack vectors; and (8) accepting that AI security work will never be complete but can raise the cost of attacks through defence-in-depth.

The paper includes five case studies demonstrating practical applications: jailbreaking vision language models via image overlays, assessing LLM potential for automated scam systems, evaluating chatbot responses to distressed users, probing text-to-image generators for gender bias, and identifying traditional SSRF vulnerabilities in GenAI video processing applications. The authors emphasise that effective red teaming must consider both adversarial attackers and benign users who encounter failures unintentionally.

---
**Captured:** 15 January 2026

**Link:** https://download.microsoft.com/download/4/9/6/496deaed-0dab-4e1d-85eb-7489a0f242a6/Lessons%20From%20Red%20Teaming%20100%20Generative%20AI%20Products%20eBook.pdf

**Key Words:** AI Red Teaming; Generative AI Security; Responsible AI; Prompt Injection; LLM Safety
