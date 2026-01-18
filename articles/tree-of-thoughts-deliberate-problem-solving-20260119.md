# Tree of Thoughts: Deliberate Problem Solving with Large Language Models
**Authors:** Shunyu Yao (Princeton University), Dian Yu (Google DeepMind), Jeffrey Zhao (Google DeepMind), Izhak Shafran (Google DeepMind), Thomas L. Griffiths (Princeton University), Yuan Cao (Google DeepMind), Karthik Narasimhan (Princeton University)

**Category:** Technical Fundamentals

**Published:** 3 December 2023

---

## Key Points
- Tree of Thoughts (ToT) generalises Chain-of-Thought prompting by enabling LMs to explore multiple reasoning paths and backtrack when necessary
- ToT frames problem solving as search through a tree where each node represents a partial solution with intermediate "thoughts"
- On Game of 24, ToT achieved 74% success rate compared to only 4% for GPT-4 with chain-of-thought prompting
- The framework combines LM-generated thought evaluation with search algorithms (BFS/DFS) enabling systematic exploration with lookahead
- ToT augments LMs' "System 1" associative processing with "System 2" deliberate reasoning, drawing on classical AI search methods

---

## Summary
This paper introduces Tree of Thoughts (ToT), a framework that enhances language model reasoning by structuring inference as deliberate search through a tree of possible reasoning paths. While standard prompting methods generate text in a linear, left-to-right fashion, ToT allows models to explore multiple intermediate "thoughts", evaluate their promise, and backtrack when necessary - mimicking human deliberate problem-solving.

The framework addresses key limitations of existing approaches by enabling local exploration of different reasoning continuations and global planning with lookahead. ToT is modular, allowing customisation of thought decomposition, generation strategies, evaluation heuristics, and search algorithms (such as breadth-first or depth-first search) based on problem characteristics.

Experiments on three challenging tasks - Game of 24, Creative Writing, and Mini Crosswords - demonstrate significant improvements over chain-of-thought prompting. Most notably, on Game of 24, ToT achieved 74% success compared to just 4% for chain-of-thought, highlighting the value of deliberate exploration for tasks requiring non-trivial planning or search.

---
**Captured:** 19 January 2026

**Link:** https://arxiv.org/html/2305.10601v2

**Key Words:** Tree of Thoughts; Chain-of-Thought; LLM Reasoning; Search Algorithms; Problem Solving
