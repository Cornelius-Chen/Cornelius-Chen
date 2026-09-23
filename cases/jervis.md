# Jervis · learning that must survive a new task

[← Portfolio](../README.md) · [System map](../assets/portfolio-architecture.svg) · [Quant application](quant.md)

> **Research system, with bounded local execution.** Jervis studies how examples, practice and feedback become conditional domain judgment that a later worker can use. A completed run does not certify a new capability.

## The three questions behind the architecture

| Responsibility | Question it answers | Current evidence boundary |
| --- | --- | --- |
| **World / project state** | What is true about the current task, objects, environment and source material? | Persisted project facts and source references exist; this is not a trained general world model. |
| **Objective / quality judgment** | Given the human's goal and constraints, what result is worth pursuing? | Domain judgments and applicability conditions are represented; this is not a universal value model. |
| **Reality feedback** | Did the action and its later outcome support the judgment? | Tool observations, comparisons and review records exist; measured human benefit remains incomplete. |

The human supplies direction and retains final authority. External results can contradict the system's own explanations. This is why Jervis records **who observed what, when, and under which scope** before a proposed lesson can become reusable.

## The system in one example

In a local Designer apprenticeship, Jervis worked on a fictional workshop sign-up preview. The worker viewed professional reference material and actual page pixels, built a complete practice page and a different layout, compared them, and saved **two scoped experimental judgments**. Later, two unrelated briefs were frozen before the new judgments were used:

| Later task | Candidate handling | What the record supports |
| --- | --- | --- |
| Archive search interface | Both workshop-specific judgments were rejected as out of scope. | Scope filtering worked; this is not a learning win caused by those judgments. |
| Tool-library handoff interface | A general information-discovery judgment was selected; the workshop layout judgment was rejected. | The selected text reached the work and the resulting interface was exercised. Its incremental quality benefit was not isolated. |

The comparison retained a difficult result: a model reviewer preferred the new mechanism for parts of the archive task, yet favored the older/reference-supported approaches for the handoff task. Human preference evidence is still pending. **The learning pipeline ran; superiority did not emerge from this evaluation.**

## Responsibility map

| Owner | Responsibility | Boundary |
| --- | --- | --- |
| Human | Goal, acceptable risk, domain scope, intervention and final acceptance | No worker promotes its own result to a stable capability. |
| Mission / project state | Work graph, shared entities, contracts, checkpoints, dependencies and successor recovery | A worker process can end without erasing the project. |
| Registry + EventLog | Versioned objects, lifecycle and source-linked events | A new branch does not invent a second durable authority. |
| Domain learning | Source admission, practice, candidate judgment, applicability and failure conditions | Stored or retrieved material is not automatically learned capability. |
| Designer domain | Design methods, examples, visual comparisons and scoped advice | Original Designer material remains an independent source; integration is bounded. |
| Worker | A short-lived model execution for one scoped task | It may propose changes; state and acceptance live outside its conversation. |
| Evaluation | Fresh-task comparison, observed behavior and independent review | Model preference and human benefit are different observations. |

Jervis also has a bounded composition run in which a brief produced a work graph and small contracts for multiple specialties. Checkpoints allowed a successor to continue after a worker stopped; an old result could not overwrite newer state. Two composite works and a separate work-graph exercise tested these mechanics. They do not prove that Jervis generally chooses the best model or improves creative quality.

## Why the learning state has stages

```text
source + context
    → practice + variations
    → candidate judgment {applies_when, fails_when, provenance}
    → scope-filtered use or justified rejection on a later task
    → observed result + independent comparison
    → human-authorized version decision, only if evidence supports it
```

The architecture keeps **raw evidence, experimental candidate, accepted judgment and verified capability** separate. It also permits `no_update`: a run can teach the system that the evidence is insufficient. This separation is a deliberate answer to an agent's tendency to call a plausible explanation “learning.”

## What has been demonstrated

| Status | Evidence-backed claim |
| --- | --- |
| **Executed locally** | Source-backed Designer practice and variants, experimental judgment storage, scoped selection or rejection on later tasks, real page interaction and bounded multi-worker recovery. |
| **Evaluated, no gain claim** | Anonymous model comparisons gave mixed results; no independent evidence shows the mechanism beats direct reference use or the original Designer. |
| **Awaiting** | Human preference, long-term transfer, measured reduction in human minutes per verified outcome, and promotion to a stable cross-domain capability. |

Another local composition example changed one shared material fact from wood to gravel. The dependent audio, page and joint-observation branches were updated while unrelated motion and a separate project stayed intact. A later worker handoff also rejected a stale predecessor result. These are demonstrations of **shared semantic contracts, local invalidation and versioned commitment**; they do not establish general exactly-once side effects or globally coordinated resource leases.

Jervis compiles a WorkOrder / context packet for each worker. Scope and permission filtering happen **before** restricted domain content is read. The packet carries the facts, source references, relevant capability and budget the worker needs; the worker's output remains a proposal until a separately authorized state transition accepts it.

The governed program ledger still lists the structured Designer migration phase as active, with later program phases locked. Local integrated engineering deliveries describe their own bounded scope; they do not override that ledger.

## Public release shape

This page is a reviewed architecture case. The source workspace contains private registries, task inputs, local paths, research media and unfinished work; it is not the public repository. A separate runnable Jervis release should include a deliberately selected source slice, synthetic example, setup command, tests and a clear scope statement after that material is reviewed for redistribution.
