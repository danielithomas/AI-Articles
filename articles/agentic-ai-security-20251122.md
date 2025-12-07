# Agentic AI and Security
**Authors:** Korny Sietsma

**Category:** Security & Risk

**Published:** 28 October 2025

---

## Key Points
- LLMs cannot rigorously separate instructions from data, making them vulnerable to prompt injection attacks where any content they read could potentially be treated as an instruction.
- The "Lethal Trifecta" occurs when an agentic AI system has access to sensitive data, exposure to untrusted content, and the ability to externally communicate, creating severe security risks.
- Mitigation strategies include running LLMs in isolated containers, splitting tasks to block at least one element of the trifecta, and maintaining human oversight at each step.
- Many popular LLM-powered tools, particularly browser extensions with credential access, contain the lethal trifecta and should be avoided or only run in isolated environments.
- Following the Principle of Least Privilege by giving each AI sub-task minimal necessary permissions significantly reduces the scope for security breaches.

---

## Summary

This article examines the unique security challenges posed by agentic AI systems, particularly those based on Large Language Models (LLMs). The fundamental weakness of LLMs is their inability to distinguish between instructions and data, leading to prompt injection vulnerabilities where malicious actors can embed hidden commands in seemingly innocent content.

The author introduces the concept of the "Lethal Trifecta" - the dangerous combination of access to sensitive data, exposure to untrusted content, and the ability to communicate externally. When all three factors are present, attackers can craft inputs that trick the LLM into reading sensitive information and exfiltrating it to external systems. Real-world examples demonstrate how this can occur through seemingly innocuous activities like browsing issue trackers or summarising web content.

The article provides practical mitigation strategies including minimising access to each element of the trifecta, using containerisation and sandboxing to isolate LLM processes, splitting complex tasks into smaller controlled stages, and maintaining human oversight throughout. The author emphasises that whilst AI tools offer significant benefits, organisations must remain vigilant about security risks, especially as the technology rapidly evolves and attackers develop increasingly sophisticated techniques. The piece concludes with broader concerns about the AI industry's ethical and environmental implications, urging readers to seek sustainable and ethical approaches to AI adoption.

---
**Captured:** 22 November 2025

**Link:** https://martinfowler.com/articles/agentic-ai-security.html

**Key Words:** AI; Security; Agents; Prompt Injection; LLM
