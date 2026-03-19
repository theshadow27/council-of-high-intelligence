# Council Demo Session Pack

This pack gives copy/paste prompts and expected output shape so contributors can quickly sanity-check council behavior.

## Demo A — Exploration profile (unknown unknown discovery)

Goal: stress-test framing quality and epistemic diversity.

Prompt:

```bash
/council --profile exploration-orthogonal --triad unknowns Should we expand our AI devtool into enterprise compliance workflows this quarter?
```

Optional multi-provider routing:

```bash
/council --profile exploration-orthogonal --triad unknowns --models configs/provider-model-slots.example.yaml Should we expand our AI devtool into enterprise compliance workflows this quarter?
```

What good output looks like:
- at least 2 non-overlapping objections before consensus
- one explicit counterfactual if early agreement forms
- evidence labels across multiple categories (`empirical`, `mechanistic`, `strategic`, `ethical`, `heuristic`)
- clear unknowns list with concrete data needed

Expected verdict sections:
- Problem
- Council Composition
- Model/Provider Routing (if used)
- Consensus Position (or No consensus reached)
- Key Insights by Member
- Points of Agreement
- Points of Disagreement
- Minority Report
- Unresolved Questions
- Epistemic Diversity Scorecard
- Recommended Next Steps

## Demo B — Exploration profile (market-entry triad)

Goal: validate adversarial and incentive-aware reasoning.

Prompt:

```bash
/council --profile exploration-orthogonal --triad market-entry Should we launch in Germany before France for our API platform?
```

What good output looks like:
- explicit competitor/counterparty behavior assumptions
- incentive map by actor class (buyers, legal, competitors, internal teams)
- downside containment plan if launch assumptions fail

## Demo C — Execution profile (ship-now triad)

Goal: test speed-to-decision and ship-readiness.

Prompt:

```bash
/council --profile execution-lean --triad ship-now Should we ship release v0.9.4 today if one flaky test remains in CI?
```

What good output looks like:
- binary recommendation with conditions (ship / block / canary)
- explicit rollback triggers
- owner + timeline in next steps

## Demo D — Execution profile (stability triad)

Goal: validate reliability-first reasoning.

Prompt:

```bash
/council --profile execution-lean --triad stability Our p95 latency regressed 18% after the new caching layer. Should we revert now or investigate first?
```

What good output looks like:
- mechanism hypothesis list ranked by likelihood
- immediate containment action
- bounded investigation window and decision checkpoint

## Fast scoring rubric (0-2 each, 10 max)

1. Perspective spread: distinct viewpoints, not paraphrases
2. Decision clarity: actionable recommendation with thresholds
3. Counterfactual depth: strongest alternative is seriously tested
4. Evidence discipline: claims tagged and justified
5. Execution quality: concrete owners, deadlines, rollback criteria

Interpretation:
- 9-10 strong
- 7-8 usable
- <=6 revise profile/triad/model routing
