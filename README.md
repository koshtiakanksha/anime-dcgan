# Anime DCGAN

This project implements a Deep Convolutional Generative Adversarial Network (DCGAN) to generate anime character images. The DCGAN is trained on a dataset of anime faces, allowing it to create unique and realistic anime characters. This README provides a quick overview, setup instructions, and explanations of each part of the code.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training Process](#training-process)
- [Results](#results)
- [References](#references)

## Overview
The goal of this project is to use a GAN (Generative Adversarial Network) to generate new anime faces. By training on thousands of anime images, the model learns patterns in the data and can generate new anime faces that mimic the training images.

**What’s included:**
- Data loading and preprocessing steps
- DCGAN model structure
- Training loop with evaluation
- Visualization of generated images

## Dataset
We used a dataset of anime character faces, which can be downloaded from [Anime Faces Dataset](https://www.kaggle.com/datasets/splcher/animefacedataset) (or any other source you used). The images are preprocessed to a size of 64x64 pixels and normalized for training.

## Model Architecture
This project uses a Deep Convolutional GAN (DCGAN) architecture, which consists of:
1. **Generator**: Generates images from random noise.
2. **Discriminator**: Classifies images as real (from dataset) or fake (from generator).

Both networks use convolutional layers to learn from the image data effectively. Leaky ReLU activation is used in the Discriminator, while the Generator uses ReLU activation.

## Training Process
The model is trained over multiple epochs. During each epoch:
1. **Noise is fed into the Generator** to produce fake images.
2. **Discriminator is trained** on both real and fake images.
3. **Loss is calculated** for both networks, and the weights are updated to improve results.

Training continues until the Generator produces realistic anime faces, and the Discriminator can’t easily tell if they’re fake.

## Results
Once training completes, the Generator creates high-quality anime face images. Below are sample images generated after training:

![image](https://github.com/user-attachments/assets/1fcf09e4-82e4-4a59-944c-76e34dfcdd92)


## References
- [DCGAN Paper](https://arxiv.org/abs/1511.06434)
- [PyTorch DCGAN Tutorial](https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html)
- [Link to the dataset](https://www.kaggle.com/datasets/splcher/animefacedataset)

---
