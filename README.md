# model-switch — 什么时候切 Claude / 用 GPT

> Claude Code skill:**判断该不该离开 DeepSeek+Qwen 双模型**,手动切到第三家(Claude 全家桶)或第四家(GPT),
> 以及切过去之后怎么接上。完整判据在 [`SKILL.md`](SKILL.md)。

## 装

```bash
git clone https://github.com/wzx666-source/Claude-Claude-gpt-.git ~/.claude/skills/model-switch
```

装完即生效(Claude Code 从 `~/.claude/skills/<名字>/SKILL.md` 发现 skill),不需要任何依赖 —— 这是纯文档 skill,没有脚本。

## 它管什么

| | |
|---|---|
| **四家各买什么** | 双模型买「**多样性**」,Claude 买「**天花板**」,GPT 买「**你有无**」 |
| **什么时候上 Claude** | 9 行判据表(4 行"留双模型" + 5 行"切 Claude")+ 切过去用哪档 |
| **什么时候上 GPT** | 只有它能做的 / 不该切的 / 待核 / 切之前先想的三件事 |
| **切过去之后** | 交接与回程(交接单六项)、什么照常什么会变 |

## 它不管什么

- 双模型内部怎么分工、日常怎么走 → skill **`qwen-dual-model`**
- 具体任务(作业 / PPT / 竞赛 / 科研)的流程 → `qwen-dual-model` 的 `scenarios/`

## 和姊妹仓库的关系

| 仓库 | skill | 内容 |
|---|---|---|
| **本仓库** (`Claude-Claude-gpt-`) | `model-switch` | 跨厂商判据 —— 什么时候离开双模型(纯文档) |
| [claude-skill-dsv4-Qwen3.8-](https://github.com/wzx666-source/claude-skill-dsv4-Qwen3.8-) | `qwen-dual-model` | 双模型外挂(脚本 + 四份任务剧本) |

两边互相指路:`qwen-dual-model` 的 SKILL.md 只留一行指针指向本 skill;本 skill 的「维护」一节指出双模型那一侧在哪。
