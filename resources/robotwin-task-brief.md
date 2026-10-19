> ⚠️ 本文档写于 WorkBuddy 协作时期，其中「提交到 workbuddy 资产库」现已废弃：本项目已迁移到 GitHub，改进请提交到 `caixinying-less-is-more/harnessx-robotwin-vla`（见仓库根目录 README「如何提交」）。

# 打榜 RoboTwin · 研读任务总说明（项目资料）

> 本文件是「打榜 RoboTwin」系列任务的统一说明。每个上榜模型对应一条独立任务，成员可重复认领。  
> 榜单来源：RoboTwin 2.0 Leaderboard（<https://robotwin-platform.github.io/leaderboard>），共 26 个上榜模型。

## 一、任务目标

研读某个 RoboTwin 2.0 榜单模型，**搞清楚它凭什么刷榜**：

1. 用了什么**架构**（骨干、是否 VLA / diffusion policy / 强化学习 / 其他范式）；
2. 用了什么**训练方法**（数据、损失、训练策略、cotrain 还是单任务 SFT）；
3. 用了什么**关键 trick** 提升榜单分数。

## 二、交付物（必须包含）

1. **架构图**：交互式风格（参考本项目资料 `lingbot-vla-flow-blog.html`，即原版交互架构参考图）。注意：原版较复杂，你们做任务时**不必画得那么复杂**，可在其基础上简化，但请保持类似交互式风格（可拖拽 / 点击看详情更佳，至少要是清晰的架构示意图）。
2. **用自己的话清晰讲解**该模型原理与刷榜点（800字以内）。
3. **「lingbot-vla-v2 基模在这个任务上提升分数」的方法与设计思路**：
   - **不能和仓库里已有实验重复**——提交前先去 **<https://github.com/caixinying-less-is-more/harnessx-robotwin-vla.git>** 查重
   - 改进思路与代码请提交到 workbuddy 资产库

## 三、合规约束（改进思路必须落在此框架内）

详细见本项目资料 program-rules.md，改进范围：

- **单一权重**：推理不按任务路由、不集成多模型。
- **仅用 clean 演示**：randomized 只能测、不能训；禁外部数据。
- **BC 框架内**：禁在线 RL / DAgger / 环境打分筛选 / 世界模型 RL 等。
- 允许：像素级增广、轨迹过滤、公开冻结感知教师作辅助监督、训练/推理策略调优、LoRA 合并回基座。

## 四、参考资源

| 资源                                                                     | 说明                                                |
| ---------------------------------------------------------------------- | ------------------------------------------------- |
| `lingbot-vla-flow-blog.html`                                           | 交互架构参考图（可拖拽/缩放/点击）。                               |
| `program-rules.md`                                                     | 改进思路的合规边界                                         |
| <https://github.com/caixinying-less-is-more/harnessx-robotwin-vla.git> | 团队仓库：已有实验查重参考（**提交请走 workbuddy 资产库**）          |
| 本项目盘「RoboTwin打榜研读」文件夹                                        | 改进思路与代码的最终提交处（直接在此文件夹内提交/更新）                  |
| <https://robotwin-platform.github.io/leaderboard>                      | 榜单本身（含各模型成绩：clean2clean easy / clean2random hard） |

## 五、认领与截止

- **截止时间：2026-10-21 18:00（北京时间）**。
- **可重复认领**：别人选过的模型你也能选，鼓励多人独立研读、交叉对比。
