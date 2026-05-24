# LLM Prompting Techniques Overview

This document provides a high-level, categorised comparison of modern prompting techniques that improve reasoning, planning, and self-correction in large language models (LLMs).  
It is intended as a quick reference – follow the links to dedicated pages for more detailed explanation.

> **Important clarification**  
> These techniques are **prompting strategies applied by the human** (or a wrapper application) to adapt how a model is queried. They do not modify the model itself but instead **elicit specific reasoning patterns the model is already capable of** thanks to its training. The model’s output structure changes in response to the prompt design – the technique lies in how you ask, not in what the model is.
>
> Some modern models (e.g., OpenAI o‑series, DeepSeek‑R1) have internal reasoning steps built in, making them automatically “chain‑of‑thought” without an explicit prompt. Even then, the user may still influence reasoning depth or style through prompting. For most off‑the‑shelf models, the techniques below are the primary way to steer reasoning and accuracy.

## Categorised Techniques

> **Note on categorisation:** Boundaries between these groups are fluid; many techniques can be combined (e.g., Self-Consistency + CoT, ReAct + Self-Refine). This layout simply helps you quickly locate the pattern most relevant to your problem.

### 1. Reasoning Topologies (Structure)
Techniques that define *how* reasoning steps are organised – from simple linear chains to dynamic graphs and iterative dialogues.

| Technique                      | Short Description                                                                                             | Typical Use Cases                                                       | Best Suited For                                                                                                |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Chain of Thought (CoT)**     | Linear, step-by-step reasoning within a single prompt.                                                        | Arithmetic, multi-step logic, debugging.                                | Any capable LLM (GPT-4, Claude, Gemini, Llama 3). Works best with models that can follow lengthy instructions. |
| **Tree of Thoughts (ToT)**     | Explores multiple reasoning paths at each step using tree search (BFS/DFS).                                   | Complex planning, creative writing, constraint satisfaction.            | LLMs with high instruction-following ability; requires explicit state evaluation.                              |
| **Graph of Thoughts (GoT)**    | Models reasoning as a directed graph, allowing merging and refinement of intermediate thoughts.               | Sorting, document merging, tasks requiring synthesis of multiple ideas. | Advanced LLMs (GPT-4 class) due to complex prompt orchestration.                                               |
| **Iteration of Thought (IoT)** | Uses an inner dialogue agent to dynamically generate context-specific prompts and refine answers iteratively. | Tasks requiring adaptive refinement, ambiguous queries.                 | LLMs that can maintain inner dialogue state across turns.                                                      |
### 2. Multi-Path Evaluation & Refinement
Strategies that generate multiple reasoning paths and use voting or iterative improvement to boost reliability.

| Technique                      | Short Description                                                                            | Typical Use Cases                                        | Best Suited For                                                        |
| ------------------------------ | -------------------------------------------------------------------------------------------- | -------------------------------------------------------- | ---------------------------------------------------------------------- |
| **Self-Consistency (SC)**      | Samples multiple CoT reasoning paths and picks the most consistent answer via majority vote. | Factual QA, math problems where reliability is critical. | Any LLM; benefits from sampling multiple completions (higher compute). |
| **Boosting of Thoughts (BoT)** | Iteratively improves reasoning by identifying flaws in previous attempts and refining.       | Error-sensitive tasks, code generation, theorem proving. | LLMs that can critique their own outputs (self-evaluation).            |
### 3. Self-Correction & Autonomous Reflection
Techniques where the LLM critiques and refines its own output, sometimes using memory of past failures.

| Technique       | Short Description                                                                                              | Typical Use Cases                                   | Best Suited For                                             |
| --------------- | -------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- | ----------------------------------------------------------- |
| **Self-Refine** | Uses the LLM to generate feedback on its own output and then refine it, repeating the cycle.                   | Text quality improvement, code review, translation. | LLMs with strong self-critique ability (e.g., GPT-4).       |
| **Reflexion**   | Agentic approach where the LLM reflects on past failures stored in episodic memory to improve future attempts. | Autonomous agents, gaming, complex decision-making. | LLMs integrated with tool use and memory (LangChain, etc.). |
### 4. Task Decomposition & Planning
Methods that break a complex problem into manageable parts or dynamically compose a reusable reasoning plan.

| Technique               | Short Description                                                                                 | Typical Use Cases                                                              | Best Suited For                                        |
| ----------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------ |
| **Least-to-Most (LtM)** | Decomposes a complex problem into simpler sub-problems and solves them sequentially.              | Compositional reasoning, instruction following.                                | Any LLM; requires careful decomposition prompt design. |
| **Self-Discover**       | The LLM composes its own reasoning structure by selecting and combining atomic reasoning modules. | Tasks where a reusable reasoning strategy exists (logical deduction, puzzles). | LLMs that can meta-reason about their own processes.   |
| **Active-Prompt**       | Selects the most uncertain examples for human annotation to build few-shot prompts dynamically.   | Tasks with limited labeled data or uncertain model behaviour.                  | Any LLM; relies on human-in-the-loop for annotation.   |
### 5. Hybrid Reasoning & Acting (Agentic Patterns)
Techniques that combine reasoning with external tools, code execution, or environment interaction.

| Technique                     | Short Description                                                                                              | Typical Use Cases                                       | Best Suited For                                                     |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------------------- |
| **ReAct**                     | Interleaves reasoning and action steps so the LLM can interact with external tools (e.g., search, calculator). | Information-seeking tasks, interactive decision-making. | LLMs with tool/action integration (function calling).               |
| **Program of Thoughts (PoT)** | Generates executable code (e.g., Python) as the reasoning path and offloads computation to an interpreter.     | Numerical computation, algorithmic tasks.               | LLMs with strong code generation, paired with a Python interpreter. |

---
## References
- [Chain-of-Thought (Wei et al., 2022)](https://arxiv.org/abs/2201.11903)
- [Tree of Thoughts (Yao et al., 2023)](https://arxiv.org/abs/2305.10601)
- [Graph of Thoughts (Besta et al., 2024)](https://arxiv.org/abs/2308.09687)