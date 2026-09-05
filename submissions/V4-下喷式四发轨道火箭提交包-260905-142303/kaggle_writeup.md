# V4 Downward-Exhaust Four-Engine Orbital Rocket

## Track

- Competition track: **Build with Agent**
- Collaboration mode: **Copilot**
- Mission: **S01 — Stable Orbital**

All submitted machine geometry was generated through the BuildArena 2.0 MCP workflow. I did not manually edit block GUIDs, types, transforms, scales, or connections in the BSG. Human screenshots and corrections guided the revisions between versions, so Copilot is the appropriate disclosure for the end-to-end process.

## Run Summary

V4 is a 51-block, four-engine vertical rocket. Its central stack uses two large fuel barrels. Four independently fed outboard fuel pods are raised on supports, with one Booster suspended under each pod so the engine bodies and visible exhaust are on the bottom side of the vehicle. Four Grip Pads provide ground clearance. Six reaction steering blocks and four steering thrusters provide three-axis attitude control, while twelve braces reinforce the central stack and engine pods.

The submitted Tracker file targets the Starting Block and contains 5,268 samples at 10 Hz, covering approximately 526.73 seconds. The accompanying screen recording is 8 minutes 21 seconds long. This writeup intentionally does not claim an unaudited orbit count or score; the official evaluator and leaderboard result should be treated as authoritative.

## Video

- [Full S01 flight screen recording (GitHub, 8:21)](https://github.com/tortoies018/BuildArena/blob/main/submissions/V4-%E4%B8%8B%E5%96%B7%E5%BC%8F%E5%9B%9B%E5%8F%91%E8%BD%A8%E9%81%93%E7%81%AB%E7%AE%AD%E6%8F%90%E4%BA%A4%E5%8C%85-260905-142303/flight_video.mp4)
- The MP4 is stored with Git LFS; the GitHub page provides access to the original recording.

## LLM / Agent Setup

- Model environment: OpenAI Codex (GPT-5 family).
- Agent configuration: one coding/engineering agent; no multi-agent delegation.
- Construction interface: BuildArena 2.0 MCP lifecycle and block-placement tools.
- Human role: supplied the mission, control constraints, in-game screenshots, engine-direction corrections, the selected Tracker run, and the final flight recording.
- Agent role: designed each geometry revision, generated the raw build history, tuned legal control fields, validated the artifacts, assembled the submission package, and published the supporting repository.

## Prompts and Workflow

The initial Chinese prompt asked for a spacecraft for the first Construction Challenge course and requested that the work be recorded in a reusable summary. During testing, the human added these constraints and corrections:

1. Correct the coordinate axis and make the rocket more complex.
2. Use only the arrow keys and numeric keypad for flight control.
3. Keep each course in one flat archive folder, with filenames ordered as version, name, then timestamp.
4. Correct the rocket's top/bottom relationship.
5. Correct the engine orientation after an ignition screenshot showed exhaust firing upward.
6. Preserve a self-contained learning file so a fresh agent can resume without the old chat.

Every structural revision used a new MCP lifecycle. Before saving a raw machine, the agent requested a final machine summary, saved both filtered and complete build histories, and closed the lifecycle. The tuned BSG was then produced by changing only permitted non-geometry `Data` fields. A structural comparison confirmed zero differences in block identity and transforms between raw and tuned files.

## Controls

| Key | Function |
| --- | --- |
| Up Arrow / Down Arrow | Start / stop all four Boosters |
| Left Arrow / Right Arrow | Yaw |
| Numeric keypad 8 / 2 | Pitch |
| Numeric keypad 4 / 6 | Roll |

The reaction steering blocks use automatic braking with speed 2.0 and damper 1.5. Steering thrusters also use automatic braking.

## Code and Tools

- BuildArena 2.0 MCP for all machine geometry and construction history.
- BuildArena Block Tracker for the Starting Block trajectory.
- PowerShell and XML validation for block counts, GUID/type identity, transform equality, legal control-only tuning, archive contents, and SHA-256 checksums.
- Git and Git LFS for reproducible public delivery of the source artifacts and the 518 MiB screen recording.
- Public repository: [tortoies018/BuildArena](https://github.com/tortoies018/BuildArena)

## Iteration Notes

- **V1:** built along tool `+Y` and appeared horizontal in game.
- **V2:** used the correct `+Z` vertical axis, but placed the Booster cluster above the fuel tanks.
- **V3:** moved the Boosters to the lower structure, but an ignition screenshot showed the exhaust plumes pointing upward.
- **V4:** raised the four outboard fuel pods and hung each Booster from the pod's lower face, with landing pads below the engine bodies. This is the submitted candidate.

The failed versions were retained as engineering evidence. The central lesson was to distinguish construction axis, engine location, exhaust direction, and reaction-force direction, and to validate the final interpretation with an in-game ignition test rather than relying on coordinate labels alone.

## Submission Artifacts

The official submission archive contains exactly these six required files: `machine_raw.bsg`, `build_history.json`, `build_history_full.json`, `machine_tuned.bsg`, `trajectory.csv`, and `chat_transcript.md`. The video, this writeup, submission notes, and checksums are supplemental evidence and are not inserted into the official six-file ZIP.
