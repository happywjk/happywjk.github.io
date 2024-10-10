---
date: 2024-09-15T00:00:00+01:00
draft: false
title: "pipeline processor"
jobTitle: "RISC-V pipeline processor"
company: "Cornell University "
location: "Ithaca, NewYork"
duration: "2024"

---
### Pipelined Processor Design and Evaluation using Verilog and PyMTL3

In my current work, I designed and implemented a five-stage pipelined processor supporting the TinyRV2 instruction set architecture (ISA) using Verilog and PyMTL3. This processor was designed in two microarchitectures: one using stalling to resolve data hazards and another that fully bypassed data using Software Predication, reducing the need for stalls. Both designs can correctly handle all kinds of hazard and interrupts/exception, ensuring that instructions flow smoothly through fetch, decode, execute, memory, and write-back stages without causing hazards or performance degradation.

I implemented a comprehensive testing strategy, focusing on unit tests for individual instructions, such as add, lw, and bne, and parameterized integration tests that validated instruction sets and memory operations. Utilizing pytest, I automated test generation and validation, ensuring the processors' correctness under a variety of conditions. This process included both directed and random testing strategies to simulate various real-world scenarios.

To evaluate performance, I conducted simulation-based analyses measuring cycles-per-instruction (CPI), instruction throughput, and memory latency. By benchmarking both the stalling and fully bypassed microarchitectures, I analyzed the trade-offs between simpler control logic and performance improvements. This comprehensive approach not only improved the designs' robustness but also provided insights into optimizing memory interfaces and processor pipelines for enhanced performance across different workloads​.