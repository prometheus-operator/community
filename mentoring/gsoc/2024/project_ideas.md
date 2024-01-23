## Project Ideas

If you are a Prometheus-Operator team member and consider mentoring during the GSoC 2024 cycle, please, submit your ideas below using the template.

[Google summer of code timeline](https://developers.google.com/open-source/gsoc/timeline).

> **NOTE:** Please note that GSoC is a program known for its strict deadlines. In addition to responding to your mentee on time, you will be required to submit evaluations on time. Failures to meet the deadlines might affect CNCF's future participation in GSoC.

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

- Description: The ScrapeConfig is a recently added Custom Resource Definition (CRD) of Prometheus-Operator. Differently from other monitoring related CRDs like ServiceMonitor and PodMonitor, ScrapeConfig offers a more generic approach by aiming to be a 1:1 equivalent of the Prometheus scrape configuration. The current state of ScrapeConfig is far from being feature-complete compared to what Prometheus configuration offers. For us to be able to promote the ScrapeConfig CRD from alpha to beta/stable, we need to implement more service discoveries as well as missing configuration options.
- Recommended Skills: Go, Prometheus
- Expected project size: small
- Mentors:
  - Jayapriya Pai (@slashpai, slashpai9@gmail.com)
  - Simon Pasquier (@simonpasquier, pasquier.simon@gmail.com)
  
### Webiste/Documentation revamp

- Description: We maintain all of our documentation on our website https://prometheus-operator.dev/ . The website was created a couple of years ago and not much has changed ever since, from project documentation exposed by the website or even the framework used to build it. This project is about different workstreams related to our website and documentation:
  - Update framework, such as doks and hugo, and propose automation to keep it up to date.
  - Review the documentation available in our [main git repository](https://github.com/prometheus-operator/prometheus-operator/tree/main/Documentation) that is not available in the website, and incorporate it to the website.
  - Review and propose a more coherent content organization.
  - Propose changes to our development process to help us keep documentation up to date.
- Recommended Skills: Technical writing, Prometheus, Alertmanager
- Expected project size: medium
- Mentor(s):
  - Arthur Silva Sens (@ArthurSens, arthursens2005@gmail.com)
  - Nicolas Takashi (@nicolastakashi, nicolas.tcs@hotmail.com)

### `*Monitor` status subresource

- Description: Currently, there are 4 CRDs fully dedicated to configure Prometheus scrape targets, `PodMonitor`, `ServiceMonitor`, `Probes` and `ScrapeConfig`, and all of them are missing the `.Status` subresource. This project is about implementing the status subresource for all 4 CRDs to increase visibility and debuggability of scrape configuration. The fields added to the status subresource will be discused deeply during the mentorship, but a few ideas that already came up is showing list of Prometheus CRs that selected each Monitor CR and how many targets the resource identifies.
- Recommended Skills: Go, Kubernetes.
- Expected project size: large
- Mentor(s): 
  - Arthur Silva Sens (@ArthurSens, arthursens2005@gmail.com)
  - Simon Pasquier (@simonpasquier, pasquier.simon@gmail.com)
- Upstream Issue (URL): https://github.com/prometheus-operator/prometheus-operator/issues/3335
