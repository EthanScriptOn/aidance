# Aidance · First-Principles AI Manga Video Workflow

This project exists for one outcome:

```text
story excerpt -> short video prompt that makes characters feel alive
```

Do not organize the workflow around film-department reports. Organize it around the smallest chain that produces a usable AI video prompt:

```text
Facts -> Drama -> Shot Chain -> Prompt -> Review
```

## Project Structure

```text
aidance/
├── script/                         source story text
├── assets/                         locked character / scene / prop references
├── knowledge/
│   ├── principles.md               core rules of the workflow
│   ├── prompt_patterns.md          reusable shot-chain patterns
│   └── model_notes.md              renderer-specific practical notes
├── output/
│   └── ep01/
│       └── prompt_cards.md         final usable prompt cards
└── .claude/agents/
    ├── fact.md                     extracts non-negotiable facts
    ├── drama.md                    extracts conflict and state change
    ├── prompt_director.md          turns state change into shots
    └── reviewer.md                 rejects dead prompts
```

## Commands

### `~fact`

Read `script/`, `assets/registry.md`, `assets/characters.md`, `assets/scenes.md`, and `assets/props.md`.

Output only a compact fact card:

```text
Excerpt:
Visible characters:
Required references:
Location:
Key props:
Start state:
End state:
Non-negotiables:
```

Facts are not a prompt. They are the guardrails.

### `~drama`

Read the fact card and source excerpt.

Output only the dramatic engine:

```text
Main desire:
Opposition:
State change:
Viewer feeling:
Behavior chain:
```

The behavior chain is mandatory. If there is no behavior chain, there is no video.

### `~prompt`

Read the fact card, drama card, and relevant `knowledge/` files.

Output a prompt card that the user can paste into Seedance or another video model:

```text
Recommended duration:
Recommended shot count:
Upload order:
Direct prompt:
```

Default for character-driven short drama:

- `5-7s`
- `6-8 shots`
- one action or reaction per shot
- explicit shot size per shot
- visible state change
- very few hard prohibitions

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
