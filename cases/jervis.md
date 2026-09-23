# Jervis · a learning architecture with evidence boundaries

[← Portfolio overview](../README.md) · [Architecture map](../assets/portfolio-architecture.svg)

## The architectural question

How does a model use external examples and practice to form a conditional domain judgment, apply it on a later task, and learn from the result—without letting one persuasive output certify its own improvement?

Jervis is my answer in progress: a **persistent project and experience layer around replaceable model workers**. I define the source boundary, domain scope, evaluation and acceptance rules. Each run can consume selected prior experience while the project state, evidence references, failures and candidate revisions survive worker replacement.

## The learning loop

1. **Admit a source and its context.** Preserve provenance and what the source actually shows.
2. **Practice and compare.** Create variations, inspect where a proposed judgment works and fails, and allow a `no_update` result.
3. **Keep a candidate.** State its `applies_when` and `fails_when`; keep it scoped and experimental.
4. **Use it on a later task.** Compile only relevant context for a worker; avoid placing all accumulated material in a global prompt.
5. **Evaluate separately.** A completed run and useful retrieval are not proof of capability gain. A fresh comparison and independent review are needed before stronger claims.

The system also composes work: shared project entities and small contracts let scoped workers handle parts of a task, with checkpoints, successor recovery and stale-result rejection in bounded local tests. These are execution properties; they do not automatically establish better design judgment.

## Designer is the first domain, not a peer box

Designer began as a separate design learning system and remains the source of its methods and material. A bounded Jervis integration has mapped selected Designer entry points, exercised source-backed practice and comparison, and used scoped domain guidance on design briefs. Core chooses and coordinates the domain capability; Designer retains the visual methods, examples and applicability limits. This is why the [architecture map](../assets/portfolio-architecture.svg) nests Designer inside the Jervis learning zone while acknowledging its independent origin.

## Evidence ceiling

The local delivery records report bounded Designer apprenticeship, scoped use, multi-project coordination and worker recovery. The governed program ledger still has the structured Designer migration active and later phases locked. Earlier independent comparisons were mixed or showed no gain; newer judgments remain experimental. There is no demonstrated human preference advantage, general autonomous learning, model-weight training, or measured reduction in human time per verified outcome.

**Design decision:** the state machine for a learning candidate and the decision to promote a capability belong to different authorities. This keeps a useful story about progress from becoming an unreviewable claim of improvement.
