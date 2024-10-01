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

<!-- write-here "shared-slides/introduction.md" -->
<!-- end-write -->

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

<!-- write-here "shared-slides/design/event_storming.md" -->
<!-- end-write -->

---

<!-- write-here "shared-slides/design/bounded_context.md" -->
<!-- end-write -->

---

<!-- write-here "shared-slides/design/context_map.md" -->
<!-- end-write -->

---

<!-- write-here "shared-slides/architecture/architecture.md" -->
<!-- end-write -->

---

<!-- write-here "shared-slides/architecture/microservices.md" -->
<!-- end-write -->

---

<!-- write-here "shared-slides/architecture/clean_architecture.md" -->
<!-- end-write -->

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

<!-- write-here "shared-slides/deployment/deployment.md" -->
<!-- end-write -->


---

<!-- write-here "shared-slides/deployment/kubernetes.md" -->
<!-- end-write -->

---

<!-- write-here "shared-slides/deployment/cluster_overview.md" -->
<!-- end-write -->

---

## Monitoring

To monitor the system:

-   **Prometheus**: for metrics collection and alerting
-   **Grafana**: for metrics visualization

[Documentation](https://revue-org.github.io/revue/docs/report/deployment/kubernetes)

---

### Dashboard

![Monitoring](https://raw.githubusercontent.com/revue-org/revue/main/docs/website/docs/report/img/monitoring/grafana-monitoring.png)
