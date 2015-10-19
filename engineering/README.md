# Engineering

The first Seed instance is Seed: Maternal Health. These are the components we
are building for it:

| Component                           | Lead     | Team | Status      |
| ----------------------------------- | -------- | -----| ----------- |
| [Mission Control](#mission-control) | Milton   | ?    | In progress |
| [Scheduler](#scheduler)             | Colin    | SRE  | -           |
| [Junebug](#junebug)                 | Simon C  | Vumi | In progress |
| [Identity Store](#identity-store)   | Simon dH | ?    | -           |
| [Billing](#billing)                 | Simon C  | Vumi | -           |
| [Helpdesk](#helpdesk)               | Milton   | WCL  | -           |
| [Operational Dashboards](#operational-dashboards) | Colin | SRE | - |
| [Jsbox Runner](#jsbox-runner)       | Simon C  | Vumi | -           |

## Mission Control

* **Lead**: Milton
* **Team**: ?

Mission Control currently has a strong Unicore / Molo focus. That needs to be
broadened to allow other applications to run and expose the needed operational
information for those applications. Mission Control already has notion of
organization level access controls.

A lot of UX, design & FED input is needed here to in order to maintain
conceptual integrity between all of the components.

##Stage-based Messaging Engine

* **Lead**: Colin
* **Team**: SRE

We have an implementation for MAMA Nigeria but it is likely we will need to go
back to the drawing board for part of it. It works but we have doubts about its
ability to scale to the size we need it to be.

##Junebug

* **Lead**: Simon Cross
* **Team**: Vumi

Of all the components this is furthest along and most promising. What needs to
be done here is that it needs to be able to accept Vumi messages via RabbitMQ
(alongside the already existing HTTP API). The rough back of the napkin estimate
for this is roughly a sprint and is needed for FamilyConnect Uganda.

##Identity Store

* **Lead**: Simon de Haan
* **Team**: ?

There is an implementation in Django for MAMA Nigeria. It needs to be extracted
from that control interface into an independent thing. The new requirement here
is that changes to fields on a contact should trigger events that other
applications can register for (new registration, baby born, unsubscribe,
opt-in / opt-out).

##Billing

* **Lead**: Simon Cross
* **Team**: Vumi

The implementation in Vumi is fairly standalone but will still need some
attention, mostly around how accounts are managed. We also need to clearly
define the purpose of billing within Seed and what non-message billing items
might be needed by other Seed components.

##Helpdesk

* **Lead**: Milton
* **Team**: Western Cape Labs

Currently Western Cape Labs is earmarked for this development and will likely
only be delivered by January / February. Since this is a Django application
Milton will need to understand how it works in order to be able to host &
integrate it with Mission Control.

##Operational Dashboards

* **Lead**: Colin
* **Team**: SRE

This is the infrastructure behind Riemann. We need robust infrastructure so the
various components can query for their relevant metrics in order to provide the
needed operational visibility.

##Jsbox Runner

* **Lead**: Simon Cross
* **Team**: Vumi

This already exists but can do with some optimizations since we no longer will
need to reload every application per request. We also need to integrate it
with Junebug.
