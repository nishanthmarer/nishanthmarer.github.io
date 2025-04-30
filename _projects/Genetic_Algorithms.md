---
layout: page
title: Distributed Genetic Algorithm for Feature Selection
description: Empirically show that process-based Parallelism speeds up the Genetic Algorithm for Feature Selection
img: assets/img/parallelvsseq.png
importance: 2
category: work
---

We empirically show that process-based Parallelism speeds up the Genetic Algorithm (GA) for Feature Selection (FS) 2x to 25x, while additionally increasing the Machine Learning (ML) model performance on metrics such as F1-score, Accuracy, and Receiver Operating Characteristic Area Under the Curve (ROC-AUC).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ga_diagram.png" title="General Genetic Algorithm Flow Diagram" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/parallelvsseq.png" title="Advantage in Time Consumption because of Parallelis" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

{% raw %}

<div style="text-align: center; margin-top: 2rem; margin-bottom: 2rem;">
    <iframe src="/assets/files/Genetic_Algorithm.pdf" width="720" height="480" style="border: 1px solid #ccc; border-radius: 8px;"></iframe>
    <div class="caption">
        <strong>Project:</strong> Distributed Genetic Algorithm for Feature Selection
    </div>
</div>
{% endraw %}
