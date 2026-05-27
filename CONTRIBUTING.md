# Contributing to Earned Media Skills

PRs and issues welcome. Here is how to contribute.

## Adding a new skill

1. Create a new directory under `skills/` using lowercase-hyphenated naming
2. Create `skills/your-skill-name/SKILL.md`
3. Follow the frontmatter format:

```yaml
---
name: your-skill-name
description: When the user wants to... [trigger phrases]. Also use when the user mentions...
---
```

4. Keep SKILL.md under 500 lines
5. Include a **Related Skills** section at the end
6. Test by asking Claude Code to use the skill

## Improving an existing skill

- Improve clarity, add missing trigger phrases, add better examples
- Keep the soul rule: would a journalist feel respected receiving output from this skill?

## Naming rules

- Lowercase letters, numbers, and hyphens only
- No consecutive hyphens
- Must match the parent directory name exactly
- Valid: `pitch-writer`, `press-release`, `ab-test-variant`
- Invalid: `PitchWriter`, `pitch_writer`, `pitch--writer`

## The soul rule

Every skill that produces external output must pass one test:

**Would a journalist feel respected receiving this?**

If the skill encourages inflation, generic pitches, or spray-and-pray outreach — it does not belong here.

## Pull request checklist

- [ ] `name` matches directory name exactly
- [ ] `description` includes clear trigger phrases
- [ ] SKILL.md is under 500 lines
- [ ] Includes **Related Skills** section
- [ ] No fabricated statistics or claims
- [ ] Output passes the journalist respect test
