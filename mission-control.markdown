---
layout: page
title: Mission Control
categories: documentation
---

Mission Control provides a graphical user interface for teams responsible for operating Seed infrastructure.

Mission Control manages application life cycles and provides access to infrastructure and application level reporting data.

By design, Seed infrastructure is separated over multiple heterogeneous applications and interfaces yet need to be presented in a unified and consistent experience. Mission Control provides this experience.

> Visit the [Mission Control GitHub repository][mc2].

Mission Control manages the deployment and build process of applications on our production clusters by automatically packaging code repositories into Linux Containers.

For running applications it provides metrics and monitoring tools as well as
live access to application logs.

> Read more about containers at [docker.com][container].

[container]: https://www.docker.com/what-docker
[mc2]: https://github.com/praekelt/mc2

Praekelt Foundation is not the target audience of Mission Control.
It is designed to enable handover to local teams as fast as possible.
