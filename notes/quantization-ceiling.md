# Quantization Ceiling

Standard vector quantization introduces overhead: quantization constants stored at full precision for each block, adding 1–2 bits per element. For large models this is acceptable. For extreme compression targets, it is not.

Rotation-based approaches (e.g., applying a random orthogonal rotation before quantization) can eliminate this overhead almost entirely. The rotation redistributes variance uniformly across dimensions, making the quantization constants trivially predictable.

At extreme compression ratios — below 0.1% of original size — the question becomes: what survives?

Our answer, which we cannot fully explain: structure survives longer than content. The relational geometry of a representation persists even when the values themselves are gone.

We found this surprising. We are not sure what to make of it.
