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

This project progressed through a structured series focusing on developing a pipelined processor, designing caches, and integrating these components into a multi-core system.  

---

#### 1. Pipelined Processor Design
**Objective:**  
Design and implement a five-stage pipelined processor supporting the TinyRV2 ISA.  

**Workflow:**  
- **Baseline Processor (Stalling):**  
  Implemented a basic five-stage pipeline with stalling for hazard resolution.  
- **Alternative Processor (Bypassing):**  
  Added bypassing paths to resolve data hazards, reducing unnecessary stalls.  
- **Pipeline Stages:**  
  1. **F (Fetch):** Instruction fetch and PC increment.  
  2. **D (Decode):** Decode instructions, read registers, and handle jump targets.  
  3. **X (Execute):** Perform ALU operations, compute memory addresses, and branch comparisons.  
  4. **M (Memory Access):** Read/write data to memory.  
  5. **W (Writeback):** Write results back to registers.  
- **Hazard Mitigation:**  
  - Data hazards addressed through forwarding and stalls.  
  - Control hazards managed with squash logic in the decode stage&#8203;:contentReference[oaicite:0]{index=0}.  
- **Testing:**  
  Directed and randomized tests using Pytest for each pipeline stage and instruction.  

---

#### 2. Cache Design
**Objective:**  
Implement direct-mapped and set-associative caches to reduce memory access latency.  

**Workflow:**  
- **Baseline Cache:**  
  Direct-mapped, write-back, write-allocate cache with 256-byte capacity.  
- **Alternative Cache:**  
  Two-way set-associative cache to reduce conflict misses&#8203;:contentReference[oaicite:1]{index=1}.  
- **Cache Organization:**  
  - **Banked Design:** Supports multi-core by partitioning the cache into four banks, enabling concurrent access.  
  - **FSM Control:** Designed a finite-state machine (FSM) to manage cache states (idle, read, write, eviction, refill).  
- **Testing:**  
  - Functional-level model (FL) verified initial correctness.  
  - Unit tests covered cache hits, misses, evictions, and memory interactions.  

---

#### 3. Multi-Core System Design
**Objective:**  
Compose single-core and multi-core systems using the previously designed processor and cache components.  

**Workflow:**  
- **Single-Core System:**  
  - Integrated the pipelined processor with private instruction and data caches.  
  - Developed a sorting microbenchmark for single-threaded performance analysis&#8203;:contentReference[oaicite:2]{index=2}.  
- **Multi-Core System:**  
  - Composed four cores, each with private instruction caches, connected by a shared, banked data cache.  
  - Implemented a **ring network** to interconnect cores and caches.  
- **Ring Network:**  
  - Four routers connected in a loop, facilitating cache coherence and memory requests/responses.  
  - Messages traverse routers, with arbitration logic managing congestion.  
- **Testing:**  
  - Incremental testing of network components (routers, adapters).  
  - Full-system tests for memory coherence, network congestion, and correctness.  

---

#### Evaluation and Benchmarking
- **Metrics:**  
  - **Cycles Per Instruction (CPI):** Measured the efficiency of pipelining and bypassing mechanisms.  
  - **Throughput:** Evaluated single-threaded vs. multi-threaded sorting performance.  
  - **Memory Latency:** Analyzed cache access times and network latencies.  
- **Performance Comparison:**  
  - Compared baseline (single-core) and alternative (multi-core) designs using sorting benchmarks.  
  - Multi-core systems demonstrated reduced latency and improved throughput for parallel workloads.  

---

#### Future Plans
- **Optimization:**  
  - Implement more sophisticated cache replacement policies and improve network routing algorithms.  
  - Explore dynamic voltage and frequency scaling (DVFS) for energy-efficient multi-core operation.  
- **Advanced Benchmarking:**  
  - Apply the design to more complex multi-threaded benchmarks beyond sorting algorithms to evaluate real-world performance.
