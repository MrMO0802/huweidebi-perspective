<div align="center">

# huweidebi-perspective

**狐尾的笔式诡谲修真、心理恐怖与反套路类型创作引擎**

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-111827?style=for-the-badge)](./SKILL.md)
[![Validation](https://img.shields.io/badge/quick__validate-pass-16a34a?style=for-the-badge)](./results.tsv)
[![Corpus Safe](https://img.shields.io/badge/corpus-no%20original%20text-7c3aed?style=for-the-badge)](./references/research/01-local-corpus-profile.md)

> 恐怖不是怪物出现。恐怖是你终于明白：判断本身已经坏了。

</div>

## What This Is

`huweidebi-perspective` 是一个 Codex Skill，用来把狐尾的笔相关公开访谈、作品研讨材料，以及本地《道诡异仙》语料的结构分析，压缩成可执行的创作工作流。

它不是原文仿写器，也不是《道诡异仙》续写器。它提炼的是可迁移的创作机制：

- 双重现实：两套解释都成立，也都伤人
- 肉身接口：规则写进眼、耳、舌、脑、血肉和疼痛
- 民俗道诡：神佛道统落到材料、组织、流程和代价
- 欺骗博弈：真话、谎言和误信共同推动剧情
- 灵感库创作法：先攒素材、爆点和题材底线，再开书
- 反套路设计：不取消追读钩子，而是换一种方式让读者失去确定性

## When To Use

触发它的典型请求：

```text
用狐尾的笔式机制帮我设计一本原创诡异修仙小说
```

```text
我这章精神病院和修真世界来回切，但读起来不吓人，帮我诊断
```

```text
把这段普通玄幻打斗改得更疯更诡异
```

```text
用道诡异仙那种“双重现实”的机制，但不要套原作设定
```

## Installation

Clone into your Codex skills directory:

```bash
git clone git@github.com:MrMO0802/huweidebi-perspective.git \
  ~/.codex/skills/huweidebi-perspective
```

Or copy this repository folder into:

```text
~/.codex/skills/huweidebi-perspective
```

Codex will discover the skill from [SKILL.md](./SKILL.md).

## Core Workflow

| Task | What the skill does |
|---|---|
| 原创设定 | 输出核心裂缝、双现实框架、主角代价、阵营骗局、第一章场景骨架和风格距离检查 |
| 章节改稿 | 先诊断章节责任、双证据、身体接口、信任变化和代价落点，再动句子 |
| 恐怖增强 | 不堆“阴森/诡异/疯狂”，而是增加证据、代价和关系变化 |
| 缺少原文 | 要求用户贴文本，同时给改稿框架；不假装已经读过 |
| 作者事实问题 | 先查公开资料，区分作者自述、媒体评价和推断 |

## Design Principles

### 1. Mechanism Over Imitation

保留机制，替换表皮。原创任务中优先避开这些组合：

- 特殊病人 + 精神病院作为默认现实端
- 原作式师徒压迫结构
- 以戏法、骰子、真假游戏为核心组织
- 原作神名或近似神名
- 原作主角式能力来源
- 照搬“疯癫证明真假”的主线

### 2. Two Realities, Both Dangerous

双现实不是“哪边是真的”的竞猜。它应该是两套证据系统的互相污染：

| Layer | Example evidence |
|---|---|
| 现实 A | 档案、病历、监控、账簿、判决、家庭录像、考勤、事故调查 |
| 现实 B | 伤口、器官异常、仪式后果、旁人反应、无法解释的物件回声 |

### 3. Body As Interface

怪异不只发生在景物里。它应该改变主角的身体和选择：

```text
感知错位 -> 身体证据 -> 他人打断 -> 规则收费 -> 选择加债
```

### 4. Anti-Routine, Not Anti-Readable

反套路不是让故事失去追读回报。它只是把回报从“升级变强”转成：

- 新证据
- 新反证
- 新代价
- 新关系污染
- 新的题材底线兑现

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   └── research/
│       ├── 01-local-corpus-profile.md
│       ├── 02-conversations.md
│       ├── 04-external-views.md
│       ├── 05-decisions.md
│       ├── 06-timeline.md
│       ├── 07-fiction-technique-from-local.md
│       ├── 11-style-microfeatures-from-local.md
│       └── 12-jiangnan-comparison.md
├── results.tsv
└── test-prompts.json
```

## Research Layers

This skill was built with a multi-layer route:

| Layer | File |
|---|---|
| 本地语料结构统计 | [01-local-corpus-profile.md](./references/research/01-local-corpus-profile.md) |
| 作者公开访谈与创作自述 | [02-conversations.md](./references/research/02-conversations.md) |
| 作品研讨与外部评价 | [04-external-views.md](./references/research/04-external-views.md) |
| 创作决策与路线变化 | [05-decisions.md](./references/research/05-decisions.md) |
| 人物时间线与动态 | [06-timeline.md](./references/research/06-timeline.md) |
| 小说机制提炼 | [07-fiction-technique-from-local.md](./references/research/07-fiction-technique-from-local.md) |
| 微观风格与改稿检查 | [11-style-microfeatures-from-local.md](./references/research/11-style-microfeatures-from-local.md) |
| 与江南 skill 的结构对比 | [12-jiangnan-comparison.md](./references/research/12-jiangnan-comparison.md) |

## Evaluation

Validation and iteration records live in [results.tsv](./results.tsv).

| Mode | Score | Notes |
|---|---:|---|
| dry_run | 91 | Initial structure check |
| local_forward_test | 94 | Three prompt forward test |
| independent_subagent_test | 80 | Three independent sub-agent blind tests |
| post_independent_patch | 93 | Patched templates and safety checks |
| post_nuwa_web_research | 96 | Added public author research and Jiangnan comparison |

The repository also includes [test-prompts.json](./test-prompts.json) for repeatable forward tests.

## Safety And Copyright Boundary

This repository does **not** include the original `.azw3` book file, chapters, or long excerpts.

It stores only:

- high-level structural observations
- derived statistics
- workflow instructions
- original safety constraints
- public-source research notes

Use this skill to create original work, diagnose structure, and design distant-style mechanisms. Do not use it to produce near-verbatim passages, sequel chapters, or replacement text for copyrighted works.

## Source Highlights

Public research includes:

- 中国作家网访谈《狐尾的笔：在跌打滚撞中前行的“探索者”》
- 上观新闻专访《做过游戏代练、当过验光师，专访网文作家“狐尾的笔”：写一两百万字才算入门》
- 《道诡异仙》作品研讨会报道
- 鹰潭融媒体关于《故障乌托邦》银河奖报道
- local derived analysis from a user-provided `.azw3` file, stored only as statistics and mechanisms

## License / Usage

This is a personal Codex skill package. The skill instructions and derived analysis are intended for creative workflow assistance. Original works and trademarks mentioned belong to their respective rights holders.
