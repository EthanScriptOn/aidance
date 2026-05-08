# Principles

## First Principle

The workflow exists to create a video prompt that produces living characters.

Professional film knowledge is useful only when it becomes visible behavior on screen.

For a multi-episode series, the workflow must solve only two core problems:

```text
1. 连续性：人物、道具、场景和状态不能乱
2. 可生成性：每个短视频片段必须有清楚的人物状态变化
```

Everything else is supporting material.

## Multi-Episode Production Line

Every episode should follow this path:

```text
script/epXX
-> output/epXX/asset_manifest.md
-> output/epXX/episode_spine.md
-> output/epXX/prompt_cards.md
-> output/epXX/test_notes.md
-> knowledge updates only when a lesson is reusable
```

### Asset Manifest

The manifest answers:

- Which locked assets are reused?
- Which new assets are needed?
- Which variants are needed?
- Which props change ownership or state?
- Which asset questions block video generation?

It is not a prompt.

### Episode Spine

The spine answers:

- Which clips should this episode become?
- What state change does each clip carry?
- What behavior chain makes each clip playable?
- How long and how many shots should each clip use?

It is not a prompt.

### Prompt Cards

Prompt cards answer:

- What images should the user upload?
- What duration and shot count should be used?
- What exactly happens in each shot?
- What minimal restrictions prevent the model from going wrong?

### Test Notes

Test notes answer:

- Which generated clips worked?
- Why did they work?
- Which clips failed?
- What should change in the next prompt?
- Is this lesson episode-specific or reusable?

Only reusable lessons should be promoted into `knowledge/`.

## The Core Chain

Every usable clip needs:

```text
who wants what -> who blocks it -> what changes -> how the camera shows the change
```

If a scene cannot be expressed as a state change, it should not become a standalone clip.

## Facts Are Guardrails

Facts prevent wrong output. They do not create drama.

Use facts to lock:

- visible characters
- required reference images
- location
- key props
- start state
- end state
- a few non-negotiables

Do not dump all facts into the prompt.

## Drama Is Behavior

Drama must become a behavior chain:

```text
stimulus -> reaction -> pressure -> changed state -> relationship landing
```

Good behavior nodes are visible:

- steps forward
- looks away
- grips rope
- blocks with pipe
- grabs ear
- shoulders shrink
- asks for help with eyes
- no one helps

Weak behavior nodes are abstract:

- feels tense
- atmosphere becomes oppressive
- relationship is complicated

## Prompt Is Direction

The final prompt should sound like a director calling action.

It should contain:

- upload order
- duration
- shot count
- shot size per shot
- one behavior per shot
- lighting summary
- performance summary
- minimal prohibitions

It should not contain:

- long theory
- department reports
- every upstream constraint
- repeated must/forbidden clauses
- vague cinematic adjectives without action

## Default Character-Drama Recipe

Use this when the scene is a short emotional / conflict beat:

```text
6 seconds
7 shots
one behavior per shot
master -> close-up -> reaction -> action close-up -> reaction -> relationship landing
```

This is the current default because testing showed it makes characters feel more alive than 2-3 longer fact-heavy shots.
