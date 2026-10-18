# Editorial Architect

An [Agent Skills](https://agentskills.io/specification)–compatible skill for the blog of a website: it interviews founders and creators to co-develop a distinctive **editorial worldview**, then translates that worldview into **evidence-based SEO/AEO** territories, topic clusters, article briefs and a living publication plan.

Its default behavior is an adaptive, **one-question-at-a-time editorial interview**, punctuated by creative hypotheses and respectful disagreements. It refuses to turn a blog into interchangeable keyword articles.

**North star:** build a blog that has something to say; make its ideas findable and usable by human readers, search engines and AI answer systems.

> **Also known as:** blog strategy skill · content strategy skill · editorial calendar generator · SEO and AEO planning · answer engine optimization (AEO) · generative engine optimization (GEO) · AI visibility · topic clusters and pillar pages · keyword research and search intent · content brief and article brief templates · Claude Code / OpenCode / Codex / Cursor Agent Skill.

## What it does

| Mode | Outcome |
| --- | --- |
| Discovery / interview | Origin, worldview, audience tensions, distinctive access |
| Creative confrontation | Alternative theses, metaphors, territories, counterpositions |
| Editorial ground | A durable `editorial-ground.md` source of truth |
| Research & discoverability | Validated search demand and AI-answer opportunities |
| Planning & production | Roadmap, article pitches, briefs, optional drafts |
| Audit & evolution | Coverage testing, revised assumptions, retired directions |

It also carries explicit anti-fabrication rules: it never invents keyword volumes, rankings, difficulty scores, competitor performance or AI-citation likelihood, and it separates **evidence** from **interpretation** from **hypothesis**.

## Install

Copy the repository into the skills directory of the harness you use, keeping `SKILL.md`, `references/` and `assets/` together under a folder named `editorial-architect`.

```sh
npx skills add marianif/editorial-architect
```

The [skills CLI](https://github.com/vercel-labs/skills) detects your installed agents, clones the repo and links the skill into each one. Useful flags:

```sh
# Install globally for Claude Code and OpenCode, non-interactive
npx skills add marianif/editorial-architect -g -a claude-code -a opencode -y

# Inspect before installing
npx skills add marianif/editorial-architect --list
```

It also works with Claude Code plugin marketplaces, Codex, Cursor, Gemini CLI, GitHub Copilot, Windsurf and [75+ other agents](https://github.com/vercel-labs/skills#supported-agents).

<details>
<summary>Manual install (no Node)</summary>

Clone the repo into the skills directory of your harness, keeping `SKILL.md`, `references/` and `assets/` together under a folder named `editorial-architect`:

```sh
git clone https://github.com/marianif/editorial-architect.git <skills-dir>/editorial-architect
```

| Harness | Typical skills directory |
| --- | --- |
| Claude Code | `~/.claude/skills/editorial-architect/` |
| OpenCode | `.opencode/skills/editorial-architect/` (project) or `~/.config/opencode/skills/editorial-architect/` |
| Codex / Cursor / other Agent Skills runtimes | that runtime's documented skills directory |

</details>

Consult your runner's documentation for skill discovery. No build step, no dependencies — the skill is Markdown instructions plus templates.

## Search terms

If you arrived here searching for any of these, this is the skill:

`agent skills` · `claude code skill` · `claude skills` · `opencode skill` · `codex skill` · `cursor skill` · `blog strategy` · `editorial strategy` · `content strategy` · `editorial calendar` · `content calendar` · `editorial ground` · `brand voice` · `tone of voice` · `storytelling framework` · `blog audit` · `seo strategy` · `aeo` · `answer engine optimization` · `geo` · `generative engine optimization` · `ai visibility` · `llm visibility` · `topic clusters` · `pillar pages` · `keyword research` · `search intent` · `topical authority` · `content brief` · `article brief` · `interview a founder`

## Suggested initial requests

- "Use Editorial Architect. Interview me to build the editorial ground for the blog of my app. Challenge generic ideas, and make unexpected proposals. Ask one question at a time."
- "Use Editorial Architect on this existing blog. Critique its editorial coherence before recommending SEO/AEO topics."
- "Given this editorial ground, create 12 distinctive article pitches with separate narrative and search hypotheses."
- "Develop a complete article brief on [topic], keeping storytelling ahead of optimization."

## Package contents

- `SKILL.md` — core instructions, modes and entry.
- `references/interview-playbook.md` — adaptive interviewing and hypothesis checks.
- `references/creative-challenge.md` — constructive disagreement and creative divergence.
- `references/seo-aeo-method.md` — research protocol and anti-fabrication rules.
- `assets/editorial-ground-template.md` — durable editorial source of truth.
- `assets/article-brief-template.md` — narrative + search briefs.
- `assets/editorial-plan-template.md` — roadmap and qualitative rubric.

## Scope

In scope: project discovery, worldview and editorial thesis, audience tensions, storytelling territories, original angles, reporting opportunities, publication standards, blog topical architecture, search intent, AI-answer questions, briefs, interlinking and editorial review.

Out of scope by default: conversion landing pages, ads, product feature pages, social copy, brand identity design, invented search statistics, guaranteed AI citations and automatic publication. Article publishing requires explicit authorization.

## Operational note

The skill is **instructions**, not a crawler, keyword database or automated publishing system. Live SEO observations require tool access. It never promises ranking or AI answer inclusion.

## License

Licensed under the [Apache License, Version 2.0](LICENSE).
