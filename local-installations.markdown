---
layout: page
title: Local Installations
categories: documentation
---

Driven by both cost factors and data sovereignty requirements, Seed is design towards enabling locally hosted applications.

We have invested in locally hosted infrastructure that offers similar capabilities as cloud based environments. It enables auto-scaling of processes, internal service discovery, automatic load balancing and routing of requests and scaling the infrastructure horizontally as and when needed.

> Read more about the [Seed stack][seed-stack].

We are developing a user-facing application for this called Mission Control. Mission Control allows local teams responsible for the cluster and the managed applications to monitor and operate every aspect.

> Read more about [Mission Control][mc2].

This infrastructure is built using Apache Mesos, a tool that manages application processes in a cluster. Mesos is the tool that has enabled Twitter and Netflix to reliably scale their infrastructure on demand. Mesos allows us to extend the principles of cloud hosting to a locally hosted context while complying with local data sovereignty laws.

Our current South Africa based cluster powers over 400 mobi sites and is the deploy target for our expansions as part of the Facebook Incubator partnership. It is the bedrock infrastructure for all our mobile health based initiatives in various countries across Africa.

> Visit the [Apache Mesos Project][mesos] website.

#### Physical host server specifications

| CPU     | 2 x Intel Xeon E5-2620 2.4GHz |
| Storage | 3 x 1tb drives in RAID5 with dual hot-swap power supplies |
| Memory  | 64 gigabytes |

From these large physical servers we provision virtual machines.
While completely configurable, a standard virtual machine is defined as:

| Memory | 8 GB RAM
| Disk   | 200 GB
| Cores  | 4
| Backups | automated nightly
| Configuration management | automated using Puppet
| Continuous deployments | Puppet and Sideloader

> Read more about our [deployment tools][deploys].

The cores are timeshared between virtual machines, memory is completely dedicated as our applications are more likely to memory bound, not CPU bound.

While it is technically possible to run a Mesos cluster on a single machine our recommendation would be to only consider this if the application starts to grow beyond the capacity of 2 large servers.

[seed-stack]: ./seed-stack.html
[mesos]: http://mesos.apache.org/
[mc2]: ./mission-control.html
[deploys]: ./deploy-tools.html
