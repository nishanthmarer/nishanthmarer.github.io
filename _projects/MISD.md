---
layout: page
title: Privacy preserving Synthetic Data Generation
description: Medically Informed Stable Diffusion (MISD)
img: assets/img/brainCT.png
importance: 3
category: work
---

The advent of deep learning has enabled the ability to solve complex problems with relative ease. However, the price of this ease comes at the cost of requiring massive amounts of data. Typically, the larger and more complex a problem, the more data is required. The medical field has several complex problems that could benefit from deep learning, but due to heavily restricted access to datasets (HIPA, risk of patient identification ), and the cost of accurate labeling of ground truth (via an expert) it becomes challenging to effectively deploy novel deep learning methods to this area. With the rising popularity of GANs and Stable Diffusion this begs the question: Is it possible to develop a low cost method of generating accurate synthetic medical data.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/FlowChart.png" title="Data Flow Pipeline" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Data flow Pipeline for Image Generation using Stable Diffusion
</div>

{% raw %}

<div style="text-align: center; margin-top: 2rem; margin-bottom: 2rem;">
    <iframe src="/assets/files/MISD.pdf" width="720" height="480" style="border: 1px solid #ccc; border-radius: 8px;"></iframe>
    <div class="caption">
        <strong>Project:</strong> Privacy preserving Synthetic Data Generation
    </div>
</div>
{% endraw %}
