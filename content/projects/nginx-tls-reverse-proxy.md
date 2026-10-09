+++
title = "Nginx Reverse Proxy and TLS"
weight = 7
projectType = "Lab"
summary = "Put a sample web service behind Nginx, enable HTTPS in a VM, and limit direct access to the backend."
challenge = "Exposing the application server directly can leave extra ports open and make routing and HTTPS behavior harder to manage."
approach = "Run Nginx in front of a local service, set the proxy routes and headers, and restrict the backend to the lab proxy."
tags = ["Nginx", "Linux", "Networking", "TLS", "Web Services"]
+++

## Scenario

I’d use this lab to give a small sample application one clear entry point instead of exposing its application server directly.

## Challenge

Wrong proxy headers, an open backend port, or a certificate mistake can make the service unreliable or expose more than intended.

## Approach

I’d configure an Nginx virtual host, proxy only the required route, and set the forwarding headers. The test certificate and private keys would stay local and out of version control.

## Verification

I’d check the Nginx configuration before reloading, test HTTP and HTTPS, confirm the backend can’t be reached directly from outside the VM, and review the logs for failed requests.
