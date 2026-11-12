# FE-021 rubric 演示仓库（二期）

配合 `V3-二期/rubric-二期-复现分类与演示场景.md` 使用。每个演示场景一个或几个分支，分支里的工作流只在**手动触发**时运行，推送不会触发任何流水线。在 Woodpecker 页面上「运行流水线」时选择对应分支即可。

| 场景 | 分支 |
|---|---|
| A · 紧急度与 30 秒 | `p2-a-bad` `p2-a-hold` `p2-a-p0` `p2-a-p0b` `p2-a-p5` `p2-a-p9` `p2-a-hold80` `p2-a-dep` `p2-a-early` `p2-a-hold25` |
| B · 仓库轮流 | `p2-b-hold` `p2-b-x` `p2-b-x7`（另一个仓库 `FE021-rubric-demo-b` 的 `p2-b-y` `p2-b-y2`） |
| C · 没有机器能跑它与 2 分钟结束 | `p2-c-long` `p2-c-gpu` |
| D · 等待原因全景 | `p2-d-occ` `p2-d-main` |
| E · 并发组 | `p2-e-a` `p2-e-a2` `p2-e-b` `p2-e-occ` `p2-e-early` `p2-e-late` `p2-e-same` |
| F · 机器掉线 | `p2-f-long` |
| B-1023 / E-1027 的页面复现 | `p2-b23-hold` `p2-b23-a1` `p2-b23-a2` `p2-b23-x` `p2-b23-y` `p2-b23-same`（另有 `FE021-rubric-demo-b` 的 `p2-b23-b1`、`FE021-rubric-demo-c` 的 `p2-b23-c1`） |

Agent 标签约定：`cpu-1`、`cpu-2`、`cpu-3` 为 `demo=c3,kind=cpu`，`gpu-1` 为 `demo=c3,kind=gpu`；每台一个槽位。
