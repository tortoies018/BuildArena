# V4 Downward-Exhaust Orbital Rocket

## Track

- Build with Agent
- Recommended mode: Copilot

The machine geometry was generated through the BuildArena 2.0 MCP. No BSG geometry was manually edited. Human visual feedback was used between successive MCP-built versions, so Copilot is the conservative disclosure for the complete workflow.

## Run Summary

V4 is a four-engine orbital rocket for Mission S01: Stable Orbital. It uses two large central fuel tanks, four independently fed outboard engine pods, four landing feet, paired three-axis reaction wheels, four RCS units and twelve braces.

The selected Tracker run contains 5268 samples at 10 Hz over approximately 526.73 seconds. Before publishing, add the observed number of completed orbital periods and a short description of the final flight result here.

## Video

TODO: Add a YouTube or other public video link showing the submitted run.

## LLM / Agent Setup

- LLM or model family used: OpenAI Codex agent environment
- How it was used: desktop coding/engineering agent with BuildArena 2.0 MCP tools
- Single-agent or multi-agent: single-agent
- Visual feedback used: yes, through screenshots supplied by the human between versions

## Prompts and Workflow

- Custom user-defined system prompt: none; the standard Codex agent environment was used.
- Human initial prompt: design a spacecraft for the first Construction Challenge track and record the work in a summary document.
- Human constraints added during iteration: use the correct vertical axis, make the rocket more complex, use arrow keys and numeric keypad controls, keep a flat per-track archive, maintain a self-contained learning file, correct the rocket top/bottom relationship, and correct the engine exhaust direction.
- Workflow: the agent created a new MCP lifespan for every structural revision, requested a final machine summary, saved and closed the raw build, then produced a separate tuned copy by changing only legal non-geometry control Data.

## Code and Tools

- BuildArena 2.0 MCP for all machine geometry.
- BuildArena Block Tracker for the Starting Block trajectory.
- PowerShell/XML checks for block identity, transform equality, control-only Data changes and SHA-256 packaging verification.
- Repository/code sharing: optional; add a public link here if desired.

## Notes

The build produced three useful failures before V4:

- V1 used tool `+Y` as vertical and appeared horizontal in game.
- V2 used the correct `+Z` axis but placed its engines at the top of the rocket.
- V3 moved the engines to the lower structure, but an ignition screenshot showed the exhaust plumes pointing upward.

V4 raises four fuel pods on supports and hangs each Booster below its pod so the exhaust is intended to point downward. The complete learning trail was preserved rather than hiding the failed designs.
