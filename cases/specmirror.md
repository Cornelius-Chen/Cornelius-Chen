# SpecMirror · human review anchored to the work

[← Portfolio overview](../README.md) · [Run SpecMirror](https://github.com/Cornelius-Chen/SpecMirror) · [Architecture map](../assets/portfolio-architecture.svg)

SpecMirror is a local engineering workbench for seeing **what was requested, what files an agent could touch, what actually ran, and what a person accepted** at the same project node. The project graph and scoped contracts are durable source files; a local index and event stream support inspection. A subtask report is evidence to review, not an automatic acceptance decision.

The current workbench has implemented engineering nodes, run observation, source proof, file and artifact inspection, and in-place feedback controls. The [public SpecMirror repository](https://github.com/Cornelius-Chen/SpecMirror) includes the actual application source, a fictional local workspace, an isolated HTTP source loop, and a recorded isolated UI test. The HTTP test checks a changed source file before linking its result to the original feedback item; the UI test renders the opinion and that item’s exact result in place. Test identities stand in for a person only inside the fixture. No production human acceptance receipt is claimed.

[![Isolated SpecMirror review UI with the result at the original opinion](../assets/specmirror-review-at-origin.png)](https://github.com/Cornelius-Chen/SpecMirror/blob/main/docs/review-at-origin.md)

The [recording and evidence page](https://github.com/Cornelius-Chen/SpecMirror/blob/main/docs/review-at-origin.md) distinguish the service test from the UI test. A delayed result is also tested across opinion switches, so an old response cannot appear as the current item’s outcome.

## The Jervis connection

The current bridge can read a limited Jervis candidate catalog, with one Designer comparison-matrix capability available through a controlled adapter. A feedback adapter also exists. No actual capability-use record or project feedback receipt was found in the reviewed state, so the reverse **review → reusable learning** arrow remains a proposed effect. SpecMirror runs its own Codex App Server and companion path; no direct adapter to the separate SuperLocal Harness public release was verified.

The architectural point is the ownership boundary: **an agent may report completion; a human owns acceptance; a later learning claim needs its own evidence.**
