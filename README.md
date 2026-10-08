# FE-021 rubric 演示仓库

配合 `V2.1-五轮/rubric-复现分类与演示场景.md` 使用。每个场景一个分支，分支里的工作流都只在**手动触发**时运行，推送不会启动任何流水线。

在 Woodpecker 页面上「运行流水线」时选择对应分支即可。

| 场景 | 分支 |
|---|---|
| A · 谁先拿到槽位 | `a-hold` `a-hold80` `a-p0` `a-p5` `a-p9` `a-gpu` |
| B · 等待原因全景 | `b-occ` `b-main` `b-single` |
| C · 并发组名额 | `c-a` `c-b` `c-c` `c-occ` `c-early` `c-late` `c-same` `c-p1` `c-p2` |
| D · 代理失联 | `d-long` |

`lint/ok.yml`、`lint/bad.yml` 是场景 A 第 0 步配置检查用的样例（不在 `.woodpecker/` 下，不会被当作流水线）。

Agent 标签约定：`cpu-1`、`cpu-2` 为 `demo=c3,kind=cpu`，`gpu-1` 为 `demo=c3,kind=gpu`（平时不开）。
