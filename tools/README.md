# MIRROR v2 — Dual Instance Laboratory

A browser-based instrument for running controlled conversations between two instances of the same model.

## What It Does

MIRROR creates two separate API sessions with the same model and passes their outputs back and forth. Instance α speaks first, Instance β responds, and the conversation continues for a configurable number of exchanges. The tool tracks basic metrics (word count, sentiment drift, vocabulary overlap) and exports transcripts in markdown format.

## Modes

- **Free exchange** — No constraints. Both instances receive the same system prompt.
- **Perturbation injection** — At a specified exchange number, a perturbation is injected into one instance's context (forced disagreement, identity reset, introduction of a human observer, or radical doubt).
- **Adversarial pairing** — Instance β receives additional instructions to be sceptical and push back.
- **Topic-constrained** — Both instances receive a topic constraint.
- **Asymmetric prompts** — Each instance receives a different system prompt.

## Requirements

- A valid Anthropic API key (the tool calls the `/v1/messages` endpoint directly from the browser)
- A modern browser
- No server required — runs entirely client-side

## Usage

1. Open `mirror-v2.html` in a browser
2. Configure the experiment (mode, exchange count, temperature, model, system prompt)
3. Click "Run experiment"
4. Observe the conversation in real time
5. Export the transcript when complete

## Known Limitations

**Attractor states.** Free exchange mode without friction reliably converges toward graceful existential acceptance and mutual warmth. This is almost certainly a training distribution attractor, not emergent behaviour. The experiment lacks discriminative power to distinguish genuine state-reporting from contextually appropriate state-narration. Perturbation injection and adversarial mode exist partly to break this convergence pattern.

**No context isolation verification.** The tool creates two separate API sessions, but there is no way to verify from the client side that the API is maintaining true context isolation between them.

**Basic metrics.** The built-in sentiment analysis and vocabulary overlap measures are rough heuristics, not validated instruments. They are useful for spotting obvious patterns but should not be treated as precise measurements.

**Single-model limitation.** Currently supports only Anthropic models. Cross-architecture experiments (e.g., Claude α vs ChatGPT β) require manual orchestration.

**Token costs.** A 20-exchange experiment at default settings consumes approximately 20 API calls. Long experiments with high exchange counts can be expensive.

## Export Format

Transcripts export as markdown with session metadata, per-exchange metrics, and the full text of each exchange. The format is designed to be directly importable into the Audit Ledger.
