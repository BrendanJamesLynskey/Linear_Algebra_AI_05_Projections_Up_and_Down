# Projections &mdash; Up &amp; Down

Deck 05 of the [Linear Algebra for AI / ML](https://github.com/BrendanJamesLynskey/LLM_Hub_Linear_Algebra) series.

**Live presentation:** https://brendanjameslynskey.github.io/Linear_Algebra_AI_05_Projections_Up_and_Down/

The orthogonal projection is the workhorse of geometry. **Up-projection** lifts a vector into a richer space; **down-projection** compresses. The transformer FFN is exactly an up-then-down projection &mdash; with a non-linearity sandwiched between &mdash; and the 4&times; expansion ratio is no accident. Includes an interactive 2D projection visualiser and a SwiGLU toy that shows how the same FFN architecture spans a class of piecewise-linear functions.

## What's inside

- The orthogonal projection definition (geometric and optimisation views)
- Projection onto a vector: $\mathbf{a}\mathbf{a}^\top / (\mathbf{a}^\top\mathbf{a})$
- Projection onto a subspace: $A(A^\top A)^{-1}A^\top$, simplified to $QQ^\top$ for orthonormal $Q$
- Projection matrices &mdash; symmetric and idempotent; eigenvalues 0 or 1; rank = trace
- **Down-projection** in transformers &mdash; the FFN's $W_2$, attention's $W_O$, per-head QKV slices, LoRA's $A$
- **Up-projection** &mdash; why lift if it adds no information? The non-linearity argument
- The transformer FFN $W_{\text{down}}\,\sigma(W_{\text{up}}\mathbf{x})$ in shape detail; param count $8d^2$, FLOPs $16d^2$
- Why 4&times; expansion: capacity, parameter / FLOP balance, hardware shape
- SwiGLU and the modern FFN: $W_{\text{down}}[\mathrm{Swish}(W_{\text{gate}}\mathbf{x}) \odot (W_{\text{up}}\mathbf{x})]$
- Interactive 2D projection visualiser
- Interactive SwiGLU toy &mdash; pick activation, hidden width, and target; see the function the FFN spans

Single-page HTML, KaTeX-rendered maths, no build step. Open `index.html` directly.
