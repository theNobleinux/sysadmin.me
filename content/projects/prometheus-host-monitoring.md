+++
title = "Linux Host Monitoring with Prometheus"
weight = 5
projectType = "Lab"
summary = "Collect basic Linux host metrics and build a Grafana dashboard for CPU, memory, disk, and service availability."
challenge = "Without a few useful system metrics, it can be hard to tell whether an outage is related to CPU, memory, disk space, or a stopped service."
approach = "Run Prometheus and a host metrics exporter in a VM, then build a small Grafana dashboard and test a couple of alerts."
tags = ["Prometheus", "Grafana", "Linux", "Monitoring", "Troubleshooting"]
+++

## Scenario

I’d use a Linux VM and a sample service to practise spotting resource and availability problems.

## Challenge

Too many alerts quickly become background noise. Each one should point to a real condition and give someone a useful place to start.

## Approach

I’d collect CPU, memory, filesystem, and host availability metrics, then graph recent trends. I’d keep alerts focused on sustained problems and include what to check first.

## Verification

I’d create CPU and disk pressure in the disposable VM and check that the graphs and alerts respond. After the test, I’d restore the VM and adjust thresholds based on what was useful. These results would describe the lab, not production monitoring.
