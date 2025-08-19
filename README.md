# Adversarial-Robustness-CORnetS

This repository contains my research and experimentation on improving the adversarial robustness of deep neural networks, with a focus on **CORnet-S**, a lightweight, biologically-inspired model of the primate ventral visual stream.  

Over the course of my work, I explored training techniques, adversarial attack methods, and architectural innovations to make CORnet-S more reliable for real-world applications in computer vision.

## Key Projects

### 1. Baseline Training & Blurry-to-Clear (BTC) Method
- **ResNet18 on MNIST** with BTC training  
- **AlexNet on MNIST** with BTC training  
- **CORnet-S on MNIST** with BTC training  

### 2. Denoising & Robustness Testing
- **CORnet-S with denoising tests** on MNIST  
- Evaluated against **FGSM, PGD, CW, and Patch Attacks**  

### 3. CORnet-S with BTC on ImageNet100
- Adapted blurry-to-clear training for ImageNet100  
- Compared standard CORnet-S with BTC-trained CORnet-S under adversarial conditions  

### 4. Adversarial Benchmarks Across Architectures
- **AlexNet, ResNet18, and CORnet-S trained on:**
  - MNIST  
  - CIFAR-100  
  - ImageNet-100  
- Evaluated against:
  - **FGSM** (Fast Gradient Sign Method)  
  - **PGD** (Projected Gradient Descent)  
  - **CW** (Carlini-Wagner)  
  - **Patch Attacks**

##  Novel Contributions in CORNet-S_RD_V2

My modified CORNet-S architecture includes several innovations designed to improve adversarial robustness:

1. **Learnable Input Prefilter**  
   - A 1x1 convolution layer that acts as a trainable preprocessing step.  
   - Helps suppress noise and adversarial perturbations before they propagate through the network.  

2. **Gated Recurrent Blocks**  
   - Iteratively refine feature maps over multiple timesteps.  
   - Introduce temporal-style gating into a CNN backbone to stabilize activations against adversarial distortions.  

3. **Residual Denoise Block with Adaptive Scaling**  
   - Applies residual denoising while learning the optimal balance between raw and denoised features.  
   - Prevents over-smoothing and improves generalization under different attack types.   

### Results
- Achieved **+10% adversarial robustness** compared to baseline CORnet-S  
- Increased adversarial accuracy up to **97.87%** under evaluated threat models  
- Maintained lightweight and biologically plausible design  

## Why This Matters

- **CORnet-S** is already a game-changing architecture in computer vision, combining biological inspiration with computational efficiency.  
- My enhanced version makes it **significantly more adversarially robust**, allowing it to be applied in **real-world, security-critical settings** such as medical imaging, robotics, and autonomous systems.  
- This work provides a foundation for **other researchers and engineers** who want to leverage CORnet-S while ensuring robustness against adversarial attacks.  

## Reference
The original CORNet-S repository: 
https://github.com/dicarlolab/CORnet
