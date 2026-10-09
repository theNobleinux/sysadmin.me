+++
title = "Internal DNS Service and Troubleshooting"
weight = 8
projectType = "Lab"
summary = "Set up a private BIND zone for test machines and trace common name-resolution problems."
challenge = "A machine can be up and reachable by IP while applications still fail because of a bad record or resolver setting."
approach = "Create a private zone on an isolated network and use `dig` to check answers from both the DNS server and clients."
tags = ["BIND", "DNS", "Linux", "Networking", "Troubleshooting"]
+++

## Scenario

I’d create a private DNS zone for a few VMs so their hostnames resolve without changing public DNS.

## Challenge

The cause could be a typo in the zone file, a stopped service, a firewall rule, or a client using the wrong DNS server.

## Approach

I’d add a few records, check the configuration before reloading BIND, and limit queries to the lab network. I’d note each VM’s resolver setting and use `dig` to compare the server’s answer with the client’s.

## Verification

I’d test records that exist and ones that don’t, confirm only lab machines can query the server, and check the logs. After troubleshooting, I’d restore the known-good configuration.
