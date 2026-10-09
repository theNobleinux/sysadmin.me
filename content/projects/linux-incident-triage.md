+++
title = "Linux Service Incident Triage"
weight = 10
projectType = "Lab"
summary = "Break a sample systemd service in a VM, investigate the logs, and work through its recovery."
challenge = "A failed service might be caused by its configuration, a missing dependency, file permissions, or a resource problem. Changing several things at once can hide the cause."
approach = "Reproduce one failure, check systemd and journal output, and change one thing at a time."
tags = ["systemd", "journalctl", "Linux", "Troubleshooting", "Incident Response"]
+++

## Scenario

I’d use a sample systemd service in a disposable VM to practise working through an outage without guessing.

## Challenge

The service status or a failed local request is only the starting point; the cause might be a bad config, missing dependency, permissions, or a full resource.

## Approach

I’d note what failed and when, then check `systemctl status`, relevant `journalctl` entries, dependencies, permissions, and resource use. I’d make one reversible change at a time and keep a short timeline.

## Verification

I’d confirm the service is running, test its local endpoint, and look for recurring errors. Then I’d write a short handover explaining the cause, fix, and what might prevent the same problem.
