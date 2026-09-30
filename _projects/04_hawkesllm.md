---
layout: page
title: HawkesLLM
description: Semantic uncertainty propagation in agentic text simulation.
img: assets/img/hawkesllm_pipeline.png
importance: 4
category: research
related_publications: true
---

**HawkesLLM** combines multivariate Hawkes processes with language models to model temporal influence and semantic uncertainty propagation in agentic text simulation.

The framework computes Hawkes influence scores over the event history, selects the most influential predecessor events under a constrained prompt-memory budget, and uses that compact context to generate the next event.

{% include figure.liquid loading="eager" path="assets/img/hawkesllm_pipeline.png" title="HawkesLLM simulation pipeline" class="img-fluid rounded z-depth-1" %}

<div class="caption">
  Hawkes influence scores select the most relevant predecessor events, which are assembled into a compact prompt for the next-event generation step.
</div>

{% cite deng2026hawkesllm %}
