# Node Exporter Down Alert

## Alert Name
Node Exporter Down

## Query
up{job="node_exporter"}

## Condition
A is below 1

## Evaluation
- Evaluation interval: 10 seconds
- Pending period: 30 seconds

## Description
Node Exporter has stopped responding to Prometheus.

## Notification
Contact point: Grafana Lab

## Verification
Node Exporter was stopped.
Prometheus detected the target as DOWN.
Grafana changed the alert state to FIRING.
Node Exporter was started again after testing.
