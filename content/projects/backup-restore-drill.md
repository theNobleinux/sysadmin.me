+++
title = "Automated Backup and Restore Drill"
weight = 6
projectType = "Lab"
summary = "Back up a sample service, check the archive, and practise restoring it somewhere clean."
challenge = "A backup command can finish without proving that the files are complete or that anyone knows how to restore them."
approach = "Write a small script to create a dated backup, check it, log the result, and remove old copies according to a simple retention rule."
tags = ["Linux", "Bash", "Backups", "Recovery", "Operations"]
+++

## Scenario

The point of this lab is to test the restore, not just the scheduled backup.

## Challenge

If the only copy is on the same machine, the archive is never checked, or the restore steps are unclear, a backup may not help when something breaks.

## Approach

I’d write a script that checks its prerequisites, creates a dated backup, records the result, and validates the archive. Old copies would only be removed according to a written retention period, and the test backup would be kept away from the sample service data.

## Verification

I’d restore into a clean test location, compare the files and service data, and write down any missing steps. I’d only report a restore time after actually running the drill.
