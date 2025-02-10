## Project Ideas

If you are a Prometheus-Operator team member and consider mentoring during the GSoC 2025 cycle, please, submit your ideas below using the template.

If you are a GSoC candidate, please check out our [contributor guidance](../contributor_guidelines.md).

[Google summer of code timeline](https://developers.google.com/open-source/gsoc/timeline).

> **NOTE:** Please note that GSoC is a program known for its strict deadlines. In addition to responding to your mentee on time, you will be required to submit evaluations on time. Failures to meet the deadlines might affect Prometheus-Operator's future participation in GSoC.

---

### Template

```
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

---

## Ideas

### Status for configuration objects

- Description: A frequent pain point for users is to understand whether their configuration resources are applied and if it's not the case, what's the issue. We improved a bit the situation by emitting events when the reconciliation loop rejects configuration resources but it would be even better if the information was persisted in the status subresource (for instance comparing the resource's generation against the observed generation can indicate if the latest version is reconciled or not).

While workload resources like Prometheus and Alertmanager have gained a Status subresource, there's no such thing (yet) for configuration resources like ServiceMonitor, PodMonitor, AlertmanagerConfig, Probe, ScrapeConfig and PrometheusRule. The main difference between workload and configuration resources is that configuration resources can be selected by multiple workloads: for example, 2 different Prometheus resources can select the same ServiceMonitor resource. As a consequence, we can't use the same API already defined for workload resources. Please note that we don't want to forbid this situation since it is a perfectly valid and supported use case (for instance running 2 stacks in parallel during migrations).

- Recommended Skills: Go, Kubernetes
- Expected project size: large
- Mentors:
  - Jayapriya Pai (@slashpai, slashpai9@gmail.com)
  - Simon Pasquier (@simonpasquier, pasquier.simon@gmail.com)
  - M Vishwanath Sai (@mviswanathsai, mviswanath.sai.met21@itbhu.ac.in)
- Upstream Issue (URL): https://github.com/prometheus-operator/prometheus-operator/issues/3335
