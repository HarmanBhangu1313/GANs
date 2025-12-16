# Generative Adversarial Network (GAN) 

A Python project implementing a Generative Adversarial Network (GAN) to generate realistic images based on a CIFAR-10 dataset.

---

##  Project Overview  
This project demonstrates how GANs work by training a Generator and Discriminator network in competition.  
The Generator tries to create realistic images, while the Discriminator learns to distinguish real from fake images.  
Example use case: generating handwritten digits (MNIST) or synthetic images.

---

##  Features  
- Data preprocessing (normalization, batching)  
- GAN architecture implemented in PyTorch  
- Training loop with loss visualization  
- Periodic sample image generation during training  
- Save generated images and trained models  

---
##  Mathematical Intuition (Generative Adversarial Networks – GANs)

###  Core Idea: Learning a Data Distribution
Generative Adversarial Networks (GANs) aim to **learn the underlying data distribution** so that new, realistic samples can be generated.

Instead of explicitly modeling the probability distribution, GANs learn it **implicitly** through a game between two neural networks.

---

###  Generator and Discriminator Roles
GANs consist of two competing models:

- **Generator (G):**
  - Takes random noise as input
  - Produces synthetic data (e.g., images)
  - Goal: generate samples that look real

- **Discriminator (D):**
  - Takes real or generated data as input
  - Outputs a probability of the data being real
  - Goal: distinguish real samples from fake ones

The two networks improve by competing with each other.

---

###  Adversarial Training as a Game
Training GANs is framed as a **two-player minimax game**:

- The discriminator tries to correctly classify real vs fake data
- The generator tries to fool the discriminator

As training progresses:
- The discriminator becomes better at detection
- The generator learns to produce more realistic samples

Ideally, the generator reaches a point where the discriminator cannot reliably tell real from fake.

---

###  Learning Signal and Optimization
The discriminator provides a **learning signal** to the generator:
- If fake samples are easily detected, the generator adjusts its parameters
- If fake samples look realistic, the generator is rewarded

This indirect feedback allows the generator to learn complex structures in the data without explicit labels.

---

###  Why GAN Training Is Unstable
GAN training is challenging because:
- The generator and discriminator must stay balanced
- If the discriminator becomes too strong, the generator stops learning
- If the generator collapses, it may produce very similar samples (mode collapse)

Architectural constraints (as in DCGAN) and training heuristics help stabilize learning.

---

###  What GANs Learn
Rather than memorizing data, GANs learn:
- High-level structure
- Texture and spatial relationships
- Variations within the data distribution

This makes GANs suitable for tasks like image generation, data augmentation, and simulation.

---

### Key Limitation
GANs:
- Do not provide explicit likelihoods
- Are sensitive to hyperparameters
- Can be difficult to evaluate quantitatively

Despite this, they remain powerful tools for realistic data generation.

---

##  Tech Stack  
- Python 3.10  
- PyTorch (optimized for M2 Mac)  
- NumPy, Pandas  
- Matplotlib  
- Jupyter Notebook  

---

##  Installation & Usage  

1. Clone this repo:  
   ```bash
   git clone https://github.com/harmansingh/gan-image-generation.git

   pip install -r requirements.txt
