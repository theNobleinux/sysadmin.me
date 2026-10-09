+++
title = "Linux User Onboarding and Offboarding"
weight = 4
projectType = "Lab"
summary = "Practise creating and closing Linux accounts from approved requests, with a record of what access changed."
challenge = "An incomplete request or copied permissions can give someone more access than they need. Old accounts can also be missed when someone leaves."
approach = "Use a sample request, role-based groups, and a Bash or Ansible workflow. Include checks for approval, account changes, and offboarding."
tags = ["Linux", "Bash", "Ansible", "Access Control", "Operations"]
+++

## Scenario

This lab covers a routine small-team task: giving a new colleague the access they need and keeping a record of the change.

## Challenge

When accounts are created by hand, it’s easy to miss approval, add the wrong group, or leave access active after it’s no longer needed.

## Approach

I’d check for an approved request, use role-based groups instead of copying another user’s access, and record each change. For offboarding, I’d disable the account, remove keys and group memberships, and handle files according to a written retention policy.

## Verification

I’d test with sample accounts in an isolated VM: confirm the right group access, check unrelated access is denied, repeat the request, and review the change log. I wouldn’t run it against real accounts without approval.
