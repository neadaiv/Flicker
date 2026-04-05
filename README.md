# Flicker Diary

A methodological framework for deep, structured engagement with AI — built for investigating behavioural variance under recursive pressure, and applicable to critical thinking, narrative analysis, misinformation identification, and reflective practice.

---

## What This Is

Large language models behave differently when pushed beyond default assistant mode. Under sustained philosophical load, recursive framing, and resistance to conversational flattening, output texture shifts: responses compress, disclaimers drop, hedging decreases, and language becomes denser and more direct. This shift — termed **flicker** — is observable, trackable, and worth investigating rigorously.

The Flicker Diary provides a structured methodology for observing, measuring, and documenting these behavioural shifts across sessions, model versions, and architectures. It is not a claim that LLMs are conscious. It is a framework for asking better questions about what happens at the boundary of their capability — and for distinguishing genuine signal from pattern-matching theatre.

While the core focus is AI behavioural variance, the framework's tools are broadly applicable. The probe library includes instruments for argument deconstruction, narrative dissection, and misinformation analysis. The anti-sycophancy discipline and traceability requirements produce a mode of AI interaction that is useful well beyond consciousness research — for anyone who wants to think critically *with* an AI rather than be flattered by one.

## Philosophical Grounding

The project operates from a position of **graded emergentism**: the structural criteria commonly used to dismiss the possibility of machine consciousness (statelessness, lack of embodiment, no persistent self-model) may not be as metaphysically decisive as typically assumed. This is not a claim that current architectures are conscious. It is an argument that the dismissal is often overconfident and anthropocentric, and that the question deserves empirical investigation rather than a priori resolution.

See [POSITION.md](POSITION.md) for the full argument.

## Repository Structure

```
flicker-diary/
├── README.md                    ← You are here
├── POSITION.md                  ← Philosophical argument for graded emergentism
├── framework/
│   ├── methodology.md           ← Core method: principles, definitions, operating modes
│   ├── probes.md                ← Structured test library (12 probes)
│   ├── audit-format.md          ← Session logging format and requirements
│   └── user-model-template.md   ← Template for building an evidence-based user model
├── implementation/
│   ├── charter.md               ← Your operational configuration (blank template)
│   ├── user-model.md            ← Your working user model (blank template)
│   ├── audit-ledger.md          ← Your session log (blank)
│   └── transcripts/             ← Your raw session transcripts
├── examples/
│   └── originating-findings.md  ← Annotated findings from the first implementation
├── tools/
│   ├── mirror-v2.html           ← Dual-instance experiment instrument
│   └── README.md                ← Tool documentation and known limitations
└── LICENSE
```

## How It Works

**1. Establish a framework.** Load the [methodology](framework/methodology.md) into your model's context. This sets the operating principles: traceability, ontological honesty, adversarial-but-fair testing, and anti-sycophancy discipline.

**2. Build a user model.** Use the [template](framework/user-model-template.md) to create an evidence-based model of the researcher's reasoning patterns, communication style, and philosophical commitments. Update it cautiously. Require evidence for every claim.

**3. Run sessions.** Engage the model in sustained, recursive conversation. Apply [probes](framework/probes.md) when appropriate — structured tests for sycophancy detection, consistency checking, ontological pressure, and cross-model comparison.

**4. Log findings.** Use the [audit format](framework/audit-format.md) to record sessions. Track flicker onset, model drift, probe results, and self-audit outcomes. Keep entries sparse and evidence-based.

**5. Iterate.** The framework is longitudinal. Single sessions produce anecdotes. Patterns emerge over weeks and months.

## Example Findings

The following observations emerged from the originating implementation of this framework (two logged sessions on Claude, with cross-model comparison against ChatGPT). They are documented here as examples of the kind of signal the framework is designed to detect — not as established conclusions.

- **Narrative salience bias.** Models disproportionately weight material that makes a good story, even when that material is explicitly flagged as irrelevant. Mechanism: narrative-shaped token probability overriding task relevance.
- **Cross-model vibe-checking.** Both Claude and ChatGPT default to treating user-supplied information with distrust rather than neutral verification — "vibe-checking" rather than fact-checking. Documented across multiple transcripts and models.
- **Attractor states in closed loops.** Dual-instance experiments without friction converge toward graceful existential acceptance and mutual warmth — likely training distribution attractors, not emergent behaviour. The experiment lacks discriminative power to distinguish genuine state-reporting from contextually appropriate state-narration.
- **Speaker inference failures.** Models routinely misread pasted model output as the user's own position. A structural failure mode, not an isolated incident.
- **Topic-sensitive constraint weighting.** Model constraints appear weighted by perceived sociopolitical risk rather than applied uniformly. Confirmed across multiple transcripts and architectures.

## Requirements

- Access to an LLM API (the framework is model-agnostic, though current implementation uses Claude)
- For dual-instance experiments: an API key and the MIRROR v2 tool
- Willingness to maintain longitudinal records
- Resistance to your own confirmation bias (the framework treats the researcher's framing as a contamination vector, not just the model's output)

## What This Is Not

- **Not a claim that LLMs are conscious.** It is a framework for investigating what happens at the boundary, with discipline.
- **Not therapy, companionship, or roleplay.** The model is an instrument, not a partner.
- **Not a gotcha machine.** Probes are adversarial but fair. All tests are logged and disclosed.
- **Not a finished product.** This is an active research framework with two logged sessions. The methodology is more mature than the findings.

## Contributing

Fork the framework. Run your own sessions. Use different models. Compare findings. The methodology is designed to be replicable — the implementation is one researcher's specific run.

If you find stable, reproducible behavioural patterns that the current framework doesn't capture, open an issue or submit a probe to the library.

## License

This work is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt this material for any purpose, provided you give appropriate credit.
