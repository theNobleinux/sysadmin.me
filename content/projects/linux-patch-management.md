+++
title = "Linux Patch Management and Change Log"
weight = 9
projectType = "Lab"
summary = "Update a disposable Linux VM in a planned sequence, then check that its services still work."
challenge = "Updates need to be applied, but changing packages without checking the impact can interrupt a service or make it hard to explain what changed."
approach = "Record the current package state, take a VM snapshot, apply updates during a planned window, and check key services and logs afterward."
tags = ["Linux", "Ubuntu", "Package Management", "Change Management", "Operations"]
+++

## Scenario

I’d use a VM running a sample web service to practise a routine maintenance window.

## Challenge

Without a before-and-after record and a few checks, it’s easy to miss a regression or forget which packages changed.

## Approach

I’d note the operating system and package state, review the updates, snapshot the VM, and apply them during a planned window. Afterward, I’d check service status, listening ports, recent logs, and whether the sample app responds.

## Verification

I’d record what changed and anything that went wrong. If a check failed, I’d practise reverting the snapshot and note what the rollback restored.
