---
layout: page
title: Shallow Net
description: Shallow Convolutional Neural Network for Image Classification
img: assets/img/VGG_Network.png
importance: 3
category: work
related_publications: false
github_url: https://github.com/nishanthmarer/Shallow_Networks
---

This study explores an alternative approach by investigating the potential of shallow neural networks that expand horizontally by increasing width and resolution while maintaining minimal depth.

The main idea here is to utilise the concept of frequency decomposition technique typically used in the signal processing for analyzing a signal at different frequencies.

Similarly, the model performs convolutions simultaneously across different resolutions. This parallel processing allows the feature maps generated from each resolution to be preserved rather than diminished through successive convolutions.

By maintaining the feature maps from each stream, the network retains critical information about the input image at various resolution. This preservation of features enhances the model's ability to learn complex patterns without losing valuable details that might be obscured in deeper architectures.

The concatenated outputs, containing information from various resolutions, provide the fully connected layer with a comprehensive view of the feature patterns present in the image. This multi-resolution approach enhances the model's classification performance by leveraging diverse insights from the input data.

The research centers around implementing a custom architecture, ShallowNet, which employs multiple parallel processing streams to potentially achieve competitive performance without the extensive depth typical of conventional deep learning models.

All experiments were conducted on the CIFAR10 dataset.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/VGG_Network.png" title="Shallow Net 3 Streams 1 Block" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The image displays the architecture of the ShallowNet model, featuring three parallel processing streams with one VGG block in each stream. This design enables multi-resolution feature extraction while maintaining minimal depth.
</div>

##### <strong>Model Configuration</strong>

###### Baseline Deep Layer Models

<table class="table">
  <thead>
    <tr>
      <th scope="col">Model Name</th>
      <th scope="col">No. of Layers</th>
      <th scope="col">No. of Parameters (Million)</th>
      <th scope="col">Block Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>VGGNet</td>
      <td>7</td>
      <td>1.852</td>
      <td>VGG</td>
    </tr>
  </tbody>
</table>
<div class="caption">
    Table 1: Baseline Deep Layer Models
</div>

###### Shallow Net Model Configuration

<table class="table">
  <thead>
    <tr>
      <th scope="col">Model Name</th>
      <th scope="col">No. of Streams</th>
      <th scope="col">No. of Blocks in each Stream</th>
      <th scope="col">No. of Parameters (Million)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ShallowModel 3Streams 1Block</td>
      <td>3</td>
      <td>1</td>
      <td>1.345</td>
    </tr>
  </tbody>
</table>
<div class="caption">
    Table 2: Variations of Shallow Net Models
</div>

#### <strong>Results</strong>

###### Baseline Model Performance

<table class="table">
  <thead>
    <tr>
      <th scope="col">Model Name</th>
      <th scope="col">Testing Accuracy (in Percentage)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>VGGNet</td>
      <td>88.2</td>
    </tr>
  </tbody>
</table>
<div class="caption">
    Table 3: Baseline Model's Testing Accuracy Figures
</div>

Examining the testing accuracy figures for the Shallow Net with VGG Block as their basic block.

###### Shallow Net Model Performance

<table class="table">
  <thead>
    <tr>
      <th scope="col">Model Name</th>
      <th scope="col">Testing Accuracy (in Percentage)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>ShallowModel 3Streams 1Block</strong></td>
      <td><strong>89.53</strong></td>
    </tr>
  </tbody>
</table>
<div class="caption">
    Table 4: Shallow Net Model's Testing Accuracy Figures
</div>
