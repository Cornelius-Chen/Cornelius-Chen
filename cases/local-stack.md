# Local model, media and Computer Use pipelines

[← Portfolio overview](../README.md) · [Public source and receipts](https://github.com/Cornelius-Chen/Local-Pipelines) · [Architecture map](../assets/portfolio-architecture.svg)

This is a **separate DeepSeek Harness engineering track**. It tests how a local model invokes media and desktop tools through explicit MCP surfaces. It is not the published SuperLocal Harness release and has not been verified as Jervis's execution backend.

## Model choice and routing

`Qwen 3.5 9B` is configured as the active local agent and vision route. `Qwen 3.8 27B` appears in the registry as a quality alternate, but is removed from local routing. The 27B entry is not evidence that every workflow was tested or that dynamic model selection works. Local tests found a 9B Computer Use ceiling; the route remains a bounded experiment.

## Image to video, with receipts

```text
9B agent / vision
    → MCP generate_image → ComfyUI Qwen-Image-2.1 → first-frame PNG
    → MCP submit_video_job → queued job ID → ComfyUI MiniMax H3 FL2VA
    → status / result → MP4 artifact in the transcript
```

The image backend was selected after a local A/B comparison with the previous image model. The video job is asynchronous because generation takes longer than a normal tool call. The backend releases the reasoning model's GPU residency before heavy video generation and returns the artifact only after the job reports completion. The [public release](https://github.com/Cornelius-Chen/Local-Pipelines) includes a matching first frame, MP4 and redacted job record from one local run; this is a media-pipeline receipt, not a claim about visual taste or general creative quality.

## MCP Computer Use

The desktop path reuses the harness's MCP client and places a thin seven-tool adapter over Cua Driver, whose larger native tool set is not exposed to the model. The intended action loop is **observe → smallest action → observe again → verify the postcondition**. Bounded local tests read back Calculator and Notepad results; the driver can enforce the declared target, policy, budget and lease. Later evaluation also found a model-level task ceiling. A working driver and tool call are not proof that the agent can reliably complete arbitrary desktop work.

The adapter also handles a concrete MCP lifecycle failure: when the driver ends a session, the wrapper drops that stale session and reconnects the next call. This is the verified reconnect behavior behind the tool interface, not a separate universal MCP reset service.

The source record describes MCP **adapter construction, connection and driver-session recovery**, including a daemon-backed policy path. It does not establish a separate universal “MCP reset” subsystem.
