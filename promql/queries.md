# PromQL Queries

## 1. CPU Usage %

Query:
100 * (1 - avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])))

Explanation:
Shows the CPU usage percentage of the monitored system.

## 2. Memory Usage %

Query:
100 * (1 - node_memory_MemAvailable_bytes / node_memory_MemTotal_bytes)

Explanation:
Shows the percentage of used memory.

## 3. Disk Usage %

Query:
100 * (1 - node_filesystem_avail_bytes{mountpoint="/",fstype!~"tmpfs|overlay"} / node_filesystem_size_bytes{mountpoint="/",fstype!~"tmpfs|overlay"})

Explanation:
Shows the percentage of used disk space.

## 4. Node Exporter Status

Query:
up{job="node_exporter"}

Explanation:
Returns 1 when Node Exporter is reachable and 0 when Node Exporter is down.




