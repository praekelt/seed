---
layout: page
title: Seed Messaging
categories: documentation
---

# Independently hostable text messaging tools for engaging with populations.

Praekelt Foundation has five years of experience building and operating population-scale text messaging services on our Vumi Go platform across Africa. We are taking this experience and re-organizing and expanding our existing code base to provide services that can be deployed where needed and scaled with the needs of the a variety of use cases such as national scale health, banking and civic engagement platforms.

System components can be deployed independently without access to cloud services, making it especially suitable for highly secure or sensitive applications.

Seed’s messaging system contains the following components that work together to provide a complete system for deploying, running, monitoring and analysing complex text messaging applications:

## Junebug

A beautiful API for creating, managing, using and monitoring messaging channels that hides the variations and complexities of aggregator, network operator and instant messaging services.

> Read more about [Junebug][junebug]

## Numi

An interface that allows service designers, content editors and developers to collaborate on building and operating rich messaging applications.

## Sandbox application runner

An API for deploying, managing and monitoring Javascript sandbox applications.

> Read more about [Javascript Sandbox applications][jsbox-apps].

## Identity service

A privacy-aware service for storing personal information provided by people interacting via messaging applications. It facilitates compliance with privacy regulations and standards by providing secure storage and management of personalized information.

## Billing statements and reports

A service for tracking message costs on a per-channel and per-network-operator basis and generating statements to allow reconciling invoices from network operators with observed usage and reports for monitoring operating costs of applications.

## Portia

A cellphone number portability and opt out tracking service used by Junebug to support direct connections to network operators and comply with local number portability and opt out laws.

> Read more about [Portia][portia].

## Open Helpdesk

A service for managing queries and issues reports submitted via text messages and a web interface allowing responders to reply to them. Includes support for selecting approved responses (FAQs) and escalating issues to managers.

## Stage-based & scheduled messaging

A service for sending a sequences of messages to subscribers. For example, financial advice messages for new account holders, or maternal health messages for pregnant mothers.

## Survey results explorer

Many text messaging applications capture registration records or results of surveys. This interface works alongside the identity service to allow exploring and analysing these results.

> Visit the [Survey results explorer GitHub Repository][survey-results-explorer]

## Nightingale

Facility or location-based incident reporting tool. Examples of facilities include bank branches and health clinics. It includes a user interface for creating and maintaining lists of facilities and a Javascript sandbox application for searching the list of facilities and submitting incident reports against a given facility.

> Visit the [Nightingale GitHub Repository][nightingale]

## System analysis

Seed components provide rich data streams describing their operational state. More than simple single-number metrics, these streams allow fine-grained system analysis and machine learning detection of nominal and error system states. The system analysis service allows aggregating and transforming data streams and directing results to analysis engines and data stores.

## Mission Control

A high-level interface that ties all of the components above together into an integrated platform. It allows launching and managing components and monitoring the parts of each service that are meaningful to the people building and operating Seed systems.

> Read more about [Mission Control][mc2]

[mc2]: ./mission-control.html
[nightingale]: https://github.com/praekelt/nightingale
[survey-results-explorer]: https://github.com/praekelt/gem-survey-tool
[portia]: https://portiadb.readthedocs.org
[jsbox-apps]: http://vumi-jssandbox-toolkit.readthedocs.org/
[junebug]: http://junebug.readthedocs.org/
