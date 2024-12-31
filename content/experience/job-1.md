---
date: 2024-09-15T00:00:00+01:00
draft: false
title: "RA #1"
jobTitle: "Research Assistant on ML hardware accelerator"
company: "Computer Systems Laboratory "
location: "Ithaca, NewYork"
duration: "2024"

---
### Accelerator Design and Exploration using Allo and Xilinx Vivado/Vitis

The allo model we used on [GitHub](https://github.com/cornell-zhang/allo).

High-Level Synthesis for Machine Learning Accelerators (Allo & Xilinx Vivado/Vitis)
Research Assistant under Prof. Christopher Batten – Sept 2024 - Present

Our work focuses on designing and accelerating FPGA-based machine learning models using Allo, a Python-based domain-specific language (DSL) developed by the Cornell Computer Systems Laboratory. The primary goal is to optimize hardware accelerators for high-performance tasks in machine learning, genomics, and robotics by transforming PyTorch models into efficient FPGA implementations.

Key Contributions:
Model Development and Parity Testing:

We began by developing a Multi-Layer Perceptron (MLP) model using PyTorch for MNIST digit classification, ensuring its performance and accuracy through rigorous training and validation​
.
The model architecture consists of three fully connected layers with ReLU activations, dropout to mitigate overfitting, and SGD optimization. This model serves as the baseline for comparison after porting it to Allo.
Allo Integration and HLS Acceleration:

After training the PyTorch model, the weights and biases were exported and re-integrated into Allo, allowing direct comparison of inference accuracy and runtime between the PyTorch and Allo models​
.
Through Allo, the same MLP was recreated, and hardware synthesis was performed on Xilinx Alveo U250 FPGA boards.
Optimization Techniques:

Loop Optimizations: We applied pipelining, unrolling, and reordering to enhance throughput and reduce initiation intervals (II) to 1, achieving single-cycle intervals on computation layers​
.
Memory and Dataflow Enhancements: Techniques such as array partitioning and buffer creation helped parallelize memory access, boosting BRAM usage from 1% to 19%, while FF/LUT utilization increased from ~0% to 1%, reflecting a balance between performance and area​
.
Performance Improvements:

The optimized Allo model achieved a 224x speedup compared to the initial HLS MLP model by addressing loop dependencies across layers.
Inference results from both PyTorch and Allo models showed parity in accuracy, validated by confusion matrices and element-wise comparison to ensure computation consistency​
.
Future Work:
CycleGAN FPGA Deployment:

We are currently working on porting CycleGAN models to Allo, targeting FPGA deployment. The goal is to optimize the balance between performance, area, and resource efficiency while maintaining high accuracy for generative tasks.
The next steps involve exploring additional memory reuse and kernel relay techniques to minimize latency during CycleGAN inference​
.
Advanced HLS Techniques:

Further work will focus on refining HLS optimizations by integrating composable schedules, inter-kernel FIFOs, and advanced loop fusion techniques to enhance scalability across larger datasets and more complex neural networks​
.
This project reflects our ongoing efforts to push the boundaries of FPGA-based ML accelerators by leveraging Allo's unique capability to decouple hardware optimization from algorithm development.
