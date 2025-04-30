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

Our research centers around implementing a custom architecture, ShallowNet, which employs multiple parallel processing streams to potentially achieve competitive performance without the extensive depth typical of conventional deep learning models.

All experiments were conducted on the CIFAR10 dataset.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/VGG_Network.png" title="Shallow Net 3 Streams 1 Block" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The image on the left displays the architecture of our ShallowNet model, featuring three parallel processing streams with one VGG block in each stream. This design enables multi-resolution feature extraction while maintaining minimal depth.
</div>

## Model Configuration

### Baseline Deep Layer Models

| **Model Name** | **No. of Layers** | **No. of Parameters (Million)** | **Block Type** |
| -------------- | ----------------- | ------------------------------- | -------------- |
| VGGNet         | 7                 | 1.852                           | VGG            |

\*Table 1: Baseline Deep Layer Models\_

### Shallow Net Model Configuration

| **Model Name**               | **No. of Streams** | **No. of Blocks in each Stream** | **No. of Parameters (Million)** |
| ---------------------------- | ------------------ | -------------------------------- | ------------------------------- |
| ShallowModel 3Streams 1Block | 3                  | 1                                | 1.345                           |

\*Table 2: Variations of Shallow Net Models\_

## Results

### Baseline Model Performance

| **Model Name** | **Testing Accuracy (in Percentage)** |
| -------------- | ------------------------------------ |
| VGGNet         | 88.2                                 |

\*Table 1: Baseline Model's Testing Accuracy Figures\_

Examining the testing accuracy figures for the Shallow Net with VGG Block as their basic block.

### Shallow Net Model Performance

| **Model Name**                   | **Testing Accuracy (in Percentage)** |
| -------------------------------- | ------------------------------------ |
| **ShallowModel 3Streams 1Block** | **89.53**                            |

\*Table 2: Shallow Net Model's Testing Accuracy Figures\_
