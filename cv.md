---
mainfont: "Latin Modern Mono Light"
geometry:
- margin=20mm
- heightrounded
block-headings: true
---

# Boris Khasanov

**Senior Data Platform Engineer / SRE**

[bouresk@outlook.com](mailto:bouresk@outlook.com) |
[+64 22 171 2798](tel:64221712798) | [borisAsCode.com](https://borisascode.com) |
Auckland, NZ | NZ citizen

Platform engineer with 14+ years building and running distributed systems
across cloud and on-prem, most recently in regulated banking. I move legacy,
hand-built platforms onto managed ones (Kafka to Confluent Cloud, Kong to AKS,
Akamai to Terraform) and leave behind automation, monitoring, runbooks and a
clear handover.

## Skills

| Category | Skills |
|----------------------:|--------------------------------------------------|
| Data platforms       | Confluent Kafka, Confluent Cloud, KRaft, Kafka Connect, Schema Registry, SQL Server |
| Cloud & containers   | Azure, AKS, AWS, Kubernetes, OpenShift, Helm, Docker |
| Infra as Code        | Terraform, Terraform Enterprise, Terragrunt, Ansible |
| CI/CD                | Azure DevOps, GitHub Actions, CloudBees/Jenkins, Octopus Deploy, ArgoCD |
| Observability        | Grafana, Prometheus, Thanos, Elastic, Splunk, Alertmanager, PagerDuty |
| Security             | Vault, CMK/BYOK, RBAC, Qualys, CIS hardening |
| Edge & API           | Akamai, EdgeWorkers, Kong Gateway, F5 |
| AI                   | GitHub Copilot agents, autonomous patching agents, Whisper |

## Experience

### ASB Bank

[asb.co.nz](https://www.asb.co.nz/) · Public API Squad · Auckland

#### Software Consultant - SRE (Contract) | August 2026 - Present

Platform modernisation, security automation and documentation for ASB's public
API platform.

- Lead the migration of legacy Kafka from physical hosts in two data centres to
  Confluent Cloud. Agreed a phased GitOps plan with the Kafka owners and the
  target platform team: topics, then producers and consumers, then the cluster.
- Lead the migration of the public-facing Kong Gateway from self-built
  containers on RHEL 7 hosts to the bank's managed Kong on AKS, with Ansible
  runbooks, GitOps, Elastic monitoring, rollback at each step and an audit
  trail.
- Replaced manual vulnerability patching across Ansible config, RHEL hosts,
  Qualys sidecars and code scan findings by getting the squad onboarded early
  to the bank's AKS-hosted AI agents that patch code automatically.
- Building Terraform modules (network lists, client lists, EdgeWorkers, rules)
  and a GitHub repository template for Akamai, which 3-4 squads currently
  manage by hand in the console. Agreed the approach with Security; piloting on
  Public API before presenting it to the fortnightly Akamai community.
- Lead ASB's response to Payments NZ CRL revocation checks for client
  certificates: EdgeWorkers enforcement at the edge, plus an interim scheduled
  GitHub Actions control that validates the CRL, matches revoked certificates
  to client records and disables affected clients.
- Rebuilt the team's documentation from two duplicated, unstructured wikis.
  Recorded handovers with departing senior engineers and turned them into wiki
  pages through a Whisper transcription pipeline, wrote the onboarding guide,
  and introduced blameless postmortems based on Google's template.

### Westpac New Zealand

[westpac.co.nz](https://westpac.co.nz/) · Event Streaming · Auckland

#### Senior Platform Engineer | May 2025 - July 2026

Led the modernisation and production reliability of a 12-broker Confluent Kafka
platform spanning two OpenShift data centres and Azure.

- Led the ZooKeeper-to-KRaft migration, redesigning the controller quorum
  across three failure domains using an Azure witness, completing the staged
  production cutover and retiring ZooKeeper deployment and monitoring.
- Delivered the Azure witness as durable infrastructure with stable networking,
  CMK-encrypted persistent metadata, idempotent rebuilds, controller-ID
  migration and dynamic Vault-backed credentials.
- Built operational visibility across Grafana, Thanos and Splunk with dual-DC
  Kafka, KRaft and broker-log dashboards, request-metrics alerts and DLQ
  monitoring. Used it to diagnose a production replication failure after KRaft
  patching, restore brokers and Kafka Connect workers, and turn the incident
  into PIRs and follow-up controls.
- Made high-risk platform changes repeatable through environment-locked
  migration automation with dry-run support, plus safe, selective rolling
  restarts for all 12 brokers.
- Introduced agentic AI delivery to the engineering chapter: wired 9+
  enterprise systems (Jira, Bitbucket, CloudBees, ServiceNow, Splunk, Azure)
  into GitHub Copilot through reusable skills, and built an agent loop that
  files the ticket, applies Terraform via CloudBees, verifies the result and
  raises PRs for review. Used it to stand up a stretched dual-DC Kafka cluster
  in a day.

#### Platform Engineer | June 2021 - May 2025

Built and operated Kafka migration and delivery capabilities across on-prem
OpenShift, AWS and Confluent Cloud.

- Migrated 20+ internal teams to new data centres over six months, building the
  deployment pipeline, topic-placement tooling, runbooks and cutover playbooks
  used from sandpit through production.
- Delivered the migration platform for selected workloads to Confluent Cloud,
  connecting AWS EKS over PrivateLink and adding cluster linking with
  consumer-offset sync, private Schema Registry, BYOK, RBAC and self-service
  onboarding.
- Built BrokerRolla to automate safe Kafka rolling restarts and supported the
  platform on call, leading incident response and blameless postmortems.

### Earlier career

- **Platform Engineer, Fraedom (now Visa) · 2019-2021.** Built Octopus Deploy
  pipelines, including an offline-deployment pipeline and a PowerShell module
  automating release packaging and transfer to production servers.
- **Applications Engineer, HealthLink · 2017-2019.** Supported core
  health-messaging services for 15,000+ medical organisations across AU/NZ;
  built WASUP (PowerShell) to auto-update 30+ machines.
- **Applications Engineer, 2degrees · 2012-2017.** Ran 24×7 support for CRM,
  payments and self-care systems; built 30+ "UFO" operations tools (Oracle,
  Shell, SOAP) that let Customer Care self-serve and cut Operations workload.
