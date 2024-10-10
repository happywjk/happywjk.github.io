---
date: 2024-09-15T00:00:00+01:00
draft: false
title: "RA #1"
jobTitle: "Research Assistant on Allo"
company: "Computer Systems Laboratory "
location: "Ithaca, NewYork"
duration: "2024"

---
### Accelerator Design and Exploration using Allo and Xilinx Vivado/Vitis

The allo model we used on [GitHub](https://github.com/cornell-zhang/allo).

In my current project, I've been deeply involved in designing hardware accelerators using Allo, a Python-embedded domain-specific language from Zhiru Zhang’s group, with a focus on high-performance workloads in machine learning, genomics, and robotics. By mapping my current simple algorithm (character exact match) to an Alveo U250 FPGA using Xilinx Vivado/Vitis, I compared the performance against an Intel Xeon CPU, gaining insights into hardware acceleration benefits.

I’ve tackled challenges like handling varying input sizes and optimizing throughput using techniques such as pipelining, loop reordering, and parallel computing. These strategies have significantly improved the performance of algorithms like matrix multiplication, enabling the accelerator to efficiently scale up for large datasets. In particular, I optimized memory usage through buffer insertion and applied hardware parallelization to ensure efficient data processing across multiple streams.

In the future, I plan to explore the Allo-to-ASIC flow using Mentor CatapultC to understand FPGA-to-ASIC migration for long-term scalability. My upcoming design project will focus on creating more complex accelerators for machine learning or genomics, aiming to further optimize memory bandwidth, computation scheduling, and parallelism to meet real-world performance demands.