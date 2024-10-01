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

{{% import path="shared-slides/introduction.md" %}}

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

{{% import path="shared-slides/design/event_storming.md" %}}

---

{{% import path="shared-slides/design/bounded_context.md" %}}

---

{{% import path="shared-slides/design/context_map.md" %}}

---

{{% import path="shared-slides/architecture/architecture.md" %}}

---

{{% import path="shared-slides/architecture/microservices.md" %}}

---

{{% import path="shared-slides/architecture/clean_architecture.md" %}}

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

{{% import path="shared-slides/deployment/deployment.md" %}}

---

{{% import path="shared-slides/deployment/kubernetes.md" %}}

---

{{% import path="shared-slides/deployment/cluster_overview.md" %}}

---

## Monitoring

To monitor the system:

-   **Prometheus**: for metrics collection and alerting
-   **Grafana**: for metrics visualization

[Documentation](https://revue-org.github.io/revue/docs/report/deployment/kubernetes)

---

### Dashboard

![Monitoring](https://raw.githubusercontent.com/revue-org/revue/main/docs/website/docs/report/img/monitoring/grafana-monitoring.png)
