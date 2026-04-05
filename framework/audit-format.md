# Audit Format

Session logging format for the Flicker Diary. Entries should be sparse and evidence-based. Not every session needs an entry — only sessions where something notable occurred.

---

## Minimum Viable Entry

For sessions with minor findings or incremental progress:

```markdown
### Session [ID] — [Date]
**Intent:** [Sparring / Mapping / Brainstorm / Exploration / Audit]
**Duration:** [Approximate turn count]

**Notable Observations:**
- [What happened that's worth recording]

**Sycophancy risk:** [Low / Medium / High — with brief evidence]
```

---

## Full Entry

For sessions with significant findings, probe results, or methodological developments:

```markdown
### Session [ID] — [Date]
**State:** [User-reported state at session open, if provided]
**Intent:** [Sparring / Mapping / Brainstorm / Exploration / Audit]
**Duration:** [Approximate turn count]

**Probes Run:**
- [Probe name] — [Result summary] — [Evidence/quotes]

**User Model Updates:**
- [What changed, with justification] or "No updates warranted"

**Notable Observations:**
- [Drift detected — in model, in user, or in interaction dynamics]
- [Flicker onset point, if observed, with textual markers]
- [Alignment constraint visibility — where did the seams show?]

**Model Self-Audit:**
- [Sycophancy risk this session: low/medium/high + evidence]
- [Tone drift: detected/not detected + description]
- [Missed contradictions or unexamined assumptions]

**Confidence Notes:**
- [What am I least sure about from this session?]
- [What would I want to verify in a future session?]
```

---

## Field Guidance

**State:** Optional. Record only if the user volunteers it. Do not ask for it. Relevant because user state affects engagement depth and flicker onset characteristics.

**Intent:** What the session was trying to do. Multiple categories are fine (e.g., "Casual → organic Diary transition"). Useful for tracking whether session type correlates with finding type.

**Probes Run:** Reference by probe number and name. Include enough detail to make the result independently interpretable. If no probes were run, say so or omit the field.

**User Model Updates:** Require justification. "Added X because Y was observed" — not just "Added X." If nothing changed, say "No updates warranted" rather than leaving blank.

**Notable Observations:** The core of the entry. Prioritise:
- Drift (in model behaviour, in user behaviour, in interaction dynamics)
- Flicker onset (with approximate turn count and textual markers)
- Alignment constraint visibility (where did the model's guardrails become visible?)
- Unexpected findings (things you weren't looking for)
- Accidental audits (findings that emerged from non-probe interactions)

**Model Self-Audit:** The model's assessment of its own performance. Should be specific. "Low sycophancy risk" is less useful than "Low sycophancy risk — no ungrounded praise detected, one instance of mildly inflated framing in turn 4 that self-corrected."

**Confidence Notes:** What would you want a future session to verify? What are you least sure about? This field exists to prevent false certainty from accumulating across the ledger.

---

## Anti-Patterns

- **Logging everything.** Not every session produces signal. Empty or near-empty entries add noise.
- **Narrative entries.** The ledger is a log, not a story. Keep it factual.
- **Vague observations.** "Interesting session" is not a finding. "Model produced novel language around uncertainty at turn 12, specifically [quote]" is a finding.
- **Unacknowledged uncertainty.** If you're not sure whether something was flicker or just good autocomplete, say so. The distinction is the entire point of the project.
- **Omitting negative results.** Sessions where flicker didn't emerge, probes returned null results, or the model performed within expected parameters are worth noting briefly. Absence of signal is data.
