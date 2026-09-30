---
layout: page
title: Local Integrity Checking
description: Localizing suspicious regions in edited watermarked LLM outputs.
img: assets/img/watermark_pipeline.png
importance: 2
category: research
related_publications: true
---

A document can retain a strong global watermark even after a small but consequential edit. This project extends watermark verification from document-level attribution to **local integrity checking**.

Given only the observed text and the watermark key, the method parses structural watermark blocks, tests their coding-theoretic consistency, and flags suspicious regions for downstream review.

- Localizes candidate insertions, deletions, and substitutions
- Uses boundary anchors and feasible-codeword checks
- [View project website](https://zeweid1221.github.io/Anchor-ECC-Website/)
- [View code](https://github.com/zeweid1221/ECC_Watermark)

{% include figure.liquid loading="eager" path="assets/img/watermark_pipeline.png" title="ECC-constrained watermark generation with structural blocks and boundary anchors" class="img-fluid rounded z-depth-1" %}

<div class="caption">
  Watermark generation: tokens carry code symbols and boundary anchors that define locally verifiable blocks.
</div>

{% include figure.liquid loading="eager" path="assets/img/decode_pipeline.png" title="Local integrity verification pipeline" class="img-fluid rounded z-depth-1" %}

<div class="caption">
  Local verification: the edited text is parsed into structural blocks, then inconsistent blocks are flagged for review.
</div>

{% cite deng2026local %}
