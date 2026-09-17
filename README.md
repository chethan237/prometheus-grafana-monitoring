# Prometheus & Grafana Monitoring

## Project Overview

This project demonstrates system monitoring using Prometheus, Node Exporter, and Grafana.

## Tools Used

- Prometheus
- Node Exporter
- Grafana
- Docker
- Ubuntu
- PromQL

## Architecture

Ubuntu Host
   |
   +-- Node Exporter :9100
   |
   +-- Prometheus :9090
   |
   +-- Grafana :3000

## Prometheus Configuration

Prometheus collects metrics from:

- Prometheus itself
- Node Exporter

Configuration file:
prometheus/prometheus.yml

## PromQL Queries

The project includes queries for:

- CPU Usage %
- Memory Usage %
- Disk Usage %
- Node Exporter Status

Detailed queries and explanations are available in:
promql/queries.md

## Grafana Dashboard

The Grafana dashboard contains monitoring panels for:

- CPU Usage
- Memory Usage
- Disk Usage
- Node Exporter Status

Dashboard Name:
Prometheus Node Monitoring

## Alerting

Alert Name:
Node Exporter Down

Query:

up{job="node_exporter"}

Condition:

A is below 1

The alert was tested by stopping Node Exporter. Grafana successfully changed the alert state to FIRING.

## Verification

Prometheus Targets:

- prometheus - UP
- node_exporter - UP

Grafana dashboard successfully displays system metrics.

## Project Structure

prometheus-grafana-monitoring/
├── alerts/
│   └── node-exporter-down.md
├── prometheus/
│   └── prometheus.yml
├── promql/
│   └── queries.md
├── screenshots/
└── README.md

## GitHub Repository

https://github.com/chethan237/prometheus-grafana-monitoring
