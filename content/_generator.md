+++

title = "Revue"
description = "A real-time video surveillance and environment monitoring system"
outputs = ["Reveal"]
aliases = [
    "/guide/"
]

+++

# Revue

## A real-time video surveillance and environment monitoring system

---

# Introduction

**Revue** is a distributed real-time system for video surveillance. It allows the user to:

1. Check an environment remotely through cameras

2. Monitor an environment using sensors

3. Add security rules based on his needs triggering alarms
    1. Intrusions in case of violated safety rule by cameras
    2. Outliers in case of violated safety rule by sensors

Due to his level of configurability, Revue can be used in multiple scenarios.

---

# Analysis

---

## Requirements

Detailed requirements can be found in the [documentation](https://revue-org.github.io/revue/docs/report/analysis/business-requirements).

---

## Quality Attributes

System's main properties:

-   _Scalability_

-   _Availability_

-   _Reliability_

-   _Observability_

-   _Modularity_

-   _Energy Efficiency_

[Documentation](https://revue-org.github.io/revue/docs/report/analysis/quality-attributes)

---

# Design

---

## Event Storming

In order to create a better understanding of the domain, we used the Event Storming technique. We performed the following steps:

1. **Unstructured exploration**: the goal is to identify the main events
2. **Timeline**: the events are ordered in time
3. **Pivotal events & pain points**: discussion about critical point that require attention and reasoning on events that have impact on the domain.
4. **Actors, Commands, Policies and Read Models**
5. **Aggregates**: groping of event into aggregates
6. **Bounded contexts**: identification of bounded contexts based on aggregates interaction

[Documentation](https://revue-org.github.io/revue/docs/report/design/event-storming)

---

## Bounded Contexts

After the event storming session, the following contexts have been identified:

-   **Auth**: Responsible for managing the authentication and authorization of the users. It also is responsible for managing the permissions of the users.
-   **User**: This context is responsible for managing the users of the system, in particular, nothing regarding the authentication process but only the management of the user registry.
-   **Monitoring**: It is responsible for managing the devices and the data they produce. This context is responsible for consulting the data produced by the devices, their configurations and everything regarding the WoT interactions.
-   **Alarm**: Responsible for managing the alarms in the overall system. It is also responsible for the object recognition feature of the system.
-   **Notification**: Responsible for managing the notifications of the system. It is responsible for sending notifications to the users when particular events occur.
-   **Location**: Responsible for the location management of the system.

---

## Context Map

![Context Map](https://raw.githubusercontent.com/revue-org/revue/main/docs/website/docs/report/img/ContextMap.png)

---

# Architecture

We chose to use a microservices architecture for the system. This architecture consists on designing software applications as suites of independently deployable services. Each service runs in its own process and communicates with other services through a well-defined interface.

-   [Components & connectors view](https://revue-org.github.io/revue/docs/report/design/architecture/documentation#components--connectors)
-   [Module view](https://revue-org.github.io/revue/docs/report/design/architecture/documentation#module-view)
-   [Deployment view](https://revue-org.github.io/revue/docs/report/design/architecture/documentation#deployment-view)

---

## Microservices

Using the _Bounded Contexts Decomposition Strategy_, we identified the following microservices:

-   **Auth Service**: Responsible for managing the authentication and authorization of the users.
-   **User Service**: Responsible for managing the users of the system.
-   **Device Service**: Responsible for managing the devices connected to the system.
-   **Monitoring Service**: Responsible for managing the data produced by the devices.
-   **Alarm Service**: Responsible for managing security rules and anomalies detections.
-   **Recognition Service**: Responsible for performing object recognition on cameras video streams.
-   **Notification Service**: Responsible for managing the notifications of the system.
-   **Location Service**: Responsible for the location management of the system.
-   **Log Service**: Responsible for storing events that occur in the system.

---

## Clean Architecture

The design of all relevant microservices follows the Clean Architecture pattern. This helped us in maintaining a core domain design that abstracts away from all technical issues. As showed in the picture above, we made use of the following layers:

-   **Domain**: DDD entities, value objects, factories, ...
-   **Application**: DDD services, repositories, ...
-   **Presentation**: Machinery to translate external data representation to domain entities and vice versa.
-   **Infrastructure**: Mostly external service implementation, DB interfaces, REST APIs, Events managers, ...

[Documentation](https://revue-org.github.io/revue/docs/report/design/architecture/microservices#clean-architecture)

---

## Microservices patterns

We reasoned about:

-   **Communication patterns**
    -   Remote Procedure Invocation
    -   Asynchronous Messaging
-   **External API patterns**
    -   API Gateway (reverse proxy)
-   **Deployment patterns**
    -   Service as container
    -   Database per service
    -   Externalized configuration
-   **Security patterns**
    -   Token-based security

[Documentation](https://revue-org.github.io/revue/docs/report/design/architecture/patterns)

---

# Deployment

Two way to deploy the system:

1. **Docker Compose**: for local development and testing
2. **Kubernetes**: for production

[Documentation](https://revue-org.github.io/revue/docs/category/deployment)

---

## Kubernetes

-   Configuration files for Kubernetes and `deploy` script are available in the repository [revue-kubernetes](https://github.com/revue-org/revue-kubernetes/)
-   It is provided an example of how to deploy the system on a Raspberry Pi cluster, using the _k3s_ distribution.

---

### Cluster Overview

![Kubernetes deployment](https://raw.githubusercontent.com/revue-org/revue/main/docs/website/docs/report/img/kubernetes-deployment.png)

---

## Monitoring

To monitor the system:

-   **Prometheus**: for metrics collection and alerting
-   **Grafana**: for metrics visualization

[Documentation](https://revue-org.github.io/revue/docs/report/deployment/kubernetes)

---

![Monitoring](https://raw.githubusercontent.com/revue-org/revue/main/docs/website/docs/report/img/monitoring/grafana-monitoring.png)
