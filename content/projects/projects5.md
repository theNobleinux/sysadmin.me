+++
title = "Ubuntu Server Access Audit and Hardening"
weight = 1
projectType = "Lab"
summary = "A practice exercise in reviewing Linux accounts, limiting admin access, and documenting a server security baseline."
challenge = "Over time, a server can collect unused accounts, broad sudo permissions, and inconsistent SSH settings. That makes it hard to tell who can access what."
approach = "In an Ubuntu Server VM, review users, groups, sudo rules, and SSH settings. Make least-privilege changes, then test the access paths and record what changed."
tags = ["Ubuntu Server", "Linux", "SSH", "sudo", "Security"]
+++

## Scenario

For this practice exercise, imagine taking over an Ubuntu server with incomplete account notes and unclear admin access. This is a lab, not client work.

## Challenge

Without an account and permission review, old accounts and excessive sudo access can go unnoticed. SSH also needs to be secure without locking out the people responsible for the server.

## Approach

1. List local users, groups, login shells, and sudo rules before making changes.
2. Confirm which accounts need admin access and remove permissions that are no longer needed.
3. Review SSH settings and test a separate admin login before ending the current session.
4. Make one change at a time and keep notes so it’s clear how to undo a mistake.

## Verification

Check that the right users can log in and use sudo, and that others cannot. Review the effective SSH settings and keep a before-and-after checklist. Only use these steps on a real server with approval and a recovery plan.
