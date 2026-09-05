# Build Transcript — S01 V4 Downward-Exhaust Orbital Rocket

This is a faithful, condensed public transcript of the human/agent build process. Verbose MCP face listings and machine-generated payloads are omitted because the complete operations are preserved in `build_history.json` and `build_history_full.json`. No hidden platform instructions are reproduced.

## Human requests and visual feedback

1. Initial request:

   > 按照赛项的要求，帮我设计一下飞船我想设计的飞船是第一个赛道的。可以把这项写入总结文档。

2. First correction after testing A1:

   > 坐标轴错了。可以设计更复杂的火箭。我希望火箭的控制方式也是方向键和小键盘数字键，设计完要有使用说明。

   The human supplied an in-game screenshot showing A1 lying horizontally.

3. Archive and orientation requirements:

   > 飞船的上下反了。文件夹的命名应该是先版本号，然后才是名字，最后才是时间，应该是先有这个赛道的文件夹。然后直接放置不同的模型就可以了，不要再套一个文件夹。注意更新学习文件，将这些内容都写在学习文件里面。使得只要开一个新的绘画机器，看到学习文件就可以自己继续工作下去。

   The human supplied an in-game screenshot showing V2 upright but with the Booster cluster at the top.

4. Engine-direction correction after testing V3:

   > 发动机的方向反了。

   The human supplied an ignition screenshot showing all four V3 exhaust plumes pointing upward. The agent therefore treated the real exhaust direction—not the MCP wording—as decisive and created V4 with the Booster blocks attached below the raised fuel pods.

5. Post-build submission questions:

   > 这个游戏的任务目标是什么

   > 要提交什么材料。

   > 怎么导出轨迹csv。

   > 应该就是这一份，将打包文件整理起来。

## Agent build progression

### V1 — Orbital Dart

- Built along tool `+Y`.
- 17 blocks.
- Rejected after the game screenshot showed the rocket lying horizontally.
- Lesson: tool `+Z` is the game vertical axis.

### V2 — Orbital Lancer

- Rebuilt along tool `+Z` with two large tanks, four landing arms, paired reaction wheels, RCS and braces.
- 39 blocks.
- Rejected after the screenshot showed the Booster cluster physically above the tanks.
- Lesson: an upright machine can still have its top and bottom reversed.

### V3 — Bottom Quad Orbital Rocket

- Put four Booster blocks around the lower structure.
- 47 blocks.
- MCP described their direction as `straight up`.
- Rejected after ignition showed the visible exhaust plumes pointing upward, implying a downward reaction force.
- Lesson: MCP direction wording cannot replace an in-game ignition check.

### V4 — Downward-Exhaust Orbital Rocket

- MCP lifespan: `V4_Downward_Exhaust_Orbital_Rocket_260905_131830`.
- Built along tool `+Z`.
- Four outboard fuel pods were raised on Single Wooden Block supports.
- Four Booster blocks were attached to the downward faces of those pods, below the pods, with MCP direction `straight down`.
- Four Grip Pads were kept below the engine bodies for landing clearance.
- Final machine: 51 blocks.
- Final MCP summary was requested before save and close.
- No manual BSG geometry editing was performed.

## Legal post-build tuning

The tuned BSG retains the same 51 block GUIDs, block types, transforms, scales and connector geometry as the raw MCP BSG. Only legal non-geometry `Data` fields were changed on 14 control blocks:

- Four Booster blocks: `UpArrow` start, `DownArrow` stop.
- Two vertical-axis reaction wheels: `LeftArrow` / `RightArrow` yaw.
- East/west reaction wheels and RCS: numeric keypad `8` / `2` pitch.
- North/south reaction wheels and RCS: numeric keypad `4` / `6` roll.
- Reaction wheels and RCS use automatic braking.

## Selected tracked run

- Original tracker file: `V4_Downward_Exhaust_Orbital_Rocket_260905_131830__20260905_055126.csv`.
- Tracker target: Starting Block GUID `54b24045-e039-40ee-9ba6-824dbdc42f9e`.
- Sample rate: 10 Hz.
- Samples: 5268 (`sample_index` 0 through 5267).
- Recorded duration: approximately 526.73 seconds.
- Packaged submission name: `trajectory.csv`.

## Track disclosure

Recommended disclosure: `Build with Agent / Copilot`. The structure of every submitted raw version was generated through BuildArena MCP and V4 itself was completed without manual geometry editing, but human screenshots and corrections were used between iterations. Copilot is the conservative classification for the complete iterative workflow.

## Submission Finalization

The human then asked to add the screen recording to the submission materials, publish it to the remote GitHub repository as the video URL, and prepare a writeup.

The agent preserved the official six-file archive as an exact six-file package and added the recording separately as `flight_video.mp4`. The recording is 543,618,999 bytes and 8 minutes 21 seconds long. Because it exceeds GitHub's normal 100 MiB file limit, it is tracked with Git LFS. The agent also replaced the draft with a submission-ready Kaggle writeup, added the public GitHub video link, updated checksums and submission notes, and kept the learning file self-contained.

## Chinese Writeup and Media Finalization

The human clarified that the Kaggle writeup could be in Chinese and requested every Kaggle-facing field: Basic Details such as Title and Subtitle, a required 560 by 280 cover image, a Media Gallery using MCP screenshots or video frames, a project description, and all remaining writeup sections.

The agent checked the current competition page and retained its required section structure. Because no suitable still images were already archived, the agent decoded the real 2048 by 1152 flight recording, reviewed a timestamped contact sheet, and selected frames at 00:05, 02:30, 04:00, and 05:30. The 00:05 launch frame was center-cropped and resized to exactly 560 by 280 for the cover. Four original-resolution frames were saved for the Media Gallery. No generative image modification was used. A Chinese writeup and a separate Kaggle field-by-field copy sheet were then created to match the actual V4 files, trajectory, controls, video, workflow, and validation results.
