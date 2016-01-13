---
layout: page
title: The Seed Stack
categories: documentation
---

Software developers looking to replicate our production environment for local development can do so by running our [Vagrant][vagrant] based seed-stack:

    $ git clone git://github.com/praekelt/seed-stack.git
    $ cd seed-stack
    $ vagrant up

[consular]: https://consular.readthedocs.org/en/latest/
[mc2]: ./mission-control.html
[vagrant]: https://www.vagrantup.com/

Our Seed stack consists of a number of open source components

#### Maintained by Praekelt Foundation

* [Consular][consular]
* [Mission Control][mc2]

#### Existing Open Source projects

* [Zookeeper](https://zookeeper.apache.org)
* [Mesos Controller & Worker](https://mesos.apache.org)
* [Marathon](https://mesosphere.github.io/marathon/)
* [Docker](https://www.docker.com/)
* [Docker Registry](https://docs.docker.com/registry/)
* [Consul](https://consul.io/)
* [Consul Template](https://github.com/hashicorp/consul-template)
* [Nginx](http://nginx.org/)
