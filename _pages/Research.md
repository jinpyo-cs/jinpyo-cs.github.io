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

My research focuses on **understanding and orchestrating heterogeneous memory systems** for emerging AI and scientific workloads (e.g., LLM serving, AlphaFold3) running across GPU HBM, host DRAM, and CXL-attached memory. My work first characterizes where capacity, bandwidth, and data movement limit performance, then uses those findings to build **runtime orchestration** that coordinates memory placement, data movement, and execution. Most recently, I built a system that dynamically repartitions GPU HBM between MoE expert weights and the KV cache in multi-turn LLM serving.

## Current Research

### Memory Management for MoE LLM Serving in Multi-Turn Agentic Workloads

Mixture-of-Experts (MoE) models activate only a few experts per token, yet serving systems keep the full expert set resident in GPU HBM. In multi-turn agentic workloads (e.g., coding agents), the reusable KV-cache footprint grows turn after turn and exhausts the fixed KV-cache pool, triggering evictions, costly re-prefills, and sharp time-to-first-token (TTFT) spikes.

I am developing a serving framework that **dynamically repartitions HBM between MoE expert weights and the KV cache**. When the KV-cache pool runs short, a cost model compares expert offloading, prefix-cache eviction, and request preemption using measured staging/recomputation costs and online-observed prefix reuse, then picks the cheapest action. HBM pages are remapped at runtime via CUDA virtual memory management, and offloaded experts are staged from host memory with double buffering. Implemented in vLLM and evaluated on Qwen3-Next-80B, this framework substantially lowers tail TTFT on recorded SWE-agent sessions while leaving low-reuse workloads unaffected.

**Preprint**:
- ["Dynamic HBM Repartitioning for Multi-Turn MoE Serving"](https://arxiv.org/abs/2609.13537) - **arXiv 2026**
  - **Jinpyo Kim**, Mingi Kwon, Younghoon Min, Jongryool Kim, Jishen Zhao

A follow-up and an open-source release are planned.

### Scientific Computing Workload Characterization

I study system-level bottlenecks in GPU-accelerated scientific applications to guide infrastructure design. My first work in this area focuses on **AlphaFold3**, systematically profiling its compute, memory, and scaling behavior across GPU configurations.

**Publication**:
- ["AlphaFold3 Workload Characterization: A Comprehensive Analysis of Bottlenecks and Performance Scaling"](https://cseweb.ucsd.edu/~jzhao/files/kim-iiswc2025.pdf) - **IISWC 2025**
  - **Jinpyo Kim**, Mingi Kwon, Jishen Zhao
  - [AFSysBench benchmark suite](https://github.com/stable-lab/AFSysBench)

## Previous Work

### LLM Serving Simulation

A **discrete-event simulator** that models the GPU serving stack — memory hierarchies (HBM/DRAM/Disk), tensor parallelism, interconnects (PCIe/NVLink), and vLLM-style scheduling (Continuous Batching, PagedAttention) — for system-level what-if analysis without exhaustive real-hardware experiments. Validated against H100 measurements with **1.5% micro-kernel error**.

## Other Research Interests

- **CXL and memory disaggregation** — heterogeneous memory tiering, cache coherence, and pooling for AI/HPC workloads
- **Non-volatile memory systems** — crash consistency, write ordering, and wear leveling for persistent memory
- **Interconnect characterization** — CXL, NVLink-C2C, AMD Infinity Fabric ([Heimdall benchmark suite](https://arxiv.org/abs/2411.02814))

## Tools

- [**AFSysBench**](https://github.com/stable-lab/AFSysBench) — AlphaFold3 workload profiling benchmark
- [**Heimdall**](https://arxiv.org/abs/2411.02814) — Cache-coherent heterogeneous system benchmark suite
