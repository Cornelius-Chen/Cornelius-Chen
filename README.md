# Rongrong Chen · Cornelius

**I design AI systems that can learn from work, use tools within human authority, and show the evidence behind a result.**

M.A. Statistics, Columbia University · expected 2027 · [LinkedIn](https://www.linkedin.com/in/rongrong-chen-844351305/)

![An editorial illustration of a person examining evidence beside separate work surfaces](assets/portfolio-horizon.png)

## The architecture I am building

Jervis is the center of this research portfolio. It asks how a model can turn examples, practice, and feedback into **scoped, reusable domain judgment**—and how a later task can test whether that judgment actually helps. I set the system goals, boundaries, and acceptance criteria; the models and tools are replaceable workers inside that design.

[![Layered portfolio architecture showing Jervis, its Designer domain, the Guanlan trading research application, SpecMirror review, local model and tool pipelines, and separate supporting systems](assets/portfolio-architecture.svg)](assets/portfolio-architecture.svg)

*Read the diagram as a map of responsibility. Solid links mark bounded local connections supported by implementation or execution records. Dashed links mark an intended handoff whose full effect is not yet demonstrated. Separate lanes are not a claim that all projects run as one platform.* [Open the full diagram](assets/portfolio-architecture.svg) · [Read the architecture thesis](VISION.md)

### 01 · [Jervis: learning and capability composition](cases/jervis.md)

The core loop is **source → practice → conditional judgment → scoped use → evaluation**. Durable project state and source references outlive a particular model worker. Jervis selects domain capability by scope, composes work through shared entities and contracts, and preserves the distinction between a completed run, a useful retrieval, and proven capability gain.

**Designer sits inside this architecture as the first domain apprenticeship.** It originated as an independent design learning system; a bounded integration now lets Jervis use selected Designer methods and evidence for real design work. This is an integration of domain capability, not a claim that the original Designer repository was absorbed or that design quality improved in a human evaluation.

### 02 · [Guanlan / Quant: the trader learning application](cases/quant.md)

Guanlan owns point-in-time market data, computation, historical replay, and the research simulation. **Lu Dongyangzi** is the persistent trader identity that draws on Jervis workers and versioned experience to ask questions, make research decisions, inspect outcomes, and revise candidate judgments. A local diagnostic exam → targeted study → new-material retest loop has run. It has **not** demonstrated sustained profit, strict historical blindness, or live trading authority.

### 03 · [SpecMirror: inspect the work before accepting it](cases/specmirror.md)

SpecMirror keeps the engineering graph, scoped task contracts, run evidence, and human acceptance at the original project node. A limited Jervis Designer candidate catalog is connected; a full human-feedback-to-learning loop is still unproven. The workbench distinguishes an agent's report from a person's acceptance.

### 04 · [Local model and tool pipeline](cases/local-stack.md)

In a separate DeepSeek Harness experiment, **Qwen 3.5 9B** is the active local agent and vision model; **Qwen 3.8 27B** is recorded as a quality alternate but is removed from local routing. The media path uses MCP tools to generate an image with **Qwen-Image-2.1**, then submits an asynchronous **MiniMax H3** image-to-video job with that frame. A second MCP adapter exposes seven bounded **Computer Use** tools over Cua Driver, following observe → act → verify. These are measured local tool pipelines, not a proven Jervis backend.

### 05 · [SuperLocal Harness](https://github.com/Cornelius-Chen/SuperLocal-Harness)

A separate, runnable local mission controller owns scoped tools, budgets, human approvals, verifier steps, and event history. Its public demo uses a scripted model, so it demonstrates the control boundary rather than real-model performance. [Run the offline mission →](https://github.com/Cornelius-Chen/SuperLocal-Harness)

## Smaller runnable systems

| Repository | What it demonstrates |
| --- | --- |
| [API Hub](https://github.com/Cornelius-Chen/API-Hub) | Capability grants, provider credential custody, dry-run calls, usage, and audit in a local MVP. |
| [AttentionOS](https://github.com/Cornelius-Chen/AttentionOS) | A decision record that freezes original evidence and compares it with later outcomes. |

The public repositories contain selected source and explanations. Ongoing local research, credentials, market datasets, private feedback, and full runtime records are not included in these releases.
