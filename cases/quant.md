# Guanlan / Quant · training a research trader across system boundaries

[← Portfolio](../README.md) · [Run the Guanlan source](https://github.com/Cornelius-Chen/Guanlan-Quant) · [System map](../assets/portfolio-architecture.svg) · [Jervis architecture](jervis.md)

> **Historical research and simulated decisions.** Lu Dongyangzi is a persistent trader identity in a research loop, not a trained foundation model or an autonomous brokerage account.

## The three-part architecture

| Owner | Holds | Sends to the next step |
| --- | --- | --- |
| **Guanlan / Quant** | Market data and provenance, time-bounded queries, computation, historical replay and simulated cash/inventory | A decision packet containing only observations admitted at that point in time. |
| **Jervis** | Replaceable model workers, source-linked domain experience, current candidate understanding and versioned state | A scoped worker context and a research judgment; raw market history stays with Guanlan. |
| **Lu Dongyangzi** | One continuing trader identity across research tasks | Questions, proposed actions, reflection and candidate revisions that can be inspected later. |

The existing local coordinator links the parts. This is a **responsibility and artifact chain**, not a claim that every arrow is a direct network API.

In the recorded trader-training stages, Quant coordinated the work and performed deterministic data queries. A Jervis MissionWorker ran a short-lived Codex CLI model process with a scoped input; its raw output and receipt returned to the Q2 experiment. The coordinator then ran the research simulation and wrote the result. Jervis kept the continuing identity and candidate experience for later workers. This should not be confused with the separate Qwen 9B / image / Computer Use experiments shown elsewhere in the portfolio.

```text
point-in-time market packet
    → Jervis worker's scoped judgment
    → Guanlan historical replay + simulated accounting
    → observed outcome and failure diagnosis
    → source-linked candidate experience in Jervis
    → next worker sees only relevant, permitted experience
```

## Guanlan's internal ownership

| Domain | Purpose |
| --- | --- |
| Q1 | Market facts, source provenance and data readiness. |
| Q2 | Research questions, historical cases, comparisons and backtests. |
| Q3 | Runtime serving and read-only/controlled surfaces; research does not itself grant order authority. |
| Q4 | Market-structure representation and learning assets. |
| Q5 | Routing, permissions and audit across domains; it does not take over Q1–Q4 business meaning. |

**Q4 and Jervis have different owners.** Q4 is Guanlan's existing structure-learning domain. Jervis is the external learning and execution framework reused by this trader research. The current record does not show that every Lu Dongyangzi revision automatically becomes a Q4 asset.

The project keeps its market warehouse outside the code repository and exposes it through an established access layer. A historical observation belongs in a decision packet only when `available_at <= decision_cutoff`. A later reveal can diagnose a decision; it cannot be smuggled back into the decision-time view.

The research record distinguishes public historical disclosures, supplier data, existing minute bars, and read-only current-market bridges. Each has a different availability time and coverage limit. For example, a company or industry mapping collected later is not automatically the mapping a historical decision maker could have seen. The public case does not redistribute those data sources.

## A completed diagnostic loop

The trader research application ran **initial simulated exams → weak-point diagnosis → targeted rereading → candidate experience revision → new-material retests**. The record keeps original worker output, market/simulation facts, and reviewer judgment distinct. Its candidate update remained `K1_CANDIDATE` because the retests did not independently establish an improved trading ability.

One simulated switch exposed a useful architectural error: **selling A** and **buying B** were treated too closely as one choice. The first action could reduce a loss while the replacement purchase still lost money. The candidate revision separated them into two tests: whether A should still be held, and whether B independently beats holding cash under the same time, cost and execution assumptions. This is a concrete example of turning a failure into a conditional research rule, not proof that the new rule now makes money.

The query contract was tested by a smaller failure too: a request used a negative drawdown parameter against a positive drawdown definition. The error was retained and the learner had to resubmit a semantically valid request. The failure was not converted into “zero matching cases.” This matters because a plausible zero can silently change a model's next decision, whereas an explicit error leaves a repairable evidence trail.

A separate numeric transfer challenge also retained a negative result: N1 hypotheses did not hold in N2. The system preserves that failure and requires a new cutoff-safe blind iteration before promoting another structure. It does not equate a promising backtest with live authority.

## Evidence limits

| Observed | Still unproven |
| --- | --- |
| Historical cases, active queries, candidate experience updates, simulated decisions, failure preservation and local diagnostic retests. | Sustained active profit, strict absence of all historical exposure, real-time reaction, live account performance, broker execution or model-weight training. |

The exam used paused historical replay and an assumed next-minute quote, not real fills. A process reviewer saw a simulated action receipt immediately after a node, so it was not a strictly pre-decision blind review. The current broader profit-wave learning round is ongoing; its planned sample counts are not completed-result claims.

## Public runnable slice

The [Guanlan-Quant repository](https://github.com/Cornelius-Chen/Guanlan-Quant) contains selected original Q1–Q5 modules and an invented, repeatable research fixture. It verifies Q1 snapshot readiness and a Q2 refusal of a mutated snapshot, compares four distinct simulated actions, records a revised Q3 question, writes a non-promoted Q4 candidate, and creates a Q5 replay receipt.

An [optional second run](https://github.com/Cornelius-Chen/Guanlan-Quant/blob/main/docs/jervis-bridge.md) pins the public Jervis code and creates an isolated Registry with three synthetic candidate versions. Guanlan's new release adapter fetches an **exact object version**, verifies the source and attachment, and checks the trader, scope and decision cutoff before storing the resolved reference in a Q3 research packet. A later invented price path is replayed with fixed actions. The latest version retains the prior active text after a `no_update` proposal. This is a public demonstration of a version boundary; the private historical Quant coordinator and K0/K1 snapshots were not released or replayed here.

[![Four separate synthetic Guanlan decisions](../assets/guanlan-synthetic-decisions.png)](https://github.com/Cornelius-Chen/Guanlan-Quant)

In the first fixture, B beats cash, but switching A into B trails holding A. Existing cash can buy B without selling A. In the second invented path, the simulated switch happens to win. These are contract examples, not the historical Lu Dongyangzi exam. Neither public run invokes a Jervis worker, reproduces the private candidate experience, or makes a historical return claim. Raw market data, account state, strategy thresholds, exact test windows and complete worker prompts stay outside the release.
