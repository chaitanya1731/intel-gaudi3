# Intel® Gaudi® 3 AI Accelerator

## Introduction
Deep Learning and Artificial Intelligence workloads continue to demand higher 
performance and lower power consumption. This technical paper introduces the 
next generation AI accelerator from Intel and Habana Labs, an Intel company: the 
Intel® Gaudi® 3 AI accelerator. The new accelerator features the 5th generation of 
heterogenous AI acceleration architecture. The Intel® Gaudi® 3 accelerator was 
designed to provide state-of-the-art datacenter performance for all AI workloads, 
from generative applications such as large language models (LLMs) and diffusion 
models (image generation such as Stable Diffusion) to standard object recognition, 
classification, and voice dubbing. 
The Intel® Gaudi® 2 AI accelerator, introduced in 2022, is supported by the Intel® 
Gaudi® software suite, which integrates the PyTorch framework. With the Intel® 
Gaudi® 3 AI accelerator we provide the next level of AI performance and power 
efficiency. Advancing from the Intel® Gaudi® 2 accelerator 7nm process, the Intel® 
Gaudi® 3 accelerator is manufactured in TSMC 5nm process, which provides 
improved area density and power efficiency. 
Intel® Gaudi® 3 AI accelerator continues to push the boundaries of what is possible 
in performance and power efficiency. Built on the Intel® Gaudi® 2 accelerator 
architecture, Intel® Gaudi® 3 accelerator provides significant boosts in compute, 
memory bandwidth, and architectural efficiency.
The Intel® Gaudi® 3 AI accelerator features two compute dies, which together 
contain 8 MME engines, 64 TPC engines and 24x 200 Gbps RDMA NIC ports. In 
addition, the total of 8 HBM2e chips comprise a 128 GB unified High Bandwidth 
Memory (HBM).
The Intel® Gaudi® 3 AI accelerator excels at training and inference with 1.8 PFlops of 
FP8 and BF16 compute, 128 GB of HBM2e memory capacity, and 3.7 TB/s of HBM 
bandwidth.

## Overview
AI applications increasingly demand faster and more energy-efficient hardware 
solutions and the Intel® Gaudi® 3 accelerator was designed to answer the demand. 
With more than 2x FP8 GEMM FLOPs and more than 4x BF16 GEMM FLOPs 
compared to the Intel® Gaudi® 2 accelerator, Intel® Gaudi® 3 accelerator continues to 
provide state-of-the-art AI training performance. With 1.5x faster HBM bandwidth and 
1.33x larger HBM capacity, the Intel® Gaudi® 3 accelerator provides an order-of-magnitude improvement in large language model inference performance compared 
to the Intel® Gaudi® 2 accelerator.
The Intel® Gaudi® 3 accelerator (Figure 1) features two 
identical compute dies, connected through a high-bandwidth, 
low-latency interconnect over an interposer bridge. The die-to-die connection is transparent to the software, providing 
performance and behavior equivalent to that of a large unified 
single die. 
The Intel® Gaudi® 3 accelerator compute architecture is 
heterogeneous and includes two main compute engines – a 
Matrix Multiplication Engine (MME) and a fully programmable 
Tensor Processor Core (TPC) cluster. The MME is responsible 
for doing all operations that can be lowered to Matrix 
Multiplication, like fully connected layers, convolutions and 
batched-GEMMs. The TPC, a Very Long Instruction Word 
(VLIW) Single-Instruction Multiple-Data (SIMD) processor 
tailor-made for deep learning applications, is used to accelerate 
all non-GEMM operations. 


## Architecture
The image below shows the complete block diagram of the Intel® 
Gaudi® 3 AI accelerator. 
Each of the components in the chip are explained in detail in the 
next chapters.
Figure 8. Intel® Gaudi® 3 AI Accelerator with L2 cache for every 2 MME 
and 16 TPC unit. Parts of L2 can be configured by the Graph Compiler to 
serve as shared L3.

Full implementation of Intel® Gaudi® 3 accelerator includes the 
following units: 
• PCIe Gen5 X16 port for communicating with host
• Scheduling and Synchronization Unit
• 8 Matrix Multiplication Engines (MMEs)
• 64 Tensor Processor Cores (TPCs)
• 14 Media Decoder Engines (DECs)
• 4 Rotator Engines (ROT)
• 24 Network ports and the accompanied RDMA Engine
• 96 MB of L2 Cache
• 128 GB of 8 HBM2e stacks

Intel® Gaudi® 3 AI accelerator compute engines are split into four 
clusters. Each cluster is referred to as a DCORE (Deep Learning 
Core) and contains: 
• 2 Matrix Multiplication Engines (MMEs)
• 16 Tensor Processor Cores (TPCs)
• 24 MB of L2 Cache 
