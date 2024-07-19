# Sparsity Observations

Conducted ~200 ablation experiments on sparsification thresholds across three architectures (details in /experiments/).

General pattern: performance degrades gracefully until approximately 3% density, then collapses abruptly. The transition is sharp — almost discontinuous.

Exception: structured sparsity in attention mechanisms. When sparsification is applied to attention patterns rather than weight matrices, the collapse threshold shifts dramatically. Some configurations maintained coherent outputs at densities below 0.5%.

We ran this experiment many times because we didn't believe the results.

The mechanism is unclear. Attention heads appear to be doing something that is robust to almost total ablation. Either the information is highly redundant, or it is being reconstructed from something we are not measuring.

Both possibilities are interesting.
