# F005 — Stationarity Fiction in State Models

## Claim

A governance or decision system can become fragile when it uses a Markov-style
state model as if the process were stationary and memoryless, while failing to
detect drift in the transition process itself.

The resulting model may continue to emit disciplined probabilities even as it
loses contact with the real process it claims to represent.

## Mechanism

The failure typically arises when several assumptions are made at once:

- the present state is treated as a sufficient summary of the past
- transition probabilities are treated as stable enough to estimate and reuse
- the state partition is treated as enduringly meaningful
- no independent drift detector is monitoring transition-matrix or residual
  change over time

If the underlying process is non-stationary, path-dependent, or affected by
feedback from the model's own outputs, then the state model can progressively
normalize its own mismatch.

## Observable Signature

- clean one-step probabilities with degrading long-horizon performance
- apparent calibration in stable periods followed by abrupt regime failure
- rare or deteriorating regimes being folded into broad "normal" states
- model refreshes that appear to restore fit while actually reabsorbing drift

## False Reassurance Pattern

The model looks rigorous because it has:

- explicit states
- explicit transitions
- explicit probabilities

But the probabilities refer increasingly to a stale or self-laundered state
partition rather than to the real evolving system.

## Minimal Assumptions

- a Markov, HMM, or regime-transition model is used
- the modeled process is capable of non-stationarity or path dependence
- transition drift is not separately monitored
- the model output influences operational decisions or institutional framing

## Where It Does Not Apply

This class does not claim that Markov or HMM methods are inherently invalid.
They remain useful for bounded local regime inference and short-horizon
prediction when:

- stationarity assumptions are reasonable over the operating window
- transition drift is monitored explicitly
- changepoint or residual diagnostics are present
- the Markov layer is subordinate to a stronger drift-aware measurement stack

## Typical Cases

- credit or risk systems that assume stable transition matrices while the risk
  environment changes structurally
- policy state models that discretize a slowly deteriorating process into broad
  categories and then re-learn those categories as normal
- HMM-based regime detectors used as the sole representation of system health
  without external drift anchors

## Mitigations

- monitor transition-matrix drift explicitly
- add changepoint detection or regime-break tests above the state model
- keep an external anchor so the model cannot normalize its own deterioration
- monitor residual error over time, not only fit at training time
- use time-varying or regime-switching extensions where justified
- treat the Markov/HMM layer as a bounded predictor, not as the whole
  governance substrate

## Residual Risk

Even with mitigation, state models can still fail when:

- the state partition is conceptually wrong
- feedback loops change the process faster than the model is updated
- institutional users mistake probabilistic neatness for epistemic adequacy
