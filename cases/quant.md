# Guanlan / Quant · a trader learning research application

[← Portfolio overview](../README.md) · [Architecture map](../assets/portfolio-architecture.svg)

## Division of responsibility

| Part | Role |
| --- | --- |
| **Guanlan / Quant** | Market data, time-bounded queries, computation, historical replay and research simulation. |
| **Jervis** | Replaceable workers, persistent trader experience, source references, versioned candidate judgment and scope. |
| **Lu Dongyangzi** | The persistent trader identity using those systems to study, decide, inspect outcomes and revise its understanding. |

The local workflow is: **point-in-time market evidence → domain reasoning → simulated decision and result → diagnosis → source-linked candidate experience → next research task**. Raw market data stays with Guanlan rather than being copied into the Jervis experience record. The relationship is coordinated through existing local processes; the diagram does not imply each arrow is a standalone network service.

## What has run

Historical case expansion, active queries, selective restudy and candidate experience updates have been reported in local execution records. A diagnostic loop ran initial simulated exams, identified weak points, revisited relevant cases, formed a candidate update and retested on new material. The records keep model output, simulation facts, and reviewer interpretation distinct. One worker completed but its experience update referenced a missing ID; the original output and failure were retained while the reference was repaired, rather than silently presenting the whole attempt as clean.

The next profit-wave learning round calls for broader examples, selected deep study and new tests. Its planned sample counts should never be represented as completed learning until its execution evidence is read back.

## What the results do not say

The completed diagnostic involved paused historical replay and simulated cash/inventory, not broker orders or real account returns. Some initial decisions lost money; two avoided part of a passive-hold loss; retests did not establish incremental profit over their relevant baselines. Historical exposure cannot be ruled out completely, and one process review had more information than a strict pre-decision blind reviewer. The results support an inspectable **learning and correction process**, not sustained profitable trading, reliable live reaction or a fully blind transfer result.

The broader Quant research system also has a cutoff-safe blind/reveal discipline: information is admissible only when `available_at <= decision_cutoff`. A separate N2 transfer challenge did not support the earlier N1 hypotheses. Those negative results remain part of the record rather than being relabeled as a strategy.
