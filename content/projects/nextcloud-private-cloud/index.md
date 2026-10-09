+++
title = "Nextcloud Private Cloud and Disaster Recovery"
date = 2026-10-06
weight = 2
projectType = "Completed project"
summary = "A multi-container Nextcloud and MariaDB deployment focused on service isolation, persistent storage, troubleshooting, and a tested database recovery path."
challenge = "The Nextcloud and MariaDB services needed to communicate reliably while keeping database storage persistent; setup also exposed a browser session issue and the need for a dependable recovery procedure."
approach = "Used Docker Compose to connect the application and database on an isolated network, persist data in named volumes, correct trusted-domain and connectivity settings, and create a database-dump-based recovery script."
tags = ["Docker Compose", "Nextcloud", "MariaDB", "Linux", "Disaster Recovery"]
+++

## What I built

I set up Nextcloud and MariaDB as separate services with Docker Compose. I wanted the database and app data to survive container restarts, and to have a recovery process I could test.

## Challenge

At first, the containers could not communicate as expected, and a browser cookie loop got in the way of testing the web interface. I also needed to make sure the data would persist and could be restored.

## Approach

- Connected the services on a dedicated Docker Compose network.
- Put app and database data in named `nextcloud_data` and `db_data` volumes so recreating containers would not erase it.
- Fixed the `trusted_domains` setting and traced the container connection issue instead of reinstalling everything.
- Used a private browsing session to get past the cookie issue and check the app.
- Wrote a database dump and restore script and tried it out; the recovery run took under two minutes.

## What I learned

I learned to check service names, network settings, volumes, and startup dependencies together when troubleshooting a multi-container setup. I also confirmed that a backup is only useful if I can restore it.

## Tools

Docker Compose, Nextcloud, MariaDB, Linux, shell scripting.
