# ConditionalGan-for-sketch-to-image-generation

![image](https://github.com/user-attachments/assets/70b22ea2-04b7-4a2b-b3e8-9c03bdc35858)

This repository contains a PyTorch implementation of a Conditional Generative Adversarial Network (cGAN) for converting face sketches into realistic human faces. The model is trained on a paired dataset of face sketches and real faces, enabling it to learn the conditional mapping from sketch domain to the real face domain.
Overview

This project demonstrates the ability of cGANs to perform image-to-image translation.
Input: Grayscale or binary face sketch images.
Output: Realistic human faces generated from the sketches.

The model uses a Conditional GAN architecture, where:

    The Generator transforms sketches into realistic images.
    The Discriminator ensures the generated images are indistinguishable from the ground truth.

Dataset

The model requires a paired dataset of face sketches and real face images. The dataset used for training can be obtained from public datasets like CUHK Face Sketch Database.

Model Architecture

The model employs the cGAN framework:

    Generator:
        A U-Net-based architecture that learns to map sketches to realistic images.
        Utilizes skip connections for preserving spatial features.

    Discriminator:
        A PatchGAN discriminator that evaluates the realism of generated patches.

Loss functions:

    Adversarial loss for the GAN objective.
    L1 loss between generated images and ground truth for image fidelity.

    
