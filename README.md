# Rongrong Chen

**Applied AI · agent workflows · data systems**

M.A. Statistics, Columbia University · expected 2027

[LinkedIn](https://www.linkedin.com/in/rongrong-chen-844351305/)

I build local systems where the input, decision boundary, and later evidence can be inspected. These two public source releases show complete, runnable workflows and the limits of what their tests establish.

## Built projects

### [AttentionOS](https://github.com/Cornelius-Chen/AttentionOS) · decisions that can be revisited

![AttentionOS architecture](https://raw.githubusercontent.com/Cornelius-Chen/AttentionOS/main/docs/images/architecture.png)

Public feed items or a recorded replay pass through event discovery and scoring. A human locks an Adopt/Skip decision with its original evidence; later observations produce a reasoned outcome without rewriting that snapshot. The release includes a three-page local UI, SQLite persistence, T0–T2 replay, 30 passing tests, and a source build. Live input covers three public technology sources. Replay demonstrates the workflow and time boundary; it does not validate prediction accuracy. [Source and three-minute walkthrough →](https://github.com/Cornelius-Chen/AttentionOS)

### [API Hub](https://github.com/Cornelius-Chen/API-Hub) · capabilities instead of shared provider keys

![API Hub architecture](https://raw.githubusercontent.com/Cornelius-Chen/API-Hub/main/docs/images/architecture.png)

Applications and short-lived agents receive scoped capability access. The local gateway checks policy and grants, routes through reviewed adapters, and records usage and audit. Provider credentials are write-only in the control plane and absent from client responses. Calls default to dry-run; a live provider request needs explicit local activation. The source release includes the UI, gateway, Node SDK/CLI/MCP bridge, tests, and Windows launcher build path. It is a local MVP, not a production secret vault. [Source and local setup →](https://github.com/Cornelius-Chen/API-Hub)

## Research and design notes

- [Jervis: evidence before reusable capability](cases/jervis.md) — why a completed agent run, useful retrieval, and demonstrated capability gain require different evidence. The broader local program remains in implementation.
- [A-share quant research: information available at decision time](cases/quant.md) — a cutoff-safe blind/reveal method and a documented negative transfer result. This is research, not a live trading system.

The public repositories contain selected runnable source and documentation. Local credentials, databases, market datasets, runtime logs, and ongoing private workspaces are outside these releases.
