---
layout: page
title: Seed Maternal Health
categories: documentation
---

Seed Maternal Health is the MomConnect programme deployed on our Seed Stack.
It consists of various components working together to deliver the health intervention.

## Application logic

The application logic is implemented in the following tailor made
Javascript Sandbox applications:

* USSD based registrations
* FAQs
* Service Ratings
* Interactive SMS & USSD based dialogues
* 3rd party health system integrations

> Visit the [applications' GitHub repository][momconnect-js]

## Mobi site

The Mobi site exposes the registration and stage based content components of
our maternal health programme for low-end smart and feature phones.

It is built using Molo, our set of tools for publishing mobi sites with a
community focus. It is built on top of Django and uses Wagtail for an
exceptional content experience.

> Read more about [Molo][molo], the technology behind our mobi sites.

## API and Integrations

Never does one solutions do everything and Seed Maternal Health is no exception.
We integrate with DHIS2, IHRIS through the OpenHIE interoperability layer.

> Visit the [GitHub repository][momconnect-py] with the API integrations.

## Billing

We aim for the Seed Maternal Health's services to be offered at zero cost to
the end user. This often happens through reverse billing. We provide billing
infrastructure and audit logs to allow network operator costs to be reconcilled
with our records.

## Dashboards

We provide operational dashboards for all our applications. This enables the
teams responsible to have an immediate view of what is going on and how the
system is performing. Long term dashboards that help determine the ongoing
strategy of the projects are housed within DHIS2.

---

The following components which are part of Seed Maternal Health are provided by the
[Seed Messaging][seed-messaging] infrastructure:

* [Junebug][junebug]
* [Open Helpdesk][open-helpdesk]
* [Scheduler][scheduler]
* [Identity Store][identity-store]

> Read more about the [Seed Messaging][seed-messaging] components that power these applications.

[seed-messaging]: ./seed-messaging.html
[molo]: https://molo.readthedocs.org
[momconnect-js]: https://github.com/praekelt/go-ndoh
[momconnect-py]: https://github.com/praekelt/ndoh-control
[junebug]: ./seed-messaging.html#junebug
[open-helpdesk]: ./seed-messaging.html#open-helpdesk
[scheduler]: ./seed-messaging.html#stage-based--scheduled-messaging
[identity-store]: ./seed-messaging.html#identity-service
