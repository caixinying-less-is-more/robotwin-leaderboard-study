# 打榜 RoboTwin · 模型研读项目

> 本项目把 RoboTwin 2.0 Leaderboard（https://robotwin-platform.github.io/leaderboard）上全部 **26 个上榜模型**拆成独立研读任务。
> **本项目已从 WorkBuddy 迁移到 GitHub，不再使用 WorkBuddy 任务面板与资产库协作。**

## 项目背景
研读每个上榜模型，拆解它凭什么刷榜（架构 / 训练方法 / 关键 trick），并为 **lingbot-vla-v2 基模**提出在该任务上的提分方法。

## 目录结构
```
.
├── README.md                      # 本文件：总表 + 说明
├── tasks/                         # 26 个任务，每个模型一个 .md
│   ├── 01-gigabrain-0.7.md
│   └── ...
└── resources/                     # 资料库
    ├── robotwin-task-brief.md     # 任务总说明
    ├── program-rules.md           # 合规约束（改进框架）
    └── lingbot-vla-flow-blog.html # 交互式架构参考图
```

## 任务总表（26 个）
| # | 模型 | 贡献者 | 设置 | easy | hard | 备注 |
|---|---|---|---|---|---|---|
| 01 | [GigaBrain-0.7](tasks/01-gigabrain-0.7.md) | GigaAI | cotrain | 66.8 | 67.92 |  |
| 02 | [π0.5](tasks/02-pi0.5.md) | RoboTwin Team | cotrain | 70.66 | 46.0 |  |
| 03 | [X-WAM](tasks/03-x-wam.md) | RoboTwin Team | cotrain | 69.98 | 25.84 |  |
| 04 | [X-VLA](tasks/04-x-vla.md) | RoboTwin Team | cotrain | 67.96 | 20.95 |  |
| 05 | [Xiaomi Robotics-0](tasks/05-xiaomi-robotics-0.md) | RoboTwin Team | cotrain | 62.86 | 18.22 |  |
| 06 | [EventVLA](tasks/06-eventvla.md) | RoboTwin Team | cotrain | 65.58 | 15.74 |  |
| 07 | [AHA-WAM](tasks/07-aha-wam.md) | RoboTwin Team | cotrain | 64.32 | 3.2 |  |
| 08 | [FastWAM](tasks/08-fastwam.md) | RoboTwin Team | cotrain | 77.76 | 1.92 |  |
| 09 | [Spatial Forcing](tasks/09-spatial-forcing.md) | RoboTwin Team | cotrain | 77.18 | 26.74 |  |
| 10 | [starVLA](tasks/10-starvla.md) | RoboTwin Team | cotrain | 46.52 | 3.16 |  |
| 11 | [Abot-M0](tasks/11-abot-m0.md) | RoboTwin Team | cotrain | 57.4 | 30.36 |  |
| 12 | [GalaxeaVLA](tasks/12-galaxeavla.md) | RoboTwin Team | cotrain | 62.72 | 12.72 |  |
| 13 | [4D-WAM](tasks/13-4d-wam.md) | OpenHelix Robotics | cotrain | 81.5 | 41.8 |  |
| 14 | [OLA-Geo](tasks/14-ola-geo.md) | OLA-HKUSTGZ | cotrain | 82.96 | 33.64 |  |
| 15 | [UniWAM](tasks/15-uniwam.md) | OLA-HKUSTGZ | cotrain | 75.12 | 67.56 |  |
| 16 | [ME-Dex-1.0](tasks/16-me-dex-1.0.md) | Li Auto Inc. | cotrain | 89.58 | 68.12 |  |
| 17 | [WorldScape Policy 2.0](tasks/17-worldscape-policy-2.0.md) | ManiFold AI | cotrain | 84.92 | 38.5 |  |
| 18 | [PatchWAM](tasks/18-patchwam.md) | PatchWAM Team | cotrain | 91.56 | 66.72 |  |
| 19 | [Discrete Forcing](tasks/19-discrete-forcing.md) | OpenHelix Team | cotrain | 59.32 | 11.2 |  |
| 20 | [ViGAR](tasks/20-vigar.md) | PKU DAGroup & AGIBOT | cotrain | 82.0 | 67.02 |  |
| 21 | [RDT](tasks/21-rdt.md) | RoboTwin Team | sft | 34.5 | 13.72 | SFT 基线 |
| 22 | [π0](tasks/22-pi0.md) | RoboTwin Team | sft | 46.42 | 16.34 | SFT 基线 |
| 23 | [ACT](tasks/23-act.md) | RoboTwin Team | sft | 29.74 | 1.74 | SFT 基线 |
| 24 | [DP](tasks/24-dp.md) | RoboTwin Team | sft | 28.04 | 0.64 | SFT 基线 |
| 25 | [DP3](tasks/25-dp3.md) | RoboTwin Team | sft | 55.24 | 4.96 | SFT 基线 |
| 26 | [CloudRobo-WM](tasks/26-cloudrobo-wm.md) | CloudRobo Team | cotrain | 88.9 | 75.0 | 🔴 最高优先级 |

## 如何认领任务
1. 在 `tasks/` 下找到你想研读的模型文件。
2. 把文件顶部「状态」从 `🟡 待认领` 改为 `🟢 进行中（认领人：你的 GitHub 名）`。
3. 提交一个 PR（分支名随意，如 `claim/<模型slug>`）。
4. **可重复认领**：别人选过的你也能选，鼓励多人独立研读、交叉对比。

## 如何提交（改进思路 / 代码）
- 改进提交统一走 GitHub（不再用 WorkBuddy 资产库）：
  - Fork `caixinying-less-is-more/harnessx-robotwin-vla`
  - 新建分支 `feat/<模型名>`，push 你的改进
  - 开 PR，并在 PR 描述里注明对应任务编号
- ⚠️ **提交前先查重**：确保思路不与 `harnessx-robotwin-vla` 已有实验重复。

## 交付物要求
1. 交互式架构图（参考 `resources/lingbot-vla-flow-blog.html`，可简化）
2. 用自己的话清晰讲解（800 字以内）
3. lingbot-vla-v2 基模提分方法（查重后提交到上述仓库）
4. 论文 / 主页链接

## 合规约束
详见 `resources/program-rules.md`：单一权重、仅用 clean 演示、BC 框架内、可用冻结公开感知教师等。

## 截止
**2026-10-21 18:00（北京时间）**
