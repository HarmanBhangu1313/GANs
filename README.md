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
