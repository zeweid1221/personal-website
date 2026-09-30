---
layout: page
title: Robust Inference for Delayed Point Processes
description: Correction-centered distributional robustness under reporting delays and model misspecification.
img: assets/img/delayed_point_process.png
importance: 5
category: research
related_publications: true
---

Reporting delays can distort the observed timing and likelihood structure of event sequences. This project develops a **correction-centered Wasserstein distributionally robust optimization** framework for point-process inference under delay-model misspecification.

The method combines event-level backward timestamp correction with sequence-level robustness, hedging against uncertainty that remains after correction. It is evaluated in controlled nonhomogeneous Poisson-process simulations and on California utility-reported wildfire events.

{% include figure.liquid loading="eager" path="assets/img/delayed_point_process.png" title="Correction-centered robust inference for delayed point processes" class="img-fluid rounded z-depth-1" %}

<div class="caption">
  Timestamp correction moves delayed observations toward the latent process, while distributional robustness hedges against the remaining misspecification.
</div>

{% cite deng2026robust %}
