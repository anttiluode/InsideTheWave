# InsideTheWave

**A speculative mathematical paper about an observer whose moment is built from delayed, state-carrying neural interactions.**

Could the geometry of such an observer make its inferred world look quantum-like? This repository develops that question through explicit models, examples, counterexamples, and proposed tests.

**Status:** working paper v0.1, 2 October 2026. AI-assisted drafting and mathematical development from Antti's idea. No new biological, consciousness, or quantum experiment is reported here.

## Read the paper

- [Paper PDF](docs/paper.pdf)
- [Readable Markdown manuscript](docs/paper.md)
- [LaTeX source](docs/paper.tex)
- [Calculation checks and source provenance](docs/verification.md)

**Paper title:** *Inside the Wave: State-Carrying Neural Pings, Delayed Observers, and Quantum-Like Inference*.

## The idea

A neuron retains a history. A spike's waveform can reflect aspects of that history. A receiver responds according to its own state, and signals arrive at different times. The observer's accessible present is therefore assembled from many local pasts.

In a narrowband wave description, a propagation delay becomes a phase factor:

$$
H_{ij}(\Omega)=g_{ij}e^{-i\Omega\tau_{ij}}.
$$

When pathways mix coherently, their relative phases can alter a receiver's output. When a query changes the memory it reads, query order can alter later answers. A specially specified quadratic detector can produce a Born-shaped probability rule for its internal channels.

Those are concrete mathematical mechanisms. The further suggestion that physical quantum mechanics originates in observer architecture remains an incomplete conjecture.

## What is derived, assumed, and left open

| Claim | Status in this repository |
|---|---|
| Delay becomes phase for a monochromatic component | Derived; approximate for a slowly varying narrowband envelope |
| Coherent paths give an interference cross term | Derived for the specified mixer and quadratic readout |
| Loop phases survive changes of local phase convention | Derived for the specified signal network |
| Projective geometry of encoded responses | Derived under normalized coherent comparison; not a spacetime metric |
| Stateful interventions can fail to commute | Explicit classical and amplitude-model examples |
| Delayed observation necessarily requires quantum probabilities | Rejected by an explicit classical counterexample |
| Born-shaped channel selection | Conditional derivation assuming quadratic rates and a Poisson race |
| Universal Born rule, Planck constant, or physical quantization | Not derived |
| Bell violations from local classical neural delays | Not obtainable under the stated Bell assumptions |
| Wave activity is the seat of consciousness | Conditional philosophical proposal; not established |
| Neural hypotheses are Everettian worlds | Analogy; no equivalence established |

The paper also distinguishes a Fourier time-frequency resolution tradeoff from quantum position-momentum uncertainty, and distinguishes neural suppression of alternatives from quantum decoherence.

## Biological starting point

The supplied preprint, [*Action potential waveforms are state-dependent*](https://doi.org/10.64898/2026.09.15.751814), reports relationships between intracellular spike shape, input drive, and selected local-field-potential features. Its supplied version is not certified by peer review. It motivates retaining waveform information; it does not show that a spike conveys a complete network state or that a receiving neuron reconstructs it.

The original preprint is cited rather than redistributed. The paper's references also cover membrane dynamics, cortical travelling waves, predictive states, quantum cognition, Gabor's communication theory, Bell tests, decoherence, QBism, and relational quantum mechanics.

## Relationship to ChessFlyStatePings

[ChessFlyStatePings](https://github.com/anttiluode/ChessFlyStatePings) tests a smaller artificial-network question: does a settling-history direction affect a frozen recurrent model's readouts, and can it retrieve recorded history?

At the inspected commit, a three-position smoke test suggested receiver-specific sensitivity, while the first literal cosine history-query experiment was negative: present-only retrieval scored 1.000 top-1 accuracy; adding the real history coordinate scored 0.333. These are existing repository results, not new runs for this paper.

The distinction matters: **carrying history, making it readable, and using it as a retrieval address are separate claims.** Neither outcome proves or disproves consciousness or the physical conjecture discussed here.

## Proposed next tests

The paper proposes five inexpensive stages: matched-budget state-message decoding; controlled delay-phase interference; query-order comparisons against classical memory models; slow-world and delay-calibration limits; and observer replacement using identical preserved records.

These stages are not implemented in this repository. Their scientific outcomes remain unknown. The included figure shows analytic examples, and the calculation checks verify arithmetic and algebra only.

## Build the PDF

The PDF is already included. To rebuild from the included LaTeX source, use a TeX installation with pdfLaTeX and the packages named in `docs/paper.tex`:

```bash
cd docs
pdflatex -interaction=nonstopmode -halt-on-error paper.tex
pdflatex -interaction=nonstopmode -halt-on-error paper.tex
```

The included `figures/observer-delay.png` supplies the figure. `paper.md` is the editable manuscript. To regenerate the styled LaTeX from Markdown, install Pandoc and run this from `docs`, then run the two pdfLaTeX passes above:

```bash
pandoc paper.md --from=markdown+tex_math_dollars --to=latex --standalone --shift-heading-level-by=-1 --resource-path=. -V documentclass=article -V fontsize=11pt -V papersize=a4 -V geometry:margin=24mm -V linestretch=1.0 -V colorlinks=true -H paper-header.tex -o paper.tex
```

## Authorship and claim boundary

Research concept: Antti (`anttiluode`). Drafting and mathematical development: assisted by OpenAI ChatGPT/Codex. This is a working manuscript for discussion, not a peer-reviewed result, a priority claim, or evidence that quantum mechanics is an illusion.

The aim is to make the speculation precise enough that its mechanisms can be examined, its assumptions can be challenged, and its predictions can fail.
