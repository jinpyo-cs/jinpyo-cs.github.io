---
layout: archive
title: "Research"
permalink: /Research/
author_profile: true
redirect_from:
  - /Research
---


{% include base_path %}

![datacenter_img](/images/datacenter.jpg)

## Research Overview

My research focuses on **memory and storage systems** for datacenter-scale workloads. I build simulation and profiling tools to understand performance bottlenecks across the GPU memory hierarchy, interconnects, and emerging technologies like CXL — with the goal of guiding efficient system design for AI and scientific computing.

## Current Research

### Memory Hierarchy Optimization for LLM Inference

LLM inference is increasingly **memory-bound**: KV cache growth from long contexts, multi-turn interactions, and multi-agent workloads competes for scarce HBM, while communication overheads (MoE routing, all-reduce) are tightly coupled with parallelism policies.

I am building a **high-fidelity discrete-event simulator** that models the full GPU serving stack — memory hierarchies (HBM/DRAM/Disk), tensor parallelism, interconnects (PCIe/NVLink), and vLLM-style scheduling (Continuous Batching, PagedAttention) — to enable system-level what-if analysis without exhaustive real-hardware experiments. The simulator is validated against real H100 measurements with **1.5% micro-kernel error** and nsys-comparable component metrics.

### Scientific Computing Workload Characterization

I study system-level bottlenecks in GPU-accelerated scientific applications to guide infrastructure design. My first work in this area focuses on **AlphaFold3**, systematically profiling its compute, memory, and scaling behavior across GPU configurations.

**Publication**:
- ["AlphaFold3 Workload Characterization: A Comprehensive Analysis of Bottlenecks and Performance Scaling"](https://cseweb.ucsd.edu/~jzhao/files/kim-iiswc2025.pdf) - **IISWC 2025**
  - **Jinpyo Kim**, Mingi Kwon, Jishen Zhao
  - [AFSysBench benchmark suite](https://github.com/stable-lab/AFSysBench)

## Other Research Interests

- **CXL and memory disaggregation** — heterogeneous memory tiering, cache coherence, and pooling for AI/HPC workloads
- **Non-volatile memory systems** — crash consistency, write ordering, and wear leveling for persistent memory
- **Interconnect characterization** — CXL, NVLink-C2C, AMD Infinity Fabric ([Heimdall benchmark suite](https://arxiv.org/abs/2411.02814))

## Tools

- [**AFSysBench**](https://github.com/stable-lab/AFSysBench) — AlphaFold3 workload profiling benchmark
- [**Heimdall**](https://arxiv.org/abs/2411.02814) — Cache-coherent heterogeneous system benchmark suite
