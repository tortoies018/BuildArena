# V4 下喷式四发轨道火箭

*Codex 与人类协作完成的 BuildArena S01 稳定轨道挑战：从三次方向纠错到 51 块四发飞船*

![V4 下喷式四发轨道火箭起飞](https://raw.githubusercontent.com/tortoies018/BuildArena/main/submissions/V4-%E4%B8%8B%E5%96%B7%E5%BC%8F%E5%9B%9B%E5%8F%91%E8%BD%A8%E9%81%93%E7%81%AB%E7%AE%AD%E6%8F%90%E4%BA%A4%E5%8C%85-260905-142303/cover-560x280.jpg)

## 项目描述

本项目面向 BuildArena Construction Challenge S01「Stable Orbital」。目标是让 Agent 通过 BuildArena 2.0 MCP 构建飞船，再由人类在 Besiege 的 The Broken Beyond 环境中手动驾驶，尽可能稳定地进入并保持轨道。

最终候选 V4 是一艘沿正确竖直轴构建的 51 块四发火箭。它由双大型中央油箱、四个独立供油发动机舱、四台下置 Booster、六个反作用转向轮、四个转向推进器、十二根结构拉索以及四点着陆支撑组成。人类没有手动修改 BSG 的结构；所有几何均由 MCP 构建。人类通过自然语言、游戏截图和点火结果持续纠错，因此本项目申报 Copilot 模式。

## Track

- 赛道：**Build with Agent**
- 模式：**Copilot**
- 任务：**S01 — Stable Orbital**

选择 Copilot 的原因是：提交模型的结构全部由 BuildArena MCP 生成，未手工编辑 GUID、块类型、Transform、Scale 或连接关系；但从 V1 到 V4 的迭代中，人类提供了截图和方向纠错反馈。

## Run Summary

V4 使用两个大型燃料桶形成中央箭体。四个小型燃料舱通过支座布置在箭体下部外围，每个燃料舱底面吊装一台 Booster，使发动机本体处于燃料舱下方、喷焰朝下。四个 Grip Pad 低于发动机本体，为地面停放提供间隙。六个反作用转向轮和四个 RCS 负责偏航、俯仰和侧倾控制，十二根 Brace 加固中央箭体及发动机舱。

录屏展示了四发同步点火、竖直离地、进入太空、行星近旁飞行以及持续的手动姿态修正。提交的 Tracker 文件跟踪 Starting Block，共 5,268 个采样，采样率 10 Hz，记录时长约 526.73 秒；飞行录屏时长约 500.93 秒，即 8 分 21 秒。

当前材料尚未通过官方评分器确认完成圈数和正式得分，因此本文不填写推测值。最终成绩以官方评测和排行榜为准。

## Video

[点击查看完整 S01 飞行录屏（GitHub，8 分 21 秒）](https://github.com/tortoies018/BuildArena/blob/main/submissions/V4-%E4%B8%8B%E5%96%B7%E5%BC%8F%E5%9B%9B%E5%8F%91%E8%BD%A8%E9%81%93%E7%81%AB%E7%AE%AD%E6%8F%90%E4%BA%A4%E5%8C%85-260905-142303/flight_video.mp4)

录像为本次候选运行的完整屏幕录制，文件通过 Git LFS 保存。没有通过剪辑改变飞行结果。

## Media Gallery

### 四发同步点火起飞｜00:05

![四发同步点火起飞](https://raw.githubusercontent.com/tortoies018/BuildArena/main/submissions/V4-%E4%B8%8B%E5%96%B7%E5%BC%8F%E5%9B%9B%E5%8F%91%E8%BD%A8%E9%81%93%E7%81%AB%E7%AE%AD%E6%8F%90%E4%BA%A4%E5%8C%85-260905-142303/gallery-01-launch.jpg)

这张画面直接验证了火箭竖直姿态、四台发动机位于底部以及喷焰向下。它也是 560 × 280 封面的原始来源。

### 近月飞行｜02:30

![近月飞行](https://raw.githubusercontent.com/tortoies018/BuildArena/main/submissions/V4-%E4%B8%8B%E5%96%B7%E5%BC%8F%E5%9B%9B%E5%8F%91%E8%BD%A8%E9%81%93%E7%81%AB%E7%AE%AD%E6%8F%90%E4%BA%A4%E5%8C%85-260905-142303/gallery-02-near-moon.jpg)

飞船已经离开地面环境，轨迹线与月面共同展示了近月飞行阶段。

### 轨道路径与姿态修正｜04:00

![轨道路径与姿态修正](https://raw.githubusercontent.com/tortoies018/BuildArena/main/submissions/V4-%E4%B8%8B%E5%96%B7%E5%BC%8F%E5%9B%9B%E5%8F%91%E8%BD%A8%E9%81%93%E7%81%AB%E7%AE%AD%E6%8F%90%E4%BA%A4%E5%8C%85-260905-142303/gallery-03-orbital-path.jpg)

远景画面展示飞船、路径标记和空间环境，用于说明长时间手动控制过程。

### 月球掠过｜05:30

![月球掠过](https://raw.githubusercontent.com/tortoies018/BuildArena/main/submissions/V4-%E4%B8%8B%E5%96%B7%E5%BC%8F%E5%9B%9B%E5%8F%91%E8%BD%A8%E9%81%93%E7%81%AB%E7%AE%AD%E6%8F%90%E4%BA%A4%E5%8C%85-260905-142303/gallery-04-lunar-pass.jpg)

画面记录飞船在后半程继续沿月球附近路径飞行，没有用概念图替代真实运行截图。

## LLM / Agent Setup

- 使用的模型或模型家族：**OpenAI Codex（GPT-5 系列）**。
- 使用方式：桌面 IDE/工程 Agent，通过 BuildArena 2.0 MCP 调用构建工具，并使用本地命令完成只读检查、合法控制参数调整、打包和版本管理。
- Agent 数量：**单 Agent**，未使用多 Agent 委派。
- 是否使用视觉反馈：**是**。人类把 Besiege 截图提供给 Agent，用于识别坐标轴、火箭上下关系和喷焰方向错误。
- 人类职责：提出任务与控制约束、提供视觉纠错、选择轨迹、手动驾驶并提供最终录像。
- Agent 职责：设计几何、生成构建记录、保存 raw 模型、调整合法非几何控制字段、验证文件一致性、整理提交材料与 Writeup。

## Prompts and Workflow

### Agent system prompt

没有另外编写参赛专用的自定义 system prompt；使用 Codex 环境的标准代理规则，包括工具调用、文件安全、验证和任务持续执行要求。平台内部管理的提示不作为自定义参赛提示复制。

### Human initial prompt

> 按照赛项的要求，帮我设计一下飞船。我想设计的飞船是第一个赛道的。可以把这项写入总结文档。

### Copilot 人类指导摘要

人类在实际游戏检查后依次补充了以下要求：

1. 坐标轴错误，需要按正确竖直轴重建，并让火箭更复杂。
2. 控制方式限定为方向键和数字小键盘，并需要使用说明。
3. 赛道归档必须是平铺目录，文件名按“版本号—名称—时间”排序。
4. 火箭上下关系颠倒，需要让鼻锥在上、发动机在下。
5. 点火截图显示发动机喷焰向上，需要重新设计为向下喷焰。
6. 所有经验必须写入自包含学习文件，保证新 Agent 能独立接续。
7. 最终整理轨迹、录屏、公开视频、中文 Writeup、560 × 280 封面和媒体画廊。

### 构建流程

每次结构修改都创建新的 MCP 生命周期。Agent 在原始模型封存前请求最终机器摘要，保存有效构建记录和完整构建记录，再保存并关闭该生命周期。raw 模型完成后，仅在 tuned 副本中修改允许的非几何 `Data` 字段，包括按键、速度、阻尼和自动制动；没有改变连接器几何。

随后对 raw 与 tuned 文件执行静态比较：两者都为 51 块，GUID、块类型和全部 Transform 差异为 0，仅 14 个控制方块的合法 `Data` 不同。游戏内飞行由人类手动完成，Starting Block 轨迹由官方 Tracker 记录。

## Controls

| 按键 | 功能 |
| --- | --- |
| `↑ / ↓` | 同步启动 / 关闭四台 Booster |
| `← / →` | 偏航 |
| 数字小键盘 `8 / 2` | 俯仰 |
| 数字小键盘 `4 / 6` | 侧倾 |

反作用转向轮启用自动制动，速度为 2.0、阻尼为 1.5；转向推进器同样启用自动制动。

## Code and Tools

- BuildArena 2.0 MCP：完成全部机器几何构建并记录操作历史。
- BuildArena Block Tracker：以 Starting Block 为目标记录飞行轨迹。
- PowerShell 与 XML 检查：验证块数量、GUID、类型、Transform、合法控制字段差异、SHA-256 和 ZIP 内容。
- OpenCV 与 Pillow：从真实 MP4 读取帧，制作精确 560 × 280 封面，并导出未生成式修改的媒体画廊图片。
- Git 与 Git LFS：版本管理并公开 518 MiB 飞行录像。
- 项目仓库：[tortoies018/BuildArena](https://github.com/tortoies018/BuildArena)

## Submission Artifacts

Kaggle 官方六文件包严格包含：

1. `machine_raw.bsg`
2. `build_history.json`
3. `build_history_full.json`
4. `machine_tuned.bsg`
5. `trajectory.csv`
6. `chat_transcript.md`

录像、封面图、媒体画廊、Writeup、提交说明和 SHA-256 校验表是补充材料，不替代也不混入官方六文件 ZIP。

## Notes

- **V1：坐标轴错误。** 使用工具 `+Y` 作为竖直方向，游戏中整船横躺。
- **V2：上下关系错误。** 改用正确的 `+Z` 轴，但发动机被放在燃料箱上方。
- **V3：喷焰方向错误。** 发动机位于下部结构，但点火截图显示喷焰向上，反作用力实际向下。
- **V4：当前提交候选。** 抬高四个外围燃料舱，把 Booster 吊装到底面，并让着陆垫低于发动机本体。

最重要的工程经验，是必须分别判断构建轴、发动机物理位置、喷焰方向和火箭受力方向。MCP 返回的方向文字不能替代游戏内短点火验证。三个失败版本被完整保留，因为它们既解释了 V4 的设计来源，也让后续 Agent 能避免重复犯错。

这个项目的结果不只是一艘火箭，也是一套可复核的人机协作过程：从错误样本、构建历史、raw/tuned 一致性检查，到轨迹、录像、中文说明和自包含学习文件，所有关键决策都能够继续追踪。
