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

# Dev Ops

---

## Version Control

### Commits
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) to standardize the commit messages.

### Versioning
[Semantic Versioning](https://semver.org/) to version the software.


---

## Build Automation

### Plugin

As an empowerment of the Node package manager, this [plugin](https://github.com/kelvindev15/npm-gradle-plugin) has been used for dependencies, devDependencies, and scripts.

### Dependency management

[Renovate](https://docs.renovatebot.com/) has been used to keep all dependencies automatically up to date

---

## Quality Assurance

- [Prettier](https://prettier.io/): a code formatter with support for many languages.
- [ESLint](https://eslint.org/): static code analysis tool for identifying problematic patterns.
- [Codefactor](https://www.codefactor.io/): review code style and security on every pull request.
- [SonarCloud](https://www.sonarsource.com/products/sonarcloud/): code quality and security service
- [Codacy](https://www.codacy.com/): automated code review tool

--- 

## Workflow


---

## License

The project is licensed under the [MIT License](https://mit-license.org/) because of its permissive nature.

---

<!-- write-here "shared-slides/deployment/deployment.md" -->
<!-- end-write -->

---

<!-- write-here "shared-slides/deployment/kubernetes.md" -->
<!-- end-write -->

---

<!-- write-here "shared-slides/deployment/cluster_overview.md" -->
<!-- end-write -->

