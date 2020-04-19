---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "[CVPR 2020] PULSE: Self-Supervised Photo Upsampling via Latent Space Exploration of Generative Models"
subtitle: ""
summary: "Current super-resolution methods optimize on pixel-wise average correctness measures which lead to blurring. We present an alternative problem formulation that focuses on creating perceptually realistic images that downscale correctly. Our algorithm, PULSE, solves this problem by doing a self-supervised search of the outputs of a generative model for images that downscale correctly, leveraging some properties of high-dimensional Gaussians; this yields far better perceptual quality than previous methods."
authors: [Sachit Menon]
tags: [CVPR]
categories: []
date: 2020-04-18T23:47:05-04:00
lastmod: 2020-04-18T23:47:05-04:00
featured: true
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Example of PULSE's outputs."
  focal_point: "Smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

The primary aim of single-image super-resolution is to construct a high-resolution (HR) image from a corresponding low-resolution (LR) input. In previous approaches, which have generally been supervised, the training objective typically measures a pixel-wise average distance between the super-resolved (SR) and HR images. Optimizing such metrics often leads to blurring, especially in high variance (detailed) regions. We propose an alternative formulation of the super-resolution problem based on creating realistic SR images that downscale correctly. We present a novel super-resolution algorithm addressing this problem, PULSE (Photo Upsampling via Latent Space Exploration), which generates high-resolution, realistic images at resolutions previously unseen in the literature. It accomplishes this in an entirely self-supervised fashion and is not confined to a specific degradation operator used during training, unlike previous methods (which require training on databases of LR-HR image pairs for supervised learning). Instead of starting with the LR image and slowly adding detail, PULSE traverses the high-resolution natural image manifold, searching for images that downscale to the original LR image. This is formalized through the “downscaling loss,” which guides exploration through the latent space of a generative model. By leveraging properties of high-dimensional Gaussians, we restrict the search space to guarantee that our outputs are realistic. PULSE thereby generates super-resolved images that both are realistic and downscale correctly. We show extensive experimental results demonstrating the efficacy of our approach in the domain of face super-resolution (also known as face hallucination). Our method outperforms state-of-the-art methods in perceptual quality at higher resolutions and scale factors than previously possible.

This work has been accepted for publication at CVPR 2020. The full paper can be found at https://arxiv.org/abs/2003.03808. 
