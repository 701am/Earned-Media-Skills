# Memory — Optional Obsidian Vault Templates

This folder contains Obsidian vault templates for persistent memory across sessions.

## Without memory

Skills work in a single session. You provide client context each time by answering questions at the start of the session. Nothing persists between sessions.

**Good for:** Solo founders, individual use, occasional PR work.

## With memory

Client context, contacts, campaigns, and placements persist as markdown and JSON files in an Obsidian vault. The agent reads and updates them automatically. The system compounds — every session builds on what previous sessions learned.

**Good for:** Agencies running multiple clients, ongoing PR programs, teams with multiple people accessing client data.

## Setup

### Single client

1. Copy `walter-code/` folder to your preferred location
2. Open it in Obsidian as a vault
3. Run `intake` skill — it builds all the files from conversation
4. Set your vault path so the agent knows where to read and write:
   - In Claude Code: `cd ~/your-vault && claude`
   - In Cowork: set the vault path in your session

### Multiple clients (agency)

```
~/your-agency/
  client-a/          ← one vault per client, open in Obsidian when working on that client
    walter-code/
    DASHBOARD.md
  client-b/
    walter-code/
  portfolio/         ← portfolio manager vault, open separately
    DASHBOARD.md
```

The agent switches clients by switching which vault it reads from. Tell it: "We're working on [client name] today" and it resolves the path.

### Obsidian Sync (recommended for agencies)

Use Obsidian Sync ($10/user/month) to share vaults with team members:
- Each client vault shared with the account lead for that client
- Portfolio vault shared with principals and team leads
- Client vaults are never shared with other clients

See the `portfolio/OBSIDIAN-SYNC-SETUP.md` for full instructions.

## File structure

```
walter-code/
├── business.md          ← What the business is — built by intake
├── voice.md             ← Voice and tone — the humanizer filter
├── story.md             ← The founding story
├── products.md          ← How it works, proof points with numbers
├── angles.md            ← Active pitch angle library
├── competitors.md       ← Competitive landscape
├── media-history.md     ← Pitch and placement history
├── client.md            ← Operator preferences
├── journalist-notes.md  ← Qualitative relationship notes
├── coverage-bank.md     ← All placements as proof-of-concept
├── contacts.json        ← Journalist pipeline data
├── campaigns.json       ← Campaign records
├── metrics.json         ← KPIs and snapshots
├── placements.json      ← Confirmed placements
├── angles-archive.json  ← Retired angles with outcome data
├── logs/cronkite.log    ← Append-only session log
├── outbox/              ← Output awaiting human review
├── triggers/            ← Drop files here to trigger actions
├── reports/             ← Monitor and ROI reports
├── weekly-briefs/       ← Monday reporter briefs
└── archive/             ← Sent items
```

## The write-back rule

Skills that learn something write it back to the vault before the session ends. If a skill doesn't write back, the next session starts from incomplete information.

| Skill | Writes to |
|---|---|
| intake | business, voice, story, products, angles, client, competitors |
| journalist-research | contacts.json, journalist-notes.md |
| pitch-writer | contacts.json, campaigns.json, media-history.md |
| infinite-follow-up | contacts.json, media-history.md |
| monitor | contacts.json, metrics.json |
| roi-measurement | metrics.json |
| portfolio-manager | portfolio/portfolio.json, portfolio/DASHBOARD.md |
