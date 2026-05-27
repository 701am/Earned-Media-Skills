# Earned Media Skills
**AI agent skills for PR, journalist outreach, and earned media. By 701am.**

28 skills covering the full earned media workflow — from building client context to pitching journalists, managing follow-ups, monitoring the news cycle, and delivering client reports. Works with Claude Code, Claude Cowork, and any agent that supports the Agent Skills format.

---

## What this is

Earned Media Skills gives AI agents the specialized knowledge to run a real earned media program. Each skill is a markdown file with plain-English instructions. Your agent reads the skill and follows it — no framework, no runtime, no setup beyond cloning the repo.

The skills cover everything: building a client's pitch angle library, researching the right journalist for a story, writing the pitch, managing the follow-up sequence, monitoring breaking news for newsjacking opportunities, measuring placements, and delivering client reports. There is also a portfolio manager skill for agencies running multiple clients — it scans across all clients and surfaces journalist conflicts, angle patterns, and accounts that need attention.

The system is built on one principle: **earned media is earned, not manufactured.** Every skill is designed to produce output a journalist would actually want to receive. The humanizer skill runs on every outreach output and strips AI writing patterns before anything goes out.

---

## How it works

### Skills are plain markdown

Each skill is a folder with a SKILL.md file inside. Your agent reads the file and follows the instructions. There is no special syntax, no execution language, no interpreter. Just Claude and markdown.

```
skills/
  pitch-writer/
    SKILL.md        ← instructions for writing journalist pitches
  humanizer/
    SKILL.md        ← strips AI writing patterns from any output
  monitor/
    SKILL.md        ← scans for coverage and pitchable opportunities
  ...
```

### Client context is the foundation

The client-context skill is read by every other skill before doing anything. It holds everything about the client: their business, voice, story, products, angles, competitors, and journalist relationships. Without it, skills work generically. With it, every pitch sounds like the client wrote it, every angle is grounded in something real, and nothing repeats what has already been tried.

Run intake once per client to build the context file from conversation. Every skill compounds from there.

### The quality gate

Two things happen before any output reaches a journalist.

**Soul check** — every output must answer yes to three questions: Is it true? Is it useful to the journalist? Would the client stand behind it without us in the room?

**Humanizer** — 24 AI writing pattern categories stripped from every outreach output. The result should sound like this specific human wrote it, not like cleaned-up AI prose.

---

## Getting started

### Installation

Clone and copy:
```bash
git clone https://github.com/701am/earned-media-skills.git
cp -r earned-media-skills/skills/* .agents/skills/
```

Or as a submodule:
```bash
git submodule add https://github.com/701am/earned-media-skills.git .agents/earned-media-skills
```

Or clone anywhere and open Claude Code from that folder — skills work as long as Claude can read the files.

### First session

Run intake first:
```
"Run the intake skill to build my client context"
```

Intake asks questions about the client one at a time — business, voice, story, products, angles, competitors. It builds the context file every other skill reads. Take time here. The quality of every pitch and strategy for the next year depends on what gets captured.

After intake, run whatever is most pressing:
```
"Write a pitch for our founder-story angle to TechCrunch"
"What should we pitch this week?"
"A story just broke about AI funding — let's newsjack it"
"Write the monthly client report"
"Prep me for my interview with Sarah Chen at Forbes"
```

---

## The 28 skills

| Skill | What it does |
|---|---|
| `client-context` | Foundation. Holds everything about the client. Read by every other skill. |
| `intake` | Builds client context from conversation. Run once per client. |
| `earned-media-strategy` | Full earned media strategy — where to play, what to lead with, what cadence to run. |
| `editorial-calendar` | 30-day pitch and content calendar. |
| `competitive-intelligence` | Maps competitor earned media landscape. Surfaces unclaimed angles. |
| `journalist-research` | Deep research on journalists by beat and outlet. Builds contact records. |
| `data-researcher` | Mines public datasets for original story angles and data study foundations. |
| `digital-pr-ideation` | Generates original data study campaign concepts — headline, hook stat, methodology. |
| `visual-gap-hunter` | Finds editorial opportunities where visual content is missing. Identifies unlinked mentions. |
| `seo-pr` | Integrates earned media strategy with SEO. Targets high-DA placements. |
| `pitch-writer` | Writes journalist pitches grounded in real angles. Humanizer runs automatically. |
| `press-release` | Writes press releases as news stories for journalists, not promotional documents. |
| `newsjacking` | Rapid-response pitching to breaking news. Hot opportunities close within hours. |
| `humanizer` | Strips AI writing patterns. 24 categories. Runs on every outreach output. |
| `infinite-follow-up` | Manages the full follow-up sequence. Knows when to bump, pivot, or move on. |
| `influencer-mapper` | Maps influencer landscape by ICP fit — newsletters, podcasts, creators, communities. |
| `tiktok-influencer` | Writes TikTok creator DM pitches in the creator's register, not PR speak. |
| `thought-leadership` | Op-eds, bylines, contributed articles. Positions the founder as category expert. |
| `podcast-placements` | Identifies podcast shows by audience fit, writes guest pitches. |
| `speaking-events` | Identifies conference opportunities, writes abstracts and bios. |
| `media-training` | Interview prep — likely questions, recommended answers, what not to say. |
| `link-reclamation` | Finds unlinked brand mentions and broken backlinks. Writes outreach to convert them. |
| `crisis-comms` | Immediate crisis response. Holding statement first. Never auto-sends. |
| `monitor` | Scans for brand coverage, competitor placements, breaking stories. Scores Hot/Warm/Watch. |
| `award-submissions` | Writes award submissions grounded in real proof points. Does not inflate. |
| `roi-measurement` | Full program measurement — placements, response rates, backlinks, business impact. |
| `client-reporting` | Monthly reports in business language. Includes what did not work. |
| `portfolio-manager` | Cross-client consciousness layer. Detects journalist conflicts, surfaces angle patterns, flags stalled accounts. Requires memory. |

---

## Memory (optional)

Skills work in a single session without any memory setup. You provide client context at the start and nothing persists between sessions.

For agencies or ongoing programs, the memory/ folder contains Obsidian vault templates for persistent memory across sessions. Client context, contacts, campaigns, and placements live in plain markdown and JSON files. The agent reads and updates them automatically. Every session builds on what previous sessions learned.

Multi-client agencies can run one vault per client. The portfolio-manager skill scans across all client vaults and surfaces intelligence that is invisible from inside any single client's context — journalist conflicts, cross-client angle patterns, accounts that have gone quiet.

See memory/README.md for setup instructions.

---

## The rule

Every output must pass one test before it goes out:

**Would a journalist feel respected receiving this?**

If the pitch inflates the client's importance, if the press release is promotional, if the follow-up is generic — say so and fix it. The skills earn placements by being honest and specific, not by producing more output faster.

---

## Contributing

Found a way to improve a skill? Have a new one to add? PRs and issues welcome. See CONTRIBUTING.md for guidelines.

## License

MIT — use these however you want.

---

*By 701am · earned media that earns it*
