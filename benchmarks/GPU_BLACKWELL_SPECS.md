# GPU Infrastructure - Dual NVIDIA RTX 5090 (Blackwell)

**Node Profile:** High-Throughput AI Inference & ZK-Proving
**Status:** Verified Operational | Optimized PCIe 5.0 Topology
**OS:** Ubuntu 24.04 LTS (Headless Server)

## Core Specifications
| Component | Specification |
| :--- | :--- |
| **Architecture** | Blackwell (Compute Capability 10.0) |
| **Driver Version** | 590.48.01 (Pinned Production) |
| **CUDA Version** | 13.1 |
| **Total VRAM** | 64GB GDDR7 (32GB per unit) |
| **Interface** | Dual PCIe 5.0 x16 (Native CPU Lanes) |

## Hardware Inventory
- **GPU 0:** NVIDIA GeForce RTX 5090 (UUID: GPU-b8b0ddc5...)
- **GPU 1:** NVIDIA GeForce RTX 5090 (UUID: GPU-83738c00...)

## Thermal & Power Management
Optimized for sustained 24/7 heavy-load operations (Node Validation).

- **Active Cooling:** Liquid Cooled Baseline + Forced External Airflow (95% Fan Duty).
- **Idle Temp:** 27°C - 29°C (Ambient stabilized).
- **Power Limit:** 600.00 W per GPU (Sustained peak capability).
- **Max Clocks:** 3210 MHz (Verified under CUDA stress).

## Connectivity & Interconnect
Unlike standard multi-GPU setups, this node utilizes **Dual x16 Gen 5 slots** connected directly to the Threadripper 7960X Root Complex.

- **Bus Speed:** 32 GT/s per lane.
- **Topology:** NODE-level affinity within NUMA Domain 0.
- **P2P Status:** Enabled (Direct memory access via PCIe bridge).

## AI & Blockchain Capacity
This infrastructure is specifically tuned for:
1. **Parallel Execution Engines:** Ideal for Monad’s asynchronous execution due to ultra-low latency between GPUs.
2. **Large Language Models (LLM):** Capable of running DeepSeek-R1 / Llama-3 405B (Quantized) or 70B (Full) with massive context windows.
3. **ZK-Proving:** Accelerated Proof-of-Stake and Zero-Knowledge proof generation via CUDA 13.1 optimization.
