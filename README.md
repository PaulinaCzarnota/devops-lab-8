This repository contains my Lab 8 - Grafana and Prometheus solution for the Introduction to DevOps module in the third year of the Computer Science course at TU Dublin.

# Overview

The aim of this lab was to set up a monitoring stack on a local Windows machine using **Windows Exporter**, **Prometheus**, and **Grafana**. The setup enables real-time visualization of system metrics, such as CPU and network usage. Prometheus collects and stores metrics from the exporter, while Grafana queries and displays them through a customizable dashboard.

All components were deployed using **Docker**, and proper configurations were made via the `prometheus.yml` file to ensure correct data flow and monitoring.

# Key Tasks

- Installed and ran **Windows Exporter**, verified metrics at `localhost:9182/metrics`.
- Created a `prometheus.yml` configuration file to scrape metrics from Windows Exporter and Prometheus.
- Deployed **Prometheus** using Docker and verified its UI at `localhost:9090`, confirming both targets were UP.
- Ran a PromQL **network usage query** in the Prometheus web UI using `rate(windows_net_bytes_received_total[1m])`.
- Deployed **Grafana** using Docker and accessed it via `localhost:3000`.
- Added Prometheus as a **data source** in Grafana and tested the connection successfully.
- Built a **CPU usage graph** in Grafana using `rate(windows_cpu_time_total{mode="user"}[30s])`, enabled **auto-refresh**, and confirmed real-time metric updates.
