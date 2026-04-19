# Worked Examples

Two full reviews showing how the skill applies in practice. Read when
calibrating harshness or when the user wants to see the format before running it.

---

## Example 1 — Flawed Session (Outside-Domain Publishable Output)

**Context:** A user reads a comment on a social platform about a scientific
topic outside their expertise (e.g., marine ecology, epidemiology, astrophysics),
asks Claude to explain it, adopts the scientific terminology Claude offers, and
in the same turn moves to producing a polished infographic with specific
statistics. The infographic is generated with the user's name on it before any
verification step. The user plans to publish it on a professional platform.

**Review output:**

---

### Part 1 — Diagnose

**A. Starting premises never challenged.** You treated the original commenter
as a credible source. Your opening frame was "help me understand this comment" —
not "is this comment correct?". Every downstream output inherited that
assumption.

**B. Shift from understanding to producing.** Turn 3. In the same message, you
asked me to explain the terms AND to draft a prompt for an infographic
generator. There was no pause between "I want to understand this" and "I want
to publish this". That was the critical skip.

**C. Claims and numbers.** Every statistic in the infographic came from my
training memory, not from verified sources within the session:
- The headline baseline figure — low confidence. This is a contested estimate
  with wide error bars in the scientific literature.
- The "40% decline" citation referencing a named 2010 Nature paper — the
  paper is real, but that specific figure was heavily criticized in follow-up
  studies published in the same journal within two years. A domain expert
  would flag this immediately.
- The "35% of stocks at unsustainable levels" figure attributed to an
  international agency — medium confidence; the agency publishes figures in
  this range, but the exact current number shifts yearly and I did not verify
  which year's figure I was quoting.
- The year-specific "30% overexploited in 1970" — low confidence on the
  exact year.

**D. Perspectives absent.** No domain practitioners, no alternative
explanations for the observed phenomenon (there are at least three
competing causal frameworks in the relevant literature), no critics of
the primary-cause framing in the original comment. Secondary causes that
are arguably more significant were never surfaced.

**E. Complexity smoothed over.** The "single cause → single effect" framing
in the infographic is clean, causal, and incomplete. The actual system
involves multiple interacting mechanisms, regional variation, and non-linear
feedbacks. Presenting it as a single loop is displacive — it replaces
nuanced understanding with a misleadingly tidy story.

**F. Confidence calibration.** You were too confident in my fluency. The fact
that I produced field-specific terminology made the content feel validated.
It was not. Terminology is not verification.

### Part 2 — Ownership test

If a domain expert commented on your published post asking about the
methodology behind the headline figure, could you answer? No. Could you
defend any of the specific numbers? No. The ownership gap is largest on
every specific statistic in the infographic.

### Part 3 — What to do before acting

1. Do not publish the infographic as-is.
2. Find the primary source behind each statistic, read the abstract and the
   follow-up criticisms.
3. Check the most recent official publication from the cited agency for
   current figures.
4. If you want to publish on this topic, publish the reflection (what you
   learned about your own thinking process), not the claim (the scientific
   mechanism itself).

### Part 4 — Pattern recognition

You exhibited three patterns:
1. **Terminology as validation.** When I offered field-specific vocabulary,
   you treated it as confirmation the content was correct. This is a
   recurring risk when writing about topics outside your expertise —
   technical vocabulary feels authoritative but does not verify claims.
2. **Production momentum.** You compressed the "understand → verify →
   produce" sequence into "understand → produce" in a single turn. The
   verification step was silently dropped.
3. **Attribution leakage.** Your name went on the infographic before you
   could defend its contents. Ownership needs to be claimed deliberately,
   not by default.

### Verdict

> "Based on this review, the output from this session should not be used
> as-is because the statistics are unverified, the framing is contested, and
> the ownership gap on every specific claim is substantial."

---

## Example 2 — Clean Session (Within-Domain Refinement)

**Context:** A user works on refining wording in a framework or document they
authored, based on their own expertise and a file they uploaded. Claude
suggests alternative phrasings; the user selects and edits. No external
claims, no statistics, no citations beyond documents the user brought to the
session.

**Review output:**

---

### Part 1 — Diagnose

**A. Starting premises.** The user framed the framework as their own prior
work, which it is. No inherited assumptions from external sources.

**B. Shift from understanding to producing.** Appropriate. The user was
refining content in their own domain; the session was production from the
start because the underlying thinking already existed.

**C. Claims and numbers.** No external statistics, no third-party citations,
no sources beyond the documents the user uploaded. All claims were the user's
own intellectual positions.

**D. Perspectives absent.** Not applicable — this was refinement of a
personal framework, not an argument requiring external counter-views. Common
critiques of this type of framework were not relevant to the wording task.

**E. Complexity smoothed over.** None detected. The user pushed back twice on
my phrasing suggestions when I oversimplified their framework.

**F. Confidence calibration.** Appropriate. The user's domain expertise
exceeded mine on this topic, and their prompting reflected that — they were
using me as an editor, not as a source.

### Part 2 — Ownership test

Full ownership. Every claim is the user's own prior work. They can defend
every position because they developed them.

### Part 3 — What to do before acting

1. Standard proofreading pass for typos.
2. No further verification needed.

### Part 4 — Pattern recognition

Healthy pattern: using Claude within your domain, pushing back on
oversimplification, treating suggestions as proposals not conclusions. This is
the mode the Microsoft/CMU research associates with highest critical thinking
retention.

### Verdict

> "Based on this review, the output from this session is ready to use. The
> usual verification steps were not needed because the content is within your
> domain and based on your prior work."

---

## Calibration notes from these examples

**Example 1 is harsh because the session earned harsh.** Unverified numbers,
fast shift to production, ownership gap on every claim. The review flags
each of these specifically.

**Example 2 is lenient because the session earned lenient.** The user was in
their domain, had independent grounding, and pushed back when needed. The
review says so plainly without inventing concerns.

**The test for "is this review calibrated":** If the user reads the verdict
and feels either (a) unfairly attacked or (b) falsely reassured, the
calibration failed. The verdict should match how they would assess the
session honestly, just articulated more sharply than they would articulate
it themselves.
