---
layout: archive
title: "Research Interest"
permalink: /Research/
author_profile: true
redirect_from:
  - /Research
---


{% include base_path %}

![datacenter_img](/images/datacenter.jpg)

The datacenter market will continue to show high growth. In addition, Machine learning and Artificial intelligence increase the demand for more efficient data-centric system. This requires sustainable and efficient green power solutions. The company I am currently working for(SK hynix inc.) is also adhering to eco-friendly management policy. In this context, my research focuses on scalable and efficient storage system for reducing carbon emissions and memory/storage hierarchy with proper emerging memory technologies.



Efficient storage system for reducing carbon emissions
======

As demand for data storage increases dramatically, storage continues to play a significant role in enterprise operation. In particular, energy consumption by cooling data center can be over 40% of total energy consumption of data center. From this point of view, reducing heat generation may be the most energy-efficient cooling method. For example, the more often the NAND Flash cells inside the SSD are written and read, the hotter they get. Decreasing write and read operation for NAND Flash cells is one of ways to improve SSD`s thermal issue. The objective of this research is to architect system to improve the power consumption and maintain performance and reliability.

  * Granted patent:
    * [US20200126624A1](https://patents.google.com/patent/US20200126624A1) (reduces NAND block copy)
    * [US11269528B2](https://patents.google.com/patent/US11269528B2) (reduces NAND page read)
  * Issued patent:
    * [US20220179573A1](https://patents.google.com/patent/US20220179573A1) (reduces DRAM access)  
  
  
Memory/storage hierarchy with proper emerging memory technologies
======

![image](https://user-images.githubusercontent.com/25541665/182406062-22a6faef-93f4-42a5-81c8-38fbc6468e76.png)

New and increasingly important data-centric workloads, such as AI/ML, IoT, and HPC demand tremendous throughput at a reasonable price. These cannot be handle by the current memory/storage hierarchy of DRAM and flash. A New memory/storage hierarchy that combines emerging memory technologies may be a solution. There are differential characteristics of memory devices such as DRAM, PMEM and Flash. These factors affect efficiency of memory/storage system which is consists of heterogeneous memories.

1) Granularity - Block vs Byte

2) Latency

3) Volatile and Non-volatile

Since heterogeneous memory architectures breaks system and software design based on conventional computer system, we need to redesign memory system considering memory heterogeneity and characteristics of memory technologies.

Recoverable persistent memory for crash consistency
======

![PM](https://user-images.githubusercontent.com/25541665/182413294-a7f7326f-0f73-4178-8d24-a01564dd79b0.png)

Maintaining the consistency of data on persistent memory requires data persistence, write ordering and transaction atomicity. The challenge of determining the optimal way to recover persistent memory from system crashes and power failures is driven by a trade-off between recovery time and overall performance. We need to seek an efficient manner to preserve persistent memory`s state before the crash.

  * Issued patent:
    * [US20220171542A1](https://patents.google.com/patent/US20220171542A1) (guarantees SSD`s data consisteny from frequent power loss)
 

