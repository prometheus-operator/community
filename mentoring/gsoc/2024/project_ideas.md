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
