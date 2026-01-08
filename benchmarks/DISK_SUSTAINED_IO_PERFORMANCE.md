# Sustained I/O Performance - Gen5 NVMe (Raw Block Access)

**Tool:** fio 3.36  
**Target:** 4TB Gen5 NVMe (Raw Device: `/dev/nvme0n1`)  
**Configuration:** 50-minute Stress Test | Mixed Random RW (50/50) | IO Depth: 64

### Executive Summary
This benchmark was designed to test thermal stability and I/O consistency over an extended period (50 minutes), simulating the extreme pressure of a high-throughput blockchain state database (e.g., MonadDB).

| Metric | Read | Write |
| :--- | :--- | :--- |
| **IOPS (Average)** | 282k | 282k |
| **Bandwidth** | 1103 MiB/s | 1103 MiB/s |
| **Total I/O** | 3232 GiB | 3232 GiB |
| **Avg Latency** | 486.64 us | 409.33 us |

### Latency Distribution (clat)
The drive maintains sub-millisecond latency for **95.0%** of all requests even under 100% utilization.

- **50th Percentile:** 251 us (Read) / 192 us (Write)
- **99th Percentile:** 3.35 ms (Read) / 3.26 ms (Write)
- **99.99th Percentile:** 10.4 ms (Max jitter)

### Thermal & Stability Analysis
The drive sustained a constant **282k IOPS per operation type (564k total IOPS)** without thermal throttling. This confirms that the Bunker's active cooling system is capable of handling the sustained power draw of Gen5 storage architecture in a production-like environment.

### Significance for Monad & Rise Chain
- **Zero-Sync Lag:** High IOPS ensure the node never falls behind the tip of the chain during high-gas events.
- **Raw Device Optimization:** Testing on the raw block device demonstrates the baseline performance required for Monad’s parallel execution engine.
