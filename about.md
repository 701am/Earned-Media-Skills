# About Earned Media Skills

**28 AI agent skills for earned media and PR. Built by 701am. Free and open source.**

---

## Why this exists

Most AI PR tools produce output. They write pitches, generate press releases, draft follow-up emails. The problem is the output sounds like AI wrote it, the pitches go to the wrong journalists, and the angles are not grounded in anything the client can actually substantiate. Journalists can tell. Coverage does not follow.

Earned Media Skills is built differently. Every skill is designed around one question: would a journalist feel respected receiving this? If the answer is no, the skill says so before producing anything.

The skills work because they do not try to replace judgment — they bring the right knowledge to bear at the right moment. The pitch-writer skill knows the rules (under 50 characters in the subject line, lead with the story not the sender, one ask per email, specific personal first line). The humanizer skill knows the 24 patterns that mark AI-generated prose and removes them. The monitor skill knows how to score a breaking story as Hot, Warm, or Watch. The intake skill knows what questions to ask to build a client context that is actually useful.

Together they run a real earned media program.

---

## What earned media is

Earned media is coverage you earn — placements in publications, quotes in stories, podcast appearances, speaking slots — as opposed to paid media (advertising) or owned media (your own blog and social channels). It is the hardest type of media to get and the most credible when you do.

Getting it consistently requires:

- A clear understanding of what angles a client can credibly own
- The right journalists matched to the right stories
- Pitches that serve the journalist's readers, not just the client's brand
- A disciplined follow-up sequence that adds value each time
- Ongoing monitoring for opportunities to respond to breaking news
- Measurement that connects placements to business outcomes

These skills handle all of it.

---

## How the skills work

### Plain markdown, no framework

Each skill is a folder with one file inside: SKILL.md. The file contains plain-English instructions. Your agent reads it and follows it. There is nothing to install beyond cloning the repo. No runtime, no configuration, no API keys.

This is intentional. The agent's own intelligence does the work. The skills provide the domain knowledge — the frameworks, rules, and workflows that an experienced earned media practitioner carries in their head. The agent applies that knowledge to the specific client and situation.

### Client context is the foundation

The client-context skill is the memory layer. It holds the client's business description, voice and tone, founding story, product proof points, pitch angle library, competitive landscape, media history, journalist relationships, and placement record.

Every other skill reads client context before doing anything. This is what makes the output specific rather than generic. A pitch written with client context sounds like this client wrote it. A pitch written without it sounds like a template.

The intake skill builds client context from a conversation. It asks questions one at a time and writes the answers to a context file. Run it once per client. Every other skill compounds from there.

### The humanizer

AI writing has tells. Words like "leverage," "robust," "seamless," "transformative." Openers like "I hope this email finds you well." Conclusions like "In summary." Bullet points where prose should flow. Passive constructions to avoid attribution.

Journalists read hundreds of pitches. They recognize AI-generated copy immediately. The humanizer skill catalogs 24 categories of AI writing patterns and removes them from every outreach output before it goes to a journalist. The result should sound like this specific human wrote it — not like cleaned-up AI prose.

The humanizer uses the voice.md file from client context as its filter. The goal is not "professional writing." The goal is "sounds like [this person] sending [this email]."

### Memory

Skills work without memory — you provide client context at the start of each session and nothing persists between sessions. This works well for individual use and occasional PR work.

For agencies running ongoing programs, the memory/ folder contains Obsidian vault templates. Client context, contacts, campaigns, placements, and weekly briefs live in plain markdown and JSON files in an Obsidian vault on your machine. The agent reads and updates them automatically. Every session builds on what previous sessions learned.

Multi-client agencies run one vault per client. The portfolio-manager skill scans across all client vaults and surfaces what is invisible from inside any single client's context: the same journalist being pitched by two different clients in the same week, angle types that are landing across the portfolio that some clients are not using, accounts that have gone quiet and need attention.

---

## The skills

### Foundation
**client-context** — The memory layer. Every other skill reads this before doing anything. Built by intake, updated by every skill that learns something new.

**intake** — Builds client context from conversation. Asks about the business, voice, story, products, angles, and competitors. Run once per client. Everything else compounds from there.

### Strategy
**earned-media-strategy** — The full earned media strategy: where to play, what angles to lead with, which publication tiers to target, what cadence to sustain. Grounded in client context, not generic PR advice.

**editorial-calendar** — 30-day pitch and content calendar synced with news cycles, product roadmap, and seasonal angles.

**competitive-intelligence** — Maps who is getting coverage in the client's space, what angles they are using, and what territory is genuinely unclaimed.

### Research
**journalist-research** — Deep research on specific journalists by beat and outlet. Past coverage, interests, pitch preferences, relationship history. Builds contact records rather than requiring manual entry.

**data-researcher** — Mines public datasets and research sources for original story angles. Identifies the statistics and data that could anchor a campaign.

### Campaign
**digital-pr-ideation** — Generates original data study and campaign concepts complete with headline, thesis, hook statistic, methodology, visual concepts, and target publications.

**visual-gap-hunter** — Finds editorial opportunities where compelling visual content is missing from high-traffic pages. Also surfaces unlinked brand mentions for outreach.

**seo-pr** — Integrates earned media strategy with SEO objectives. Identifies publication targets that will also earn high-DA backlinks.

### Outreach
**pitch-writer** — Writes journalist pitches from client context. Every pitch grounded in a real angle, targeted to a specific journalist, written in the client's voice. The humanizer skill runs automatically on every pitch before it is presented.

**press-release** — Writes press releases structured as news stories for journalists, not promotional documents. Announcements, funding, product launches, data study releases.

**newsjacking** — Rapid-response pitching to breaking news and trending stories. Matches breaking coverage to client angles and writes the pitch immediately. Hot opportunities close within hours.

### Quality
**humanizer** — Strips AI writing patterns from any external output before it goes to a journalist or client. 24 pattern categories covering language, structure, tone, and formatting. Uses the client's voice.md as the specific filter.

### Relationships
**infinite-follow-up** — Manages the full follow-up sequence for active pitches. Bump 1 at day 3, Bump 2 at day 7, Bump 3 at day 14. Knows when to pivot the angle and when to move on. Each bump must add something new — the skill will not send a generic "just following up."

**influencer-mapper** — Maps the influencer landscape by ICP fit. Newsletter writers, podcast hosts, TikTok creators, YouTube channels, community leaders. Prioritizes by audience quality over size.

**tiktok-influencer** — Writes TikTok creator DM pitches in the creator's register. Not PR speak. Sounds like a human reaching out to a creator, not an agency pitching a brand deal.

### Content
**thought-leadership** — Op-eds, bylines, and contributed articles that position the founder as a category expert. The company is not the subject. The insight is.

**podcast-placements** — Identifies podcast shows by audience fit rather than download count. Writes guest pitch emails and prepares appearance briefs.

**speaking-events** — Identifies conference speaking opportunities, writes speaker abstracts and bios, and builds a pre/post event earned media plan to amplify each appearance.

**media-training** — Prepares the founder or executive for media interviews. Likely questions from this specific journalist, recommended answers grounded in real proof points, what not to say, and soundbites to work in naturally.

### Links
**link-reclamation** — Finds unlinked brand mentions and broken backlinks. Writes outreach to convert mentions to links and reclaim lost backlinks.

### Defense
**crisis-comms** — Immediate crisis response to negative coverage, viral criticism, or reputational threats. Writes the holding statement first. Then assesses the situation, determines the strategy, and writes the full response. Human review required before anything goes out — the skill will not auto-send under any circumstances.

**monitor** — Daily intelligence scan for brand coverage, competitor placements, category stories, and beat activity. Scores each opportunity as Hot (act within 2 hours), Warm (queue for next session), or Watch (track and return). Pre-populates pitch content for Hot opportunities so action is immediate.

### Recognition
**award-submissions** — Identifies relevant industry awards and writes submission narratives grounded in real proof points. Does not inflate claims — exaggerated submissions are disqualified and damage relationships with award bodies.

### Measurement
**roi-measurement** — Full program measurement: pitch-to-placement rate, coverage by tier, backlinks earned, domain authority gains, estimated reach, and business impact attribution.

**client-reporting** — Translates earned media activity into business language for CEOs, boards, and investors. Covers what worked, what did not work and why, and what the next month's priorities are. The "what did not work" section is not optional — it is the section that earns trust.

### Portfolio
**portfolio-manager** — The consciousness layer for agencies running multiple clients. Scans all client vaults and surfaces what is invisible from inside any single client's context: journalist conflicts, angle patterns, health by client, team workload. Requires memory with multiple client vaults.

---

## Who this is for

**Founders doing their own PR** — Run intake, build your context file, then use pitch-writer and monitor to run a systematic outreach program without a PR agency.

**In-house communications teams** — Use the full skill set to run a structured program: weekly monitor, editorial calendar, pitch sequences, monthly reporting.

**PR agencies** — Run one vault per client. The portfolio-manager skill gives you visibility across the full book of business. The intake skill runs onboarding. The client-reporting skill writes the monthly reports.

**Anyone who has tried AI for PR and found the output generic** — The client context layer and the humanizer are specifically built for this problem. The output is specific to the client because it is built from the client's actual voice, real proof points, and tested angles.

---

## What this is not

This is not a media database. The journalist-research skill finds contacts through research, not a licensed contact list. There is no built-in email sending. The outbox — everything the system produces — requires human review before it goes anywhere. The system does not send on your behalf.

This is also not a replacement for genuine relationships with journalists. The skills help you reach journalists with pitches worth their time. The relationship that develops from that is between you and the journalist.

---

## Contributing

The skills improve when practitioners contribute. If you have worked in earned media and know a better way to structure the pitch sequence, a smarter approach to newsjacking, or a skill that is missing entirely — open a PR. See CONTRIBUTING.md for guidelines.

The one rule for contributions: every skill must produce output a journalist would feel respected receiving. If a skill makes it easier to send more generic pitches faster, it does not belong here.

---

## License

MIT. Use these however you want — in client work, in products, in your own forks. Attribution appreciated but not required.

---

*Earned Media Skills by 701am*
*earned media that earns it*
