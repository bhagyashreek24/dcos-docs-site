---
layout: layout.pug
navigationTitle: Spinnaker 0.2.0-1.4.2
title: Spinnaker 0.2.0-1.4.2
menuWeight: 50
excerpt: Overview of DC/OS Spinnaker 0.2.0-1.4.2
featureMaturity:
enterprise: false
---


Spinnaker is an open source multi-cloud Continuous Delivery and Deployment tool started by Netflix for fast and stable deployments.

Spinnaker’s flexible pipeline model allows for easy customization and enhancement in addition to facilitating smart pipeline management to serve a variety of cloud deployment needs.

As of today, Spinnaker can deploy to and manage clusters simultaneously across both Amazon Web Services (AWS), Kubernetes and Google Cloud Platform (GCP) with full feature compatibility for those cloud providers. Spinnaker can also deploy to Cloud Foundry, and support for full integration with Microsoft Azure is currently underway.

## Benefits

1. Immutable Infrastructure
2. Multi-Cloud Deployments
3. Management Flexibility


## DC/OS Spinnaker provides the following features:
1. Canary Deployments: For monitoring test deployments on a small percentage of servers before scaling the changes to the rest. When would I use it? When testing a new batch of code or deployments.
2. Spinnaker is a collection of sub-services that work together to form the Continuous Deployment platform. Each service follows the single-responsibility principle which allows for faster iteration on each individual component and a more


## Components/Services
Spinnaker framework is a collection of sub-services that work together to form the Continuous
Deployment platform. Each service follows the single-responsibility principle which allows for
faster iteration on each individual component and a more pluggable architecture for custom
components.

For Spinnaker [Architecture refer]:( https://www.spinnaker.io/reference/architecture/)
The Spinnaker components are:-
● Deck
● Gate
● Orca
● Clouddriver
● Front50
● Rosco
● Igor
● Echo
● Fiat
● Kayenta
