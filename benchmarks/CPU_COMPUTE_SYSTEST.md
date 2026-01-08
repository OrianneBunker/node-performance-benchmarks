# CPU Compute Performance - AMD Threadripper 7960X

**Tool:** sysbench 1.0.20  
**Target:** Prime Number Calculation (Limit: 20,000)  
**Configuration:** 48 Threads (Full Parallelization)

### Execution Summary
The AMD Threadripper 7960X demonstrated exceptional multi-threaded performance, maintaining high stability across all 48 logical cores.

| Metric | Value |
| :--- | :--- |
| **Events per second** | 4343.27 |
| **Total Events** | 43,461 |
| **Avg Latency** | 11.00 ms |
| **95th Percentile Latency** | 69.29 ms |
| **Thread Fairness** | 905.43 events (stddev: 15.63) |

### Raw Output Snippet
```text
CPU speed:
    events per second:   4343.27

General statistics:
    total time:                          10.0063s
    total number of events:              43461

Latency (ms):
         min:                                    0.45
         avg:                                   11.00
         max:                                  142.47
```

### Analysis for Node Operations
The low standard deviation in thread fairness (15.63) confirms that the **NUMA-aware scheduling** and the Zen 4 architecture are handling high-concurrency tasks without significant jitter. This is critical for maintaining synchronization in high-TPS networks like Rise and MegaETH.
