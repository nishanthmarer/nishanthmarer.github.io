---
layout: page
title: Emperical Risk Minimization vs. Multi-Layer Perceptron
description: Quantitative performance benchmarking between statistical and neural approaches
img: assets/img/ERM_MLP.png
importance: 4
category: work
related_publications: false
github_url: https://github.com/nishanthmarer/ITMLPRFinalProjectAlex_Nishanth
---

Analyze a data set of all NFL games outcomes since the year 2000.

Specifically, we started with the preprocessed generated from this github repository: https://github.com/ukritw/nflprediction.

Our goal was to see if an artificial neural network could approach the Empirical Risk Minimization (ERM) estimate for this data to predict the outcome of each game.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/CM_ERM.png" title="Confusion Matrix" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/MLP_Plot.png" title="MLP vs. ERM Performance Plot" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <strong>Left:</strong> Confusion Matrix depicting the classification performance of the ERM.  
    <strong>Right:</strong> Empirical Probability of Error comparing the ERM and MLP models.
</div>

{% raw %}
<div style="text-align: center; margin-top: 2rem; margin-bottom: 2rem;">
    <iframe src="assets/files/ERM_vs_MLP_Presentation.pdf" width="720" height="480" style="border: 1px solid #ccc; border-radius: 8px;">
        This browser does not support PDFs. Please download the PDF to view it: 
        <a href="assets/files/ERM_vs_MLP_Presentation.pdf">Download PDF</a>.
    </iframe>
    <div class="caption">
        <strong>Presentation:</strong> Empirical Risk Minimization vs. Multi-Layer Perceptron
    </div>
</div>
{% endraw %}