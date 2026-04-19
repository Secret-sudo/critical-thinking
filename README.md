# Critical Thinking Skill for Claude

A Claude skill that switches Claude from collaborative assistant into an uncomfortable critical reviewer at the end of a working session — before you act on, publish, or share what the session produced.

## What this skill does

After a substantive session with Claude (writing a post, building an analysis, drafting a report, producing an infographic), you ask Claude to run a critical review. The skill forces Claude into a different role: reviewer, not collaborator. It walks through six dimensions:

1. **Starting premises** you never challenged
2. **The moment** you shifted from understanding to producing
3. **Claims and numbers** accepted without verification
4. **Perspectives** that never entered the room
5. **Complexity** Claude smoothed over
6. **Confidence calibration** — was your trust in the output too high?

It then gives you an ownership test, a to-do list of what to verify, and a pattern-recognition note about how you worked with Claude in this session. It ends with a one-sentence verdict: ready to use, needs verification, or should not be used as-is.

Critically: the skill does not soften under pushback, and it never ends with encouragement.

## Why this skill exists

Research from 2024–2026 shows that frequent AI use correlates with reduced critical thinking, mediated by cognitive offloading (Gerlich 2025). Microsoft and Carnegie Mellon found that higher confidence in AI leads to less critical engagement with its outputs (Lee et al. 2025). And the "metacognitive laziness" research (Fan et al. 2024, MIT Media Lab 2025) shows users can produce good outputs while retaining less of the material and losing the ability to defend it.

The skill is a structured intervention against those patterns. It is friction you missed during the session, delivered at the moment before you publish.

Full research citations and caveats are in `references/research-foundation.md`.

---

## How to install

You do not need to know how to code to install this skill. Follow the steps below for the Claude product you use.

### Quick overview

1. Download the file `critical-thinking.skill` from this repository's [Releases page](../../releases).
2. Open Claude, find the Skills settings for your product, and upload the file there.
3. Enable the skill.

Skills currently (2026-April) work in Claude.ai (Pro, Max, Team, Enterprise plans), Claude Code, and via the Claude API. Installation works slightly differently on each. Below are the most common paths.

### For Claude.ai (web app and mobile — most common)

You need a **paid plan** (Pro, Max, Team, or Enterprise) for custom skill uploads. Free plans can use Anthropic's pre-built skills but cannot currently upload custom ones.

**Before uploading:** Make sure "Code execution and file creation" is enabled in your settings. This is what powers skills. On Free/Pro/Max plans, go to `Settings > Capabilities`. On Team/Enterprise plans, your organization owner enables this in `Organization settings`.

**To upload the skill:**

1. Download `critical-thinking.skill` from the [Releases page](../../releases) to your computer.
2. Open Claude.ai in your browser.
3. Go to `Settings` (usually found by clicking your profile picture or name in the sidebar).
4. Look for `Customize` in the menu, then `Skills`.
5. Click the upload button (wording varies — it may say "Upload skill", "Add skill", or show a "+" icon).
6. Select the `critical-thinking.skill` file you downloaded.
7. Once uploaded, make sure the toggle next to "critical-thinking" is switched on.

That is it. In your next conversation, you can trigger the skill by saying things like "run a critical thinking check on this session" or "am I ready to publish this?".

### For Claude Code (developer tool)

If you use Claude Code: clone this repository, then copy the `critical-thinking/` folder into your `~/.claude/skills/` directory. Claude Code will pick it up automatically. See [Claude Code Skills documentation](https://code.claude.com/docs/en/skills) for details.

### For the Claude API

Skills in the API are uploaded via the Skills endpoint. See [Anthropic's Skills API Quickstart](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) for code examples. Note that skills uploaded via the API are separate from skills uploaded to Claude.ai — you need to upload to each surface independently.

### Official documentation — always more current than this README

Anthropic updates the skills feature regularly, so interface details may change. For the most current installation steps, see:

- [Use Skills in Claude — Help Center](https://support.claude.com/en/articles/12512180-use-skills-in-claude) — general Claude.ai guide
- [Agent Skills Overview — API Docs](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) — for API and developers
- [Extend Claude with skills — Claude Code Docs](https://code.claude.com/docs/en/skills) — for Claude Code users

If the steps above do not match what you see in the Claude interface, the official documentation is the source of truth.

---

## How to use the skill after installation

In any Claude session, at the end of substantive work, say something like:

- "Run a critical thinking check on this session"
- "Am I ready to publish this?"
- "Did I skip anything?"
- "Kritische Prüfung bitte" (German is supported — the skill matches the session's language)

Claude will activate the skill and walk through the full six-part review.

## What to expect

The review will feel uncomfortable if you skipped verification steps during the session. That is the point. If the session was genuinely clean — you worked within your domain, verified your sources, pushed back on oversimplification — the skill will say so plainly without inventing concerns.

Two full worked examples (one flawed session, one clean session) are in `references/examples.md`.

## Limitations

The skill cannot solve three things, and it says so openly:

1. **Self-review blindness.** The same Claude that produced the session is now reviewing it. For high-stakes outputs, a second reviewer (different model, human expert, non-AI source) is still needed.
2. **Ritualization.** If you run the review to check a box, it becomes theater. The friction only works if you actually sit with a "needs verification" verdict.
3. **Domain depth.** Claude can flag uncertainty but cannot substitute for a domain expert's methodological critique.

These limitations are documented in `references/research-foundation.md`.

## Repository structure

```
critical-thinking/
├── SKILL.md                          # The skill itself (loaded when triggered)
└── references/
    ├── research-foundation.md        # Academic grounding and citations
    └── examples.md                   # Two worked review examples
```

The `critical-thinking.skill` file in the [Releases page](../../releases) is a packaged version of the three files above, ready to upload directly to Claude.

## License

MIT License. See `LICENSE` file.

## Contributing

Issues and pull requests welcome. If the skill produces a review that feels miscalibrated (too harsh on a clean session, or too lenient on a flawed one), please open an issue with the session context and the review output so the calibration guidance can be improved.

## Credits

Built with Claude. Grounded in published research on AI and critical thinking (see `references/research-foundation.md` for full citations).
