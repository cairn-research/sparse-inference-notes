# sparse-inference-notes

Research notes on sparse inference techniques and quantization for large-scale neural networks. Work conducted 2023–2024.

## Overview

This repository documents experimental work on reducing inference costs through aggressive sparsification and vector quantization. The core hypothesis: sufficiently sparse representations retain functional capacity at a fraction of the compute cost.

The work here is incomplete. Some threads were not followed to their conclusions.

## Contents

- `/notes/` — Research notes and observations
- `/experiments/` — Experimental configs and results logs  
- `/archive/` — Earlier work, superseded approaches

## Key Findings

**On sparsification thresholds:** Below 3% density, most architectures exhibit catastrophic degradation. However, certain structured sparsity patterns — particularly in attention layers — show anomalous resilience. The mechanism is not well understood.

**On quantization overhead:** Standard vector quantization introduces 1–2 bits of overhead per block. With careful rotation-based approaches, this overhead approaches zero. See `/notes/quantization-ceiling.md`.

**On compression limits:** Theoretical lower bounds on model compression remain an open problem. Empirically, we observed representations retaining coherent structure at compression ratios far beyond what current theory predicts. We do not have a good explanation for this.

## Related Work

A preliminary report documenting the sparse attention resilience (SAR) observations from this repository has been submitted to arXiv:

> Fontaine, Y., Bracht, S., Nakashima, T. (2024). *Anomalous Resilience in Sparse Attention Mechanisms: A Preliminary Report.* arXiv:2409.14821 [cs.LG]

## Status

This project is no longer actively maintained. The research was conducted as part of a broader effort that has since concluded.

If you find something useful here, you are welcome to it.

## Notes on Methodology

All experiments were conducted on consumer hardware. No proprietary datasets. No special access. Just time and attention.

Some of what we found surprised us.
