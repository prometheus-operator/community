# Project Ideas

If you are a Prometheus-Operator team member and consider mentoring during the GSoC 2026 cycle, please, submit your ideas below using the [template](#template) in the [Ideas](#ideas) section.

If you are a GSoC candidate, please review our [contributor guidance](../contributor_guidelines.md), familiarize yourself with the [Ideas](#ideas) below, and read the [AI Use Policy](#ai-use-policy) before submitting your proposal.

[Google Summer of Code timeline](https://developers.google.com/open-source/gsoc/timeline).

> [!NOTE]
> Please note that GSoC is a program known for its strict deadlines. In addition to responding to your mentee on time, you will be required to submit evaluations on time. Failures to meet the deadlines might affect Prometheus-Operator's future participation in GSoC.

> [!NOTE]
> You'll notice all topics have the same mentors. To ensure each project receives dedicated attention, not all ideas listed here may be selected. Final selection will depend on the quality of proposals received for each project.

---

## AI Use Policy

We allow the use of AI tools when contributing to the project. Please review our [AI use policy](https://github.com/prometheus-operator/prometheus-operator/blob/main/CONTRIBUTING.md#ai-use-policy) before submitting your application.

> [!WARNING]
> **Avoid submitting low-effort, AI-generated proposals.** AI can be helpful, especially for non-native English speakers, but we strongly discourage low-quality or clearly AI-generated "slop." Such proposals will be rejected.

---

## Template

```markdown
### Project Title

- Description:
- Expected Outcome:
- Recommended Skills:
- Expected project size: # one of small (~90 hour projects), medium (~175 hour projects) and large (~350 hour projects)
- Mentor(s): #For GSoC, it is **required** to have at least 2 mentors with 1 being a primary mentor.
  - Jane Doe (@jane-github, jane@email.address) - primary
  - John Doe (@john-github, john@email.address)
- Upstream Issue (URL):
```

## Ideas

### Documentation and Examples Gap Analysis

- Description: The Prometheus-Operator project has grown significantly over the years, and there are gaps in documentation and practical examples that make it challenging sometimes for users to adopt and configure the operator effectively.

  Identify gaps in prometheus-operator or/and kube-prometheus documentation, then create comprehensive, tested content. This includes use case examples, troubleshooting guides, and example configurations for different deployment scenarios.

- Expected Outcome:
  - Audit of existing documentation to identify gaps and outdated content.
  - New documentation covering missing topics with tested and verified examples.
  - Updated examples and getting-started guides reflecting current best practices.

- Recommended Skills: Technical writing, Kubernetes, Prometheus, Alertmanager, Go (for understanding code examples)

- Expected project size: small

- Mentor(s):
  - Jayapriya Pai (@slashpai, <slashpai9@gmail.com>)
  - Simon Pasquier (@simonpasquier, <pasquier.simon@gmail.com>)
  - Hélia Barroso (@heliapb, <helia_barroso@hotmail.com>)

- Upstream Issue (URL): NA

---

### Silence CRD for Alertmanager

- Description: Implement a new CRD that allows users to declaratively manage  Alertmanager silences as Kubernetes resources, enabling standard tooling (kubectl, GitOps) instead of direct API interaction.

- Expected Outcome:
  - New Silence CRD with spec fields for matchers, time windows, and metadata.
  - Controller logic to reconcile Silence resources with Alertmanager.
  - Documentation, examples, and end-to-end tests.

- Recommended Skills: Go, Kubernetes, Alertmanager API

- Expected project size: medium

- Mentor(s):
  - Simon Pasquier (@simonpasquier, <pasquier.simon@gmail.com>)
  - Jayapriya Pai (@slashpai, <slashpai9@gmail.com>)
  - Hélia Barroso (@heliapb, <helia_barroso@hotmail.com>)

- Upstream Issue (URL): <https://github.com/prometheus-operator/prometheus-operator/issues/2398>

- Related PR: <https://github.com/prometheus-operator/prometheus-operator/pull/7798>

---

### Zone-Aware Sharding for Prometheus

- Description: Implement zone-aware sharding per the accepted proposal in the prometheus-operator repo to reduce inter-zone network traffic by binding each Prometheus shard to a specific zone.

- Expected Outcome:
  - Implementation of `shardingStrategy.mode: Topology` behind a feature gate.
  - Node selector and relabel configuration generation for zone-based sharding.
  - Validation logic and documentation with examples.

- Recommended Skills: Go, Kubernetes, Prometheus configuration, understanding of cloud provider zones/regions

- Expected project size: small

- Mentor(s):
  - Simon Pasquier (@simonpasquier, <pasquier.simon@gmail.com>)
  - Jayapriya Pai (@slashpai, <slashpai9@gmail.com>)
  - Hélia Barroso (@heliapb, <helia_barroso@hotmail.com>)

- Upstream Issue (URL): <https://github.com/prometheus-operator/prometheus-operator/issues/6437>

---

### Perses Integration for kube-prometheus

- Description: [Perses](https://github.com/perses/perses) is a CNCF project that provides an open-source alternative to Grafana for visualizing Prometheus metrics, using the Apache 2.0 license. The kube-prometheus project currently bundles Grafana for dashboarding, but some users prefer or require using Perses instead. This project adds the option to deploy Perses in kube-prometheus, implementing the necessary Jsonnet libraries and leveraging Perses community dashboards.

- Expected Outcome:
  - Jsonnet libraries for deploying Perses in kube-prometheus.
  - Configuration options to choose between Grafana, Perses, or both.
  - Tested dashboards using Perses community dashboards for Kubernetes monitoring.
  - Migration guide from Grafana to Perses dashboards.

- Recommended Skills: Jsonnet, Kubernetes, Perses, Prometheus, Grafana (for understanding existing dashboards)

- Expected project size: medium

- Mentor(s):
  - Jayapriya Pai (@slashpai, <slashpai9@gmail.com>)
  - Hélia Barroso (@heliapb, <helia_barroso@hotmail.com>)
  - Simon Pasquier (@simonpasquier, <pasquier.simon@gmail.com>)

- Upstream Issue (URL): <https://github.com/prometheus-operator/kube-prometheus/issues/2654>
