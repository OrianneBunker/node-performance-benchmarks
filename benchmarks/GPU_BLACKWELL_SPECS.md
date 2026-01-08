# GPU Infrastructure - Dual NVIDIA RTX 5090 (Blackwell)

**Architecture:** Blackwell (Compute Capability 10.0+)  
**Driver Version:** 590.48.01  
**CUDA Version:** 13.1  
**VRAM Total:** 64GB (32GB per unit)

### Hardware Identification
- **GPU 0:** NVIDIA GeForce RTX 5090 (UUID: GPU-b8b0ddc5...)
- **GPU 1:** NVIDIA GeForce RTX 5090 (UUID: GPU-83738c00...)

### Power & Thermal Profiles
- **Default Power Limit:** 600.00 W per GPU.
- **Current Idle Temp:** 27°C - 29°C (Liquid Cooled Baseline).
- **Max Clocks:** 3210 MHz (SM / Graphics).

### AI & ZK Capacity
With a combined **64GB of GDDR7 VRAM**, this node is capable of:
1. **Large Scale Inference:** Running DeepSeek-R1 / Llama-3 70B models with high context windows in-memory.
2. **Parallel Proving:** Generating Zero-Knowledge proofs using dual-GPU acceleration via CUDA 13.1.
3. **High Throughput:** Massive parallelization for tensor-intensive operations.

---
*Status: Verified Operational under Ubuntu 24.04 LTS (Headless).*
