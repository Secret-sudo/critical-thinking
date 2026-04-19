# Research Foundation

Academic grounding for the critical-thinking skill. Read when the user asks why
a concern is being flagged, or when the rigor of the review itself needs defense.

---

## 1. Gerlich (2025) — Cognitive Offloading

**Source:** Gerlich, M. (2025). AI Tools in Society: Impacts on Cognitive Offloading
and the Future of Critical Thinking. *Societies*, 15(1), 6. DOI: 10.3390/soc15010006

**Method:** Mixed methods, 666 participants, surveys + thematic interviews.

**Key findings:**
- Significant negative correlation between frequent AI tool usage and critical
  thinking abilities, mediated by cognitive offloading.
- Younger participants (17–25) showed higher AI dependence and lower critical
  thinking scores than older groups.
- Higher education correlates with better critical thinking regardless of AI
  usage — education acts as a protective buffer.
- Non-linear relationship: moderate AI usage does not significantly harm
  critical thinking; excessive reliance produces diminishing cognitive returns.

**Implication for the skill:** The intervention is not "use AI less" — it is
"maintain cognitive engagement while using AI". The review's job is to detect
the moments engagement dropped.

**Caveats:** Correlational, not causal. Self-reported measures. The study
establishes the pattern, not the mechanism.

---

## 2. Lee et al. / Microsoft & Carnegie Mellon (2025) — Knowledge Worker Study

**Source:** Lee, H.-P., Sarkar, A., Tankelevitch, L., Drosos, I., Rintel, S.,
Banks, R., & Wilson, N. (2025). The Impact of Generative AI on Critical Thinking:
Self-Reported Reductions in Cognitive Effort and Confidence Effects From a Survey
of Knowledge Workers. Proceedings of CHI 2025.

**Method:** 319 knowledge workers, 936 first-hand GenAI use cases, quantitative
and qualitative analysis.

**Key findings:**
- **Higher confidence in GenAI → less critical thinking.** This is the central
  finding. Users who trust the tool engage less critically with its outputs.
- **Higher self-confidence (in one's own expertise) → more critical thinking.**
  Users who are confident in the domain verify more, not less.
- For 40% of tasks, participants reported using no critical thinking at all.
- Critical thinking happens in three phases: (1) goal and query formation,
  (2) response inspection, (3) response integration. Each is a potential
  skip-point.
- GenAI shifts the nature of cognitive work from execution to oversight — but
  only when oversight actually happens. When users trust the tool, oversight
  collapses.

**Implication for the skill:** The review targets the three phases explicitly.
It also detects the confidence asymmetry — the user's confidence in Claude's output
vs. his grounding in the domain.

**Caveats:** Self-report. No direct behavioral measure. Short-term study.

---

## 3. Fan et al. (2024) — Metacognitive Laziness

**Source:** Fan, Y., Tang, L., Le, H., Shen, K., Tan, S., Zhao, Y., Shen, Y.,
Li, X., & Gašević, D. (2024). Beware of metacognitive laziness: Effects of
generative artificial intelligence on learning motivation, processes, and
performance. *British Journal of Educational Technology*.

**Method:** Lab experiment, 117 Chinese university students, randomized
between ChatGPT, human expert, checklist tool, and control groups. Writing
task in English (non-native language).

**Key findings:**
- Coined "metacognitive laziness" — offloading not just the task, but the
  self-regulatory oversight of the task.
- ChatGPT users achieved higher short-term performance (essay scores) but
  showed no gains in knowledge transfer or retention.
- Students often bypassed instruction boundaries to get ChatGPT to write
  directly for them, even when prompted not to.
- Reduced engagement in orientation, planning, monitoring, and evaluation
  phases of self-regulated learning.

**Implication for the skill:** The "pattern recognition" section of the review
(Part 4 in SKILL.md) is specifically about detecting metacognitive laziness in
the user's prompting patterns — not just the outputs.

**Caveats:** Student population, lab setting, single task type. Generalization
to senior practitioners is an inference, not a demonstrated finding.

---

## 4. MIT Media Lab (Kosmyna et al., working paper 2025) — Brain Activity Study

**Source:** MIT Media Lab working paper, 54 participants writing essays under
three conditions: ChatGPT, search engine, brain-only.

**Key findings:**
- Brain activity (measured via EEG) was lowest in the ChatGPT group.
- ChatGPT users showed weaker recall of what they had just written.
- Brain-only group showed strongest neural engagement and strongest recall.
- Early AI use in a task correlated with lower downstream engagement even
  when AI was removed.

**Implication for the skill:** Reinforces that even successful outputs can
leave thin cognitive traces. The ownership test (Part 2) is designed to
surface this — can the user reconstruct the reasoning without the session?

**Caveats:** Working paper, not peer-reviewed. Small N. Writing task may not
generalize to other knowledge work.

---

## 5. Singh et al. (2025) — Metacognitive Cues (MetaCues)

**Source:** Singh, A. et al. (2025). MetaCues: Enabling Critical Engagement
with Generative AI for Information Seeking and Sensemaking. arXiv / CHI 2025.

**Method:** Controlled studies on AI-assisted information search, comparing
users given metacognitive cues vs. no cues.

**Key findings:**
- Metacognitive cues — prompts to pause, reflect, assess comprehension, and
  consider multiple perspectives — increase active engagement, broader
  exploration, and more thoughtful follow-up questioning.
- Five cue categories proved effective: orienting, monitoring, comprehension,
  broadening perspective, consolidation.

**Implication for the skill:** The six-part review structure maps to these
cue categories:
- Part 1A (premises) = orienting cue
- Part 1B (shift to producing) = monitoring cue
- Part 1C (claims/numbers) = comprehension cue
- Part 1D–E (perspectives, complexity) = broadening perspective cue
- Parts 2–3 (ownership, to-do) = consolidation cue

---

## 6. Microsoft Research (Sarkar et al. 2025) — Rethinking AI in Knowledge Work

**Source:** Microsoft Research blog and CHI 2025 workshop, "Rethinking AI in
Knowledge Work: From Assistant to Tool for Thought".

**Key findings:**
- Generative AI can lead knowledge workers to produce a narrower range of
  ideas, invest less effort in critical thinking, and retain less of what they
  write or read.
- Low-stakes tasks are reviewed less critically than high-stakes tasks — but
  "stakes" are often underestimated by users in the moment.
- AI works best as a thought partner: when AI challenges users, decision
  quality improves; when AI accommodates, decision quality drops.

**Implication for the skill:** The skill is deliberately designed to challenge,
not accommodate. The "no encouragement" rule at the end is a direct response
to this finding.

---

## How the research shapes skill design

| Research insight | Skill design choice |
|------------------|---------------------|
| Confidence in AI → less scrutiny (Lee 2025) | Part 1F explicitly surfaces confidence asymmetry |
| Three critical-thinking phases (Lee 2025) | Part 1 walks through all three |
| Metacognitive laziness is patterned (Fan 2024) | Part 4 names the pattern, not just the session |
| Thin cognitive traces (MIT 2025) | Part 2 tests whether the user can reconstruct the reasoning |
| Metacognitive cues work (Singh 2025) | Six-part structure mirrors the five cue categories |
| AI that challenges improves decisions (Sarkar 2025) | "No encouragement" rule, hold position under pushback |
| Moderate use is fine (Gerlich 2025) | Calibration section: do not fake friction |

---

## Open questions and skill limitations

**The skill cannot solve:**

1. **Self-review blindness.** I wrote the session, now I'm reviewing it. My
   blind spots produced the outputs and will also shape the review. For
   high-stakes outputs, a second reviewer (different AI model, human expert,
   non-AI source) is needed. The skill is self-review, not peer-review.

2. **Ritualization.** If the user runs the review purely to check a box, it
   becomes theater. The research on metacognitive laziness suggests users
   often perform engagement while offloading. The skill's friction only works
   if the user actually sits with the "needs verification" verdict.

3. **Domain depth.** I can flag uncertainty in domains outside the user's core
   expertise, but I cannot substitute for a domain expert's methodological
   critique. For medical, legal, or technical claims, expert review is
   non-negotiable.

These limitations are honest, not defeatist. The skill still captures most of
what the user would miss alone, especially compared to the current alternative
(no review at all).
