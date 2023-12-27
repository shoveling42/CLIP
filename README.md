# Finetuning-CLIP

# Introduction

This repository is about finetuning CLIP and zero-shot classification via pre-trained CLIP.

# Prerequisites

Before you begin, ensure you have met the following requirements:

* Python 3.6 or later
* PyTorch 1.7.1 or later
* transformers and clip libraries installed
* Colab Pro V100 GPU or an equivalent GPU while fine-tuning CLIP
* [Wandb](https://wandb.ai/site)(NOT NECESSARY, it is used to track losses of text and image.)

# Experiments

## Dataset

In this project, you can download [Indo fashion dataset](https://www.kaggle.com/datasets/validmodel/indo-fashion-dataset).

The dataset is split into 3 section, that is, training, validation, and test. The total number of categories is 15. Each class is one kind of indo fashion categories.

|Training|Validation|Test|Total|
|---|---|---|----|
|91K|7.5K|7.5K|106K|

## Hyperparameter's Configuration

|Epochs|Batch sizes|Optimizer|Loss Function|
|---|---|---|----|
|30|256|Adam|Cross Entropy|

The hyperparameters used in Adam optimizer are below:

|learning rate|$B_1|$B_2|Weight Decay|
|---|---|---|----|
|5e-5|0.9|0.98|0.2|

# Result

![Quantative Result](https://github.com/shoveling42/CLIP/assets/65910972/5fbb747e-5c15-4d4e-8cde-286247f07a94)

# Reference

Inference code: [CLIP](https://github.com/openai/CLIP)
