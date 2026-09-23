---
mainfont: "Latin Modern Mono Light"
geometry:
- margin=20mm
- heightrounded
block-headings: true
---

# Boris Khasanov

**Senior Platform / DevOps / SRE Engineer**

[bouresk@outlook.com](mailto:bouresk@outlook.com) |
[+64 22 171 2798](tel:64221712798) | [borisAsCode.com](https://borisascode.com) |
Auckland, NZ | NZ citizen

Platform engineer with 14+ years building and running distributed systems
across cloud and on-prem. I take ambiguous, high-risk platform work from design
through production, leaving repeatable automation, operational visibility and
a clear handover. Deep experience in event streaming and Kubernetes within
regulated, change-controlled environments.

## Skills

| Category | Skills |
|----------------------:|--------------------------------------------------|
| Cloud                | Azure, AWS, Confluent Cloud |
| Containers           | Kubernetes, OpenShift, Helm, Confluent for Kubernetes (CFK), Docker |
| Infra as Code        | Terraform, Terraform Enterprise, Terragrunt |
| CI/CD & GitOps       | CloudBees/Jenkins, GitHub Actions, ArgoCD, Renovate |
| Confluent Kafka      | KRaft, Kafka Connect, Schema Registry, ksqlDB |
| Security & Secrets   | HashiCorp Vault, Venafi, CIS hardening, BYOK, RHEL 9 |
| Observability        | Prometheus, Grafana, Thanos, Alertmanager, Splunk, PagerDuty |

## Experience

### ASB Bank

[asb.co.nz](https://www.asb.co.nz/) · Public API / API Shared Platform · Auckland

#### Software Consultant - SRE (Contract) | August 2026 - Present

Lead ASB's bank-wide response to Payments NZ client certificates that require
CRL-based revocation checks, owning both the permanent edge design and an interim
ASB-side control for regulated API traffic.

- Introduced Akamai EdgeWorkers as the strategic request-time CRL enforcement
  path. Lead the architecture with Akamai to reject revoked Payments NZ
  certificates at the edge while preserving OCSP for existing client issuers.
- Own the end-to-end introduction of Terraform for ASB's Akamai platform.
  Consulted Security and gained the go-ahead for the approach; establishing
  GitHub Actions runner connectivity to make edge changes reviewable and repeatable.
- Architect and develop the interim ASB-side CRL control while EdgeWorkers is
  tested: a scheduled GitHub Actions workflow to retrieve and validate the CRL,
  match revoked certificates against client records and traffic, alert operators,
  and disable affected clients in the database.
- Lead automation of an assigned gMSA migration portfolio, replacing an opaque
  manual procedure with repeatable account discovery, AD/SQL access checks,
  Octopus/IIS cutover, runtime verification and rollback across environments.

\newpage

### Westpac New Zealand

[westpac.co.nz](https://westpac.co.nz/) · Event Streaming · Auckland

#### Senior Platform Engineer | May 2025 - July 2026

Led the modernisation and production reliability of a 12-broker Confluent Kafka
platform spanning two OpenShift data centres and Azure.

- Led the ZooKeeper-to-KRaft migration, redesigning the controller quorum
  across three failure domains using an Azure witness, completing the staged
  production cutover through phase 5 and retiring ZooKeeper deployment and
  monitoring.
- Delivered the Azure witness as durable infrastructure with stable networking,
  CMK-encrypted persistent metadata, idempotent rebuilds, controller-ID
  migration and dynamic Vault-backed credentials.
- Delivered Enterprise ML infrastructure through CloudBees and Terraform
  pipelines, production Vault bootstrap, private Azure AI Speech endpoints and
  credential-propagation safeguards.
- Pioneered agentic AI delivery and drove its adoption across the engineering
  chapter: wired 9+ enterprise systems (Jira, Bitbucket, CloudBees,
  ServiceNow, Splunk, Azure) into GitHub Copilot through reusable skills, and
  built a self-correcting agent loop that files the ticket, applies Terraform via
  CloudBees, verifies the result and raises human-reviewable PRs. Used it to
  stand up a stretched dual-DC Kafka cluster in a day.
- Made high-risk platform changes repeatable through environment-locked
  migration automation with dry-run support and guarded Azure-controller
  handling, plus safe, selective rolling restarts for all 12 brokers.
- Built operational visibility across Grafana, Thanos and Splunk with dual-DC
  Kafka, KRaft and broker-log dashboards, request-metrics alerts, DLQ monitoring
  and idempotent deployment. Used it to diagnose a production replication
  failure after KRaft patching, restore brokers and Kafka Connect workers, and
  turn the cross-datacentre routing failure into PIRs and follow-up controls.

#### Platform Engineer | June 2021 - May 2025

Built and operated Kafka migration and delivery capabilities across on-prem
OpenShift, AWS and Confluent Cloud.

- Migrated 20+ internal teams to new data centres over six months, building the
  deployment pipeline, topic-placement tooling, runbooks and cutover playbooks
  used from sandpit through production.
- Delivered the migration platform for selected workloads to Confluent Cloud,
  connecting AWS EKS over PrivateLink/VPC endpoints and adding cluster linking
  with consumer-offset sync, private Schema Registry, BYOK, RBAC and
  self-service onboarding.
- Removed manual SSO and on-prem dependencies by building IAM-authenticated
  CloudBees EC2 agents and moving cloud pipeline secrets from Vault to AWS
  Secrets Manager.
- Built BrokerRolla to automate safe Kafka rolling restarts and supported the
  platform on call, leading incident response, troubleshooting and blameless
  postmortems.

### Earlier career

- **Platform Engineer, Fraedom (now Visa) · 2019-2021.** Built Octopus Deploy
  pipelines, including an offline-deployment pipeline and a PowerShell module
  automating release packaging and FTP transfer to production servers.
- **Applications Engineer, HealthLink · 2017-2019.** Supported core
  health-messaging services for 15,000+ medical organisations across AU/NZ; built
  WASUP (PowerShell) to auto-update 30+ machines and an Apigee/Docker developer
  onboarding tool.
- **Applications Engineer, 2degrees · 2012-2017.** Ran 24×7 support for CRM,
  payments and self-care systems; built 30+ "UFO" operations tools (Oracle,
  Shell, SOAP) that let Customer Care self-serve and cut Operations workload.
