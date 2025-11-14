# AutoEncoders
## Variational Autoencoder (VAE) and Gaussian Mixture Model VAE (GMM-VAE)

This repository contains implementations of:

- **Variational Autoencoder (VAE)**
- **Gaussian Mixture Model Variational Autoencoder (GMM-VAE)**  
  (also referred to as Mixture-of-Gaussians Prior VAE)

Both models are implemented from scratch using **PyTorch**, closely following the original research papers.

---

## 📄 Referenced Papers

### **1. Variational Autoencoder (VAE)**
**Paper:** *Auto-Encoding Variational Bayes*  
**Authors:** Kingma & Welling (2013/2014)  
**arXiv:** https://arxiv.org/abs/1312.6114  

This work introduces the VAE framework and the reparameterization trick for efficient gradient-based variational inference.

---

### **2. Gaussian Mixture VAE (GMM-VAE)**
**Paper:** *Deep Unsupervised Clustering with Gaussian Mixture Variational Autoencoders*  
**Authors:** Dilokthanakul et al., 2016  
**arXiv:** https://arxiv.org/abs/1611.02648  

This model extends VAEs by replacing the simple Gaussian prior with a **Gaussian mixture prior**, enabling multimodal latent representations and unsupervised clustering.

---

## 📌 Features Implemented

### ✔ Variational Autoencoder (VAE)
- Encoder outputs mean (μ) and log-variance (logσ²)  
- Reparameterization trick  
- Decoder for reconstruction  
- ELBO loss:  
  - Reconstruction term  
  - KL divergence term

### ✔ Gaussian Mixture Model VAE (GMM-VAE)
- Learnable Gaussian mixture prior  
- Latent variable decomposition:  
  - Categorical variable \(c\)  
  - Continuous variable \(z\) conditioned on \(c\)  
- KL terms:  
  - KL(q(c|x) || p(c))  
  - KL(q(z|x,c) || p(z|c))  
- Supports multimodal latent spaces and clustering

---
