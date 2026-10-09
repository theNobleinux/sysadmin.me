+++
title = "Ansible Linux Server Baseline"
weight = 3
projectType = "Lab"
summary = "Use Ansible to apply the same basic user, package, SSH, firewall, and service settings to fresh Linux hosts."
challenge = "Setting up each server by hand makes it easy for small differences and missed steps to build up."
approach = "Write a few focused Ansible roles, test them on disposable Ubuntu hosts, and run the playbook again to check whether it makes unnecessary changes."
tags = ["Ansible", "Ubuntu", "Linux", "Automation", "Hardening"]
+++

## Scenario

This lab explores how I’d set up a few new Linux servers with the same documented baseline.

## Challenge

The playbook should be easy to read, safe to run again, and clear about which settings are shared and which differ by host.

## Approach

I’d split the work into roles for packages, admin users, SSH, firewall rules, and services. Shared defaults and host-specific settings would be kept separate, and secrets would stay out of the repository.

## Verification

I’d run the playbook on disposable hosts, inspect the result, then run it again to catch unexpected changes. Before using it elsewhere, I’d document prerequisites, supported distributions, and how to recover if a change goes wrong.
