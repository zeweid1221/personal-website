---
layout: page
title: Watermark Edit Detection
description: Error-correcting-code watermarks for detecting insertions, deletions, and substitutions after generation.
img: assets/img/ecc_edit_detection_centered.png
importance: 1
category: research
related_publications: true
---

Modern watermark detectors typically answer whether a document is watermarked. This project asks a harder integrity question: **has a watermarked output been edited after generation?**

We encode structured redundancy into LLM outputs using error-correcting codes. The resulting verifier can identify inconsistencies introduced by post-generation insertions, deletions, and substitutions while retaining the underlying watermark signal.

- Accepted to **EMNLP 2026 Findings**
- Covers method design, implementation, experiments, and evaluation

{% include figure.liquid loading="eager" path="assets/img/ecc_edit_detection_centered.png" title="Error-correcting-code watermark generation with synchronization strings" class="img-fluid rounded z-depth-1" %}

<div class="caption">
  The watermarking key generates both a VT-code tag and a synchronization string, which jointly structure token selection for edit detection.
</div>

{% cite deng2026detecting %}
