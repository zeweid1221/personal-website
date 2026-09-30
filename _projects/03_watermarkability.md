---
layout: page
title: Watermarkability
description: Measuring and improving model compatibility with logit-based watermarks.
img: assets/img/watermarkability_pipeline.png
importance: 3
category: research
related_publications: true
---

Different language models can respond very differently to the same logit-based watermarking rule. This project studies **watermarkability**: the degree to which a model can satisfy watermark constraints while maintaining generation quality.

The work develops measurements of model–watermark compatibility and methods for improving watermark performance across model families.

- Evaluates compatibility across language models and watermark rules
- Studies the relationship between constraint satisfaction and text quality
- [View code](https://github.com/zeweid1221/LLM_Watermarkability)

{% include figure.liquid loading="eager" path="assets/img/watermarkability_pipeline.png" title="Watermarkability improvement pipeline" class="img-fluid rounded z-depth-1" %}

<div class="caption">
  The method first improves model–watermark compatibility with LoRA, then uses a residual controller to meet the target watermark strength reliably.
</div>

{% cite deng2026watermarkability %}
