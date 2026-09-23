# Architecture thesis · human-directed intelligence

[← Portfolio overview](README.md)

## The problem I am trying to solve

An agent can produce a plausible answer, finish a task, or remember a past result while still leaving important questions unanswered: Where did the evidence come from? What was the agent allowed to do? Who approved a consequential action? Did the result survive later review? Did the system actually improve on a fresh task?

My projects explore those questions at different points in the same lifecycle. They are currently **independent systems and research workstreams**. This document describes their logical fit and the conditions for a future integration; it does not describe a deployed platform.

## One lifecycle, separate owners

[![Rongrong Chen and six core projects in a relationship map](assets/portfolio-map.png)](assets/portfolio-map.png)

The map shows six core workstreams around me. Solid spokes mean project ownership; dashed links mean possible future integration. Quant research and product experiments are domain laboratories discussed in the table below, rather than components of an existing shared runtime.

| Layer | Purpose | Current work | What I can point to today |
| --- | --- | --- | --- |
| Evidence and decision | Retain input provenance and freeze a decision before later outcomes are known | AttentionOS; cutoff-safe quant research | Runnable AttentionOS release; [quant method and negative result](cases/quant.md) |
| Capability and permission | Express an allowed operation without distributing a provider credential | API Hub | Runnable local MVP with dry-run default, grants, and audit |
| Execution and verification | Route agent work through scoped tools, budgets, human approval, and a verifier | IRONMAN Harness; DeepSeek Harness experiments | Runnable scripted offline mission and approval example in the public IRONMAN release |
| Human review | Let a person inspect agent plans, work state, and evidence before accepting a result | SpecMirror / Mirror | Local prototype and design work, not a public source release here |
| Learning | Keep candidate knowledge separate from independently demonstrated capability | Jervis | [Research note](cases/jervis.md), including a bounded evaluation that did not support capability gain for one sample |
| Explanation and applications | Make complex state understandable; challenge the architecture in domain-specific settings | Designer; digital studio, community, and other application experiments | Separate local design and product work; no shared runtime is claimed |

The ownership boundaries matter more than a single diagram. AttentionOS owns its decision record. API Hub owns provider grants and usage. IRONMAN owns mission execution and approval. A future workspace should connect those records through explicit contracts while preserving each source of truth.

## What integration would require

1. **A shared case identity and evidence references.** A decision, capability call, mission, review, and later outcome would need traceable references without copying each subsystem's private state into a new authority.
2. **A real permission handoff.** A mission could request an API Hub capability only under a verified grant and with the same human approval boundary visible in its event history.
3. **A closed review loop.** A reviewer would be able to compare the original evidence, approved action, tool receipts, verifier result, and later outcome before accepting a conclusion.
4. **Independent learning evaluation.** A proposed reusable lesson would face a fresh, frozen comparison. A completed run or useful retrieval alone would not count as capability gain.

Those are acceptance conditions for future work, not features claimed by the current releases. The immediate public proof is simpler: each released component can be run and examined on its own.

## Why the portfolio is arranged this way

The homepage leads with runnable work, then shows the broader design question and research limits. The visual is an editorial illustration of separate work surfaces, not a system topology diagram. The repositories contain the actual architecture figures and commands for readers who want to inspect implementation details.
