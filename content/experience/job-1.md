---
date: 2024-09-15T00:00:00+01:00
draft: false
title: "RA #1"
jobTitle: "Research Assistant on ML hardware accelerator"
company: "Computer Systems Laboratory "
location: "Ithaca, NewYork"
duration: "2024"

---


### High-Level Synthesis for Machine Learning Accelerators (Allo & Xilinx Vivado/Vitis)  
**Research Assistant under Prof. Christopher Batten – Sept 2024 - Present**  

The allo model we used on [GitHub](https://github.com/cornell-zhang/allo).

Our work focuses on designing and accelerating FPGA-based machine learning models using Allo, a Python-based domain-specific language (DSL) developed by the Cornell Computer Systems Laboratory. The primary goal is to optimize hardware accelerators for high-performance tasks in machine learning, genomics, and robotics by transforming PyTorch models into efficient FPGA implementations.  

---

#### Key Contributions  
1. **Model Development and Parity Testing:**  
   - Developed a Multi-Layer Perceptron (MLP) model in PyTorch for MNIST digit classification, ensuring accuracy through rigorous training and validation&#8203;:contentReference[oaicite:0]{index=0}.  
   - Exported weights and biases to Allo for direct performance comparisons.  

2. **Allo Integration and HLS Acceleration:**  
   - Recreated the MLP in Allo and synthesized it onto Xilinx Alveo U250 FPGA boards.  
   - Ensured inference accuracy matched the PyTorch model.  

3. **Optimization Techniques:**  
   - **Loop Optimizations:** Applied pipelining, unrolling, and reordering to reduce initiation intervals to 1, achieving single-cycle intervals in computation layers&#8203;:contentReference[oaicite:1]{index=1}.  
   - **Memory and Dataflow Enhancements:** Parallelized memory access through partitioning and buffering, increasing BRAM usage from 1% to 19%, with LUT/FF utilization rising from ~0% to 1%.  

4. **Performance Improvements:**  
   - Achieved **224x speedup** on MNIST MLP models by resolving loop dependencies and optimizing layer architectures.  
   - Ensured performance parity with PyTorch models by validating inference outputs element-wise.  

---

#### Future Work  
- **CycleGAN FPGA Deployment:**  
   - Porting CycleGAN models to Allo for FPGA deployment, focusing on balancing performance, area, and resource efficiency.  
   - Exploring kernel relay techniques and memory reuse to minimize latency during inference.  

- **Advanced HLS Techniques:**  
   - Refining HLS optimizations by integrating composable schedules, inter-kernel FIFOs, and loop fusion techniques.  
   - Targeting scalability across larger datasets and complex neural networks.  

This project pushes the boundaries of FPGA-based ML accelerators by leveraging Allo’s unique ability to decouple hardware optimization from algorithm development.  
