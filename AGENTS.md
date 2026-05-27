# AGENTS.md

Guidelines for AI agents working with Earned Media Skills by 701am.

## Repository Overview

This repository contains **Agent Skills** for earned media, PR, and journalist outreach — built for AI agents using Claude Code, Claude Cowork, or any agent that supports the Agent Skills format.

- **Name**: Earned Media Skills
- **Publisher**: 701am
- **GitHub**: 701am/earned-media-skills
- **License**: MIT

## Repository Structure

```
earned-media-skills/
├── skills/                        # All skill definitions
│   ├── client-context/            # Foundation — read by every other skill
│   │   └── SKILL.md
│   ├── pitch-writer/
│   │   └── SKILL.md
│   └── ...                        # 28 skills total
├── memory/                        # Optional Obsidian vault templates
│   ├── README.md
│   ├── walter-code/               # Per-client memory files
│   └── portfolio/                 # Portfolio manager vault
├── AGENTS.md                      # This file
├── CLAUDE.md                      # Symlink → AGENTS.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## How Skills Work

Skills are plain markdown files. Your agent reads them and follows the instructions.
No special runtime, no DSL, no framework. Just Claude and markdown.

Each skill has:
- A `name` and `description` in YAML frontmatter (for skill discovery)
- Instructions written in plain English
- A **Related Skills** section showing what connects to what

## The Foundation Skill

**`client-context`** is the foundation. Every other skill reads it first.

It holds everything about the client: their business, voice, story, products, angles,
competitors, and journalist relationships. Without it, every skill works generically.
With it, every skill works specifically for that client.

Run `client-context` first. Everything else compounds from there.

## Memory (Optional)

The `memory/` folder contains Obsidian vault templates for persistent memory across sessions.

- **Without memory**: Skills work in a single session. No persistence between sessions.
- **With memory**: Client context, contacts, campaigns, and placements persist in markdown files. The agent reads and updates them automatically.

See `memory/README.md` for setup.

## Skill Categories

| Category | Skills |
|---|---|
| Foundation | client-context, intake |
| Strategy | earned-media-strategy, editorial-calendar, competitive-intelligence |
| Research | journalist-research, data-researcher |
| Campaign | digital-pr-ideation, visual-gap-hunter, seo-pr |
| Outreach | pitch-writer, press-release, newsjacking |
| Quality | humanizer |
| Relationships | infinite-follow-up, influencer-mapper, tiktok-influencer |
| Content | thought-leadership, podcast-placements, speaking-events, media-training |
| Links | link-reclamation |
| Defense | crisis-comms, monitor |
| Recognition | award-submissions |
| Measurement | roi-measurement, client-reporting |
| Portfolio | portfolio-manager |

## Writing Style for Skills

- Direct and instructional
- Second person ("You are an earned media specialist")
- Specific over vague — name exact outputs, not general guidance
- Under 500 lines per SKILL.md

## The Soul Rule

Every skill that produces external output must pass one question before finishing:

**Would a journalist feel respected receiving this?**

If the answer is no — the pitch inflates, the press release is promotional, the follow-up is generic — say so and offer to fix it. The system earns placements by being honest and specific, not by producing more output faster.
