---
layout: page
title: Deployment Tools
categories: documentation
---

Seven years of designing, deploying and maintaining population scale mobile sites globally has dramatically shaped our thinking around what kind of processes, infrastructure and tools lead to highly reliable web applications.

Over the last three years we have developed and maintained an continuous integration and deployment system called Sideloader. This open source tool allows for complete end-to-end automation of development, testing and deploying of our applications.

> Visit the [Sideloader Github repository][sideloader].

Any change made to any of our software proejcts is automatically tested and checked for code coverage. If all audits pass, the software is versioned, prepared as a Debian package, and immediately deployed to a QA server without any manual intervention. This ensures that our deploys remain relatively small, predictable, and repeatable.

As changes have successfully been applied on the QA server, we typically have good guarantees that the changes can be applied to the production environment as well. Like QA deploys, production builds are completely automated and repeatable.

We have a graphical web based UI called [Xenzen][xenzen] that helps us provision virtual machines from the large bare metal servers.

#### Typical Virtual Machine Stack

| Server | Ubuntu Server (current LTS release)
| Load Balancer | Haproxy
| Proxy & SSL Termination | Nginx
| App Server | uWsgi
| Single Machine Process Manager | Supervisord
| Cluster Process Manager | Apache Mesos
| Databases | Postgresql & Redis
| Message Broker | RabbitMQ

> Visit the [Xenzen Github repository][xenzen]

[sideloader]: https://github.com/praekelt/sideloader
[xenzen]: https://github.com/calston/xenzen
