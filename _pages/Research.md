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

## Research Vision

The datacenter market continues to show exponential growth, driven by machine learning and artificial intelligence workloads that demand increasingly efficient data-centric systems. This requires sustainable and efficient green computing solutions. My research focuses on developing scalable and efficient storage systems that reduce carbon emissions while optimizing the memory/storage hierarchy with emerging technologies.

## Current Research Areas

### 🔋 Energy-Efficient Memory Systems for Sustainable Computing
**Focus**: Reducing power-hungry data movement in datacenter applications

Modern datacenters consume over 1% of global electricity, with memory systems accounting for up to 40% of system power. My research explores:
- **Processing-in-Memory (PIM)** architectures for LLM and HPC workloads
- **Computational storage devices** that process data near storage
- Thermal management strategies for high-density memory systems
- Carbon-aware memory allocation and scheduling

**Related Patents**:
- [US20200126624A1](https://patents.google.com/patent/US20200126624A1) - Reduces NAND block copy operations
- [US11269528B2](https://patents.google.com/patent/US11269528B2) - Optimizes NAND page read patterns
- [US20220179573A1](https://patents.google.com/patent/US20220179573A1) - Minimizes DRAM access frequency

### 🏗️ Memory/Storage Hierarchy with CXL and Emerging Technologies
**Focus**: Optimizing heterogeneous memory systems for AI and scientific computing

![image](https://user-images.githubusercontent.com/25541665/186185086-84dd2ae7-3d22-4229-9632-c39a746c23ca.png)

The emergence of CXL (Compute Express Link) enables new memory architectures that break traditional boundaries:
- **Memory tiering** strategies using CXL-attached memory expanders
- **Heterogeneous memory management** across DRAM, CXL memory, and SSDs
- Integration of **Storage Class Memory (SCM)** in the memory hierarchy
- **Byte-addressable** vs **block-addressable** memory optimization

### 🤖 Machine Learning Workload Optimization
**Focus**: Accelerating LLM and HPC performance on heterogeneous memory

Large Language Models and HPC applications present unique memory challenges:
- **LLM inference optimization** with CXL memory pooling
- **Memory-aware model partitioning** and placement

**Recent Publication**:
- ["The Hitchhiker's Guide to Programming and Optimizing Cache Coherent Heterogeneous Systems"](https://arxiv.org/abs/2411.02814) (2024)
  - Led CXL memory performance evaluation for LLM workloads
  - Analyzed CXL, NVLink-C2C, and AMD Infinity Fabric interconnects

### 🔗 Next-Generation Interconnects and Memory Disaggregation

Memory disaggregation promises better resource utilization and scalability:
- **CXL 3.0** memory pooling and sharing mechanisms
- **Multi-level memory** networks with fabric-attached memory
