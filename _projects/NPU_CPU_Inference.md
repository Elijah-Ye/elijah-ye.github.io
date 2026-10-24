---
layout: page
title: NPU-CPU LLM Inference
description: Furiosa RNGD NPU + Intel AMX cooperative inference for Llama 3.1 8B
img: assets/img/npu_cpu_policy2.png
importance: 1
category: work
github: https://github.com/Elijah-Ye/ECE527_FinalProject_Code
related_publications:
---

By the collaboration of [Elijah Ye](https://elijah-ye.github.io) and Frey Zhao <br>
UIUC ECE527 FA25 | August 2025 ~ December 2025

For the benchmark code, please see the project github repository at this [link](https://github.com/Elijah-Ye/ECE527_FinalProject_Code).

## Overview

High-end GPUs are expensive to buy and run, with TDPs of 300-700W. This project explores NPU-CPU cooperative computing, pairing the Furiosa RNGD NPU (180W TDP) with Intel Advanced Matrix Extensions (AMX) on Sapphire Rapids as a power-efficient alternative to GPU-only inference of Llama 3.1 8B.

I led the project and designed an analytical performance model that partitions inference between the NPU and the CPU by arithmetic intensity and batch size, predicting end-to-end latency from measured component latencies.

## Adaptive Partitioning Policies

- **Policy 1 (CPU-only, small batch):** CPU with AMX computes all layers. Best for batch size 1 thanks to 20× faster model loading.
- **Policy 2 (hybrid, medium batch):** CPU handles memory-bound operations and the NPU handles compute-bound ones. Only 12% average latency degradation vs. H100 at batch sizes 4 and 16, with 2.6× lower total system power (330W vs 850W).
- **Policy 3 (NPU-only, large batch):** 16.8% degradation at batch size 64 with 3.9× lower accelerator power.

{% include figure.html path="assets/img/npu_cpu_policy2.png" title="Policy 2 end-to-end latency" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    Policy 2 (hybrid NPU+CPU) end-to-end latency vs. GPU across batch sizes 4 and 16.
</div>

## Results

Overall, the NPU-CPU system delivers 2× better power efficiency than GPU-only systems, and a three-year total cost of ownership analysis projects 23-40% lower cost than H100-based systems.
