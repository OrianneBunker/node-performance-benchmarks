# System Topology & Bus Connectivity

**Bus Type:** PCIe Gen 5 (Capable)  
**Host:** ASUS Pro WS TRX50-SAGE WIFI  
**P2P Interconnect:** NODE (Optimized PCIe Bridge Access)

### GPU-to-GPU Affinity Matrix
```text
        GPU0    GPU1    CPU Affinity    NUMA Affinity
GPU0     X      NODE    0-47            0
GPU1    NODE     X      0-47            0
```

### Technical Assessment
The topology report confirms that both RTX 5090 units are connected via a **NODE** link within the same NUMA domain (NUMA 0). 

**Significance:**
- **Latency:** Direct connected peer type prevents CPU-SMP bottlenecks (UPI/QPI traversal).
- **Bandwidth:** GPUs share the same PCIe Root Complex, allowing for high-speed data transfer between devices, essential for `TensorParallel` LLM orchestration.
- **PCIe Gen 5:** Hardware reports `Max Link Speed: 5` (32 GT/s), ensuring maximum throughput for data-heavy blockchain state updates.
