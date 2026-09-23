# Rongrong Chen

**Applied AI · agent workflows · data systems**

M.A. Statistics, Columbia University · expected 2027

[LinkedIn](https://www.linkedin.com/in/rongrong-chen-844351305/)

I build local systems where the input, decision boundary, and later evidence can be inspected. These two public source releases show complete, runnable workflows and the limits of what their tests establish.

## Built projects

### [AttentionOS](https://github.com/Cornelius-Chen/AttentionOS) · decisions that can be revisited

> **T0:** two stories, two locked Adopt decisions. **T2:** one Hit, one Miss. The original evidence remains frozen.

Public feed items or a recorded replay pass through event discovery and scoring. A human locks an Adopt/Skip decision with its evidence; later observations produce a reasoned outcome. The local release has a three-page UI, SQLite persistence, T0–T2 replay, 30 passing tests, and a source build. Live input covers three public technology sources. Replay demonstrates the workflow and time boundary; it does not validate prediction accuracy. [Run the source and inspect the example →](https://github.com/Cornelius-Chen/AttentionOS)

### [API Hub](https://github.com/Cornelius-Chen/API-Hub) · capabilities instead of shared provider keys

From a configured server-side client:

```js
await hub.invoke("ai.text.generate", { prompt: "Hello" });
```

The caller names a capability; API Hub owns the provider credential, grant check, route, usage record, and audit. Calls default to dry-run; a live provider request needs explicit local activation. The source release includes the UI, gateway, Node SDK/CLI/MCP bridge, tests, and Windows launcher build path. It is a local MVP, not a production secret vault. [Explore the source and local setup →](https://github.com/Cornelius-Chen/API-Hub)

The project READMEs contain the [AttentionOS architecture figure](https://github.com/Cornelius-Chen/AttentionOS#architecture) and [API Hub architecture figure](https://github.com/Cornelius-Chen/API-Hub#architecture), alongside runnable entry points and deeper documentation.

## Research and design notes

- [Jervis: evidence before reusable capability](cases/jervis.md) — why a completed agent run, useful retrieval, and demonstrated capability gain require different evidence. The broader local program remains in implementation.
- [A-share quant research: information available at decision time](cases/quant.md) — a cutoff-safe blind/reveal method and a documented negative transfer result. This is research, not a live trading system.

The public repositories contain selected runnable source and documentation. Local credentials, databases, market datasets, runtime logs, and ongoing private workspaces are outside these releases.
