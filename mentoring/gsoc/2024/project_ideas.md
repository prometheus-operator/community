## Project Ideas

If you are a Prometheus-Operator team member and consider mentoring during the GSoC 2024 cycle, please, submit your ideas below using the template.

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

### Extending ScrapeConfig surface

- Description: The ScrapeConfig is a recently added Custom Resource Definition (CRD) of Prometheus-Operator. Unlike other monitoring-related CRDs like ServiceMonitor and PodMonitor, ScrapeConfig offers a more generic approach by aiming to be a 1:1 equivalent of the Prometheus scrape configuration. The current state of ScrapeConfig is far from being feature-complete compared to what Prometheus configuration offers. For us to be able to promote the ScrapeConfig CRD from alpha to beta/stable, we need to implement more service discoveries as well as missing configuration options.
- Recommended Skills: Go, Prometheus
- Expected project size: small
- Mentors:
  - Jayapriya Pai (@slashpai, slashpai9@gmail.com)
  - Simon Pasquier (@simonpasquier, pasquier.simon@gmail.com)
  
### Website/Documentation revamp

- Description: We maintain all of our documentation on our website https://prometheus-operator.dev/ . The website was created a couple of years ago and not much has changed ever since, from project documentation exposed by the website or even the framework used to build it. This project is about different workstreams related to our website and documentation:
  - Update frameworks, such as doks and hugo, and propose automation to keep them up to date.
  - Review the documentation available in our [main git repository](https://github.com/prometheus-operator/prometheus-operator/tree/main/Documentation) that is not available on the website, and incorporate it into the website.
  - Review and propose a more coherent content organization.
  - Propose changes to our development process to help us keep documentation up to date.
- Recommended Skills: Technical writing, Prometheus, Alertmanager
- Expected project size: medium
- Mentor(s):
  - Arthur Silva Sens (@ArthurSens, arthursens2005@gmail.com)
  - Nicolas Takashi (@nicolastakashi, nicolas.tcs@hotmail.com)

### `*Monitor` status subresource

- Description: Currently, there are 4 CRDs fully dedicated to configuring Prometheus scrape targets, `PodMonitor`, `ServiceMonitor`, `Probes` and `ScrapeConfig`, and all of them are missing the `.Status` subresource. This project is about implementing the status subresource for all 4 CRDs to increase the visibility and debuggability of the scrape configuration. The fields added to the status subresource will be discussed deeply during the mentorship. Still, a few ideas that already came up are showing a list of Prometheus CRs that selected each Monitor CR and how many targets the resource identifies.
- Recommended Skills: Go, Kubernetes.
- Expected project size: large
- Mentor(s): 
  - Arthur Silva Sens (@ArthurSens, arthursens2005@gmail.com)
  - Simon Pasquier (@simonpasquier, pasquier.simon@gmail.com)
- Upstream Issue (URL): https://github.com/prometheus-operator/prometheus-operator/issues/3335

### Prometheus Agent - Daemoset deployment model

- Description: The `PrometheusAgent` Custom Resource Definition (CRD) was recently implemented as an Alpha CRD. Before graduating the CRD to Beta/Stable, we want to implement additional deployment models. One of the deployment models that we look forward to implement is the Daemonset approach, where a small agent is deployed in every node of a Kubernetes cluster. This project will touch on several parts of software engineering, such as requirements research, writing up design documents, building consensus in the community and implementing the approved proposal.
- Recommended Skills: Go, Kubernetes, [Operator Design Pattern](https://github.com/cncf/tag-app-delivery/blob/main/operator-whitepaper/v1/Operator-WhitePaper_v1-0.md#foundation)
- Expected project size: large
- Mentor(s):
  - Arthur Silva Sens (@ArthurSens, arthursens2005@gmail.com)
  - Simon Pasquier (@simonpasquier, pasquier.simon@gmail.com)
  - Kemal Akkoyun (@kakkoyun, kakkoyun@gmail.com)
- Upstream Issue (URL): https://github.com/prometheus-operator/prometheus-operator/issues/5495
