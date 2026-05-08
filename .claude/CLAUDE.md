# Aidance · First-Principles AI Manga Video Workflow

This project exists for one outcome:

```text
剧情片段 -> 让人物活起来的短视频提示词
```

Default output language is Chinese. Keep only unavoidable model / UI terms in English, such as `Seedance`, `image-to-video`, `Shot`, or `9:16`.

Do not organize the workflow around film-department reports. Organize it around two first-principles problems:

```text
多集连续性：人物、道具、场景不能乱
单条可生成性：每个视频片段必须有人物状态变化和镜头行为链
```

So the full production line is:

```text
全系列资产库 -> 本集资产清单 -> 本集戏剧脊柱 -> 片段提示词卡 -> 实测反馈回写
```

## Project Structure

```text
aidance/
├── script/                         source story text
├── assets/                         locked character / scene / prop references
├── knowledge/
│   ├── principles.md               core rules of the workflow
│   ├── asset_generation.md         asset generation rules
│   ├── prompt_patterns.md          reusable shot-chain patterns
│   └── model_notes.md              renderer-specific practical notes
├── templates/                       reusable output templates
├── output/
│   └── ep01/
│       ├── asset_manifest.md       per-episode asset use and new asset needs
│       ├── episode_spine.md        per-episode clip list and state changes
│       ├── prompt_cards.md         final usable prompt cards
│       └── test_notes.md           generation results and reusable lessons
└── .claude/agents/
    ├── manifest.md                builds per-episode asset manifests
    ├── spine.md                   builds per-episode dramatic spines
    ├── fact.md                     extracts non-negotiable facts
    ├── drama.md                    extracts conflict and state change
    ├── prompt_director.md          turns state change into shots
    └── reviewer.md                 rejects dead prompts
```

## Commands

### `~episode`

Start a new episode from a script file.

Read `assets/registry.md`, `assets/characters.md`, `assets/scenes.md`, `assets/props.md`, and the selected script.

Create these files under `output/epXX/`:

```text
asset_manifest.md
asset_regen_plan.md（如需要重跑资产）
episode_spine.md
prompt_cards.md
test_notes.md
```

Rules:

- Do not generate video prompts before the asset manifest is clear.
- Do not invent new asset appearances inside video prompts.
- If a new character, prop, scene, or state variant is needed, record it in `asset_manifest.md` first.
- If assets need to be regenerated, create `asset_regen_plan.md` before prompt generation.
- If a clip has no state change, merge it with a neighboring clip or drop it.

### `~manifest`

Create or update the episode asset manifest.

Output:

```text
复用资产：
新增资产需求：
变体需求：
本集关键道具归属变化：
暂不进入视频生成的问题：
```

### `~spine`

Create or update the episode spine.

Output:

```text
Clip 编号：
原文范围：
片段名：
状态变化：
核心行为链：
建议时长：
建议镜头数：
```

### `~fact`

Read `script/`, `assets/registry.md`, `assets/characters.md`, `assets/scenes.md`, and `assets/props.md`.

Output only a compact fact card:

```text
原文范围：
可见人物：
需要参考图：
地点：
关键道具：
开始状态：
结束状态：
不可错事实：
```

Facts are not a prompt. They are the guardrails.

Write the fact card in Chinese.

### `~drama`

Read the fact card and source excerpt.

Output only the dramatic engine:

```text
主要欲望：
阻力：
状态变化：
观众感受：
行为链：
```

The behavior chain is mandatory. If there is no behavior chain, there is no video.

Write the drama card in Chinese.

### `~prompt`

Read the fact card, drama card, and relevant `knowledge/` files.

Output a prompt card that the user can paste into Seedance or another video model:

```text
建议时长：
建议镜头数：
上传顺序：
直贴提示词：
```

Default for character-driven short drama:

- `5-7s`
- `6-8 shots`
- one action or reaction per shot
- explicit shot size per shot
- visible state change
- very few hard prohibitions

Write the final prompt card in Chinese by default.

### `~notes`

After testing generated videos, update `test_notes.md`.

Promote only reusable lessons into `knowledge/model_notes.md` or `knowledge/prompt_patterns.md`.

Output:

```text
Clip：
结果：好 / 可用但需修 / 失败
有效原因：
失败原因：
下一版修正：
是否回写知识库：
```

### `~review`

Read the final prompt only. Do not admire it. Try to reject it.

Reject the prompt if:

- it describes a situation but not a behavior chain
- it uses fewer than 5 shots for a fast emotional beat
- it has no clear state change
- it puts too many facts and prohibitions into every shot
- visible characters lack uploaded references
- the last shot does not land on a changed relationship

## Important Principle

The final prompt is not a summary of all upstream work.

The final prompt is a directed performance instruction:

```text
stimulus -> reaction -> pressure -> changed state -> relationship landing
```

When in doubt, delete theory and write behavior.
