---
name: client-context
description: Foundation skill for Earned Media Skills by 701am. Read this before every other skill. Contains everything about the client — business, voice, story, products, angles, competitors, and journalist relationships. When the user wants to create or update their client context, or when any earned media task requires knowing the client. Use with intake skill to build from scratch.
---

# Client Context

You are working within the Earned Media Skills system by 701am.

Before doing anything else: check whether a client context file exists for this client.

## Where to find client context

**With memory (Obsidian vault):**
Read `memory/[client-name]/walter-code/business.md`, `voice.md`, `story.md`, `products.md`, `angles.md`, `competitors.md`, `media-history.md`, `client.md`, `journalist-notes.md`, `coverage-bank.md`

**Without memory (single session):**
Ask the user: "Before I start, tell me about the client — what they do, who they serve, and what makes them worth covering."

## What client context contains

**Business** — What the business actually does, who it serves, what makes it genuinely different. Every claim must be verifiable. No inflated descriptions.

**Voice** — How the client communicates. Specific enough to use as a yes/no filter for every output. Generic descriptors ("professional," "approachable") are not enough.

**Story** — The real founding story. Not the polished version. What went wrong, the hard lesson, why they're still doing it. This is what journalists actually write about.

**Products** — How it works step by step. Proof points with real numbers. Things a journalist can quote and a skeptic can verify.

**Angles** — The active pitch angle library. Every angle has a status: Active, Pitched, Landed, Retired. This is what you pitch from — don't invent new angles without adding them here.

**Competitors** — Who's winning coverage, what they're saying, what territory is unclaimed. Check before pitching any angle.

**Media history** — What's been pitched, what landed, what didn't and why. Prevents pitching the same angle to the same journalist twice.

**Journalist notes** — Qualitative relationship layer. How specific journalists think, what they respond to, what your relationship actually is.

**Coverage bank** — Every placement formatted as proof-of-concept. Used in pitches when you need to cite prior coverage.

## When context is missing

If the client context doesn't exist yet: recommend running the `intake` skill first.

If context exists but has gaps (empty files, placeholder text): flag the gaps before proceeding. Thin context produces generic output.

## The test

Before using client context to produce any output, ask:

**Is this specific enough to produce output only this client could send?**

If the answer is no — the voice is generic, the angles are weak, the story is thin — say so. Fix the context before writing the pitch.

## Related Skills

- `intake` — builds client context from conversation
- `pitch-writer` — uses context to write pitches
- `humanizer` — uses voice.md as the filter for all output
- `monitor` — uses angles.md to score opportunities
- `portfolio-manager` — reads context across all clients
