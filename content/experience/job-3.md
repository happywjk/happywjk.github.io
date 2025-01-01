---
date: 2024-09-09T00:00:00+01:00
draft: false
title: "GAN-Based Image Transformation System"
jobTitle: " GAN-Based Image Transformation System"
company: "Cornell University "

duration: "2024"

---
### GAN-Based Image Transformation System   

The project focuses on developing a portable GAN-based image transformation system using a Raspberry Pi 4, Pi camera, and PiTFT touchscreen. The goal was to capture images, apply transformations (such as day-to-night conversion), and display results in real time through a user-friendly interface.  

---

#### System Setup  
- Configured the Raspberry Pi with Raspbian OS and installed PyTorch.  
- Enabled touch control on the PiTFT and verified functionality.  

---

#### Model Development  
- **Conditional GAN (CGAN):**  
  - Developed using convolutional layers to generate labeled digit images (initially trained on MNIST).  
  - Transitioned from linear to convolutional layers for handling high-resolution inputs.  
  
- **Pix2Pix for Day-to-Night Transformation:**  
  - Implemented a U-Net-based Pix2Pix model for paired image-to-image translation.  
  - Preprocessed 18,000 paired images (resizing, color jitter, horizontal flip).  
  - Trained the model for 400 epochs using multi-GPU setups (GTX 1080, TITAN Xp, RTX 3090).  
  
- **Multi-GPU Training:**  
  - Training scripts were modified to utilize multiple GPUs, accelerating processing.  

---

#### Integration  
- Developed a Python interface for the Pi camera, enabling one-click image capture and transformation through the PiTFT.  
- Integrated trained GAN models to allow real-time transformations on the PiTFT screen.  

---

#### Testing and Validation  
- **Conditional GAN:** Successfully generated digit images from MNIST.  
- **Pix2Pix:** Initial results for day-to-night transformation were blurry, requiring refinement.  
- **Challenges:**  
  - Long training times, even with multi-GPU setups.  
  - Blurry outputs from Pix2Pix, necessitating hyperparameter tuning.  

---

#### Results  
- **Successes:**  
  - Deployed Conditional GAN and Pix2Pix models for image transformations.  
  - Demonstrated real-time GAN operation on embedded hardware.  
- **Limitations:**  
  - Pix2Pix outputs needed additional tuning for improved clarity.  

---

#### Future Work  
- Further refine the Pix2Pix model and explore alternative architectures.  
- Automate hyperparameter tuning and leverage transfer learning.  
- Expand transformation capabilities with additional styles and effects.  
