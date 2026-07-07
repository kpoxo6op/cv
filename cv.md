---
mainfont: "Latin Modern Mono Light"
geometry:
- margin=25mm
- heightrounded
block-headings: true
---

# Boris Khasanov

**Senior Platform / DevOps / SRE Engineer**

[bouresk@outlook.com](mailto:bouresk@outlook.com) |
[+64 22 171 2798](tel:64221712798) | [borisAsCode.com](https://borisascode.com) |
Auckland, NZ | NZ citizen

Platform engineer with 13+ years building and running mission-critical
distributed systems across cloud and on-prem. I take end-to-end ownership of
ambiguous, high-stakes platform work in regulated, change-controlled
environments, spanning infrastructure-as-code, CI/CD, security and
observability, and deliver it to run unattended. Deep specialism in event
streaming and Kubernetes, with a strong bias for automation and clear
documentation.

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

### Senior Platform Engineer, Westpac New Zealand

**May 2025 – Present · Event Streaming · Auckland** · [westpac.co.nz](https://westpac.co.nz/)

Ran and modernised the bank's business-critical Confluent Kafka
platform across on-prem OpenShift and Azure.

- **Owned the ZooKeeper-to-KRaft migration end to end** for a stretched
  12-broker cluster across two data centres: Sandpit to Production, all five
  Confluent phases, zero customer data loss. Mapped each phase to repeatable Git
  tags and CloudBees pipelines and wrote reversible, idempotent runbooks so any
  on-call engineer can run or roll back a phase unattended.
- **Built a greenfield "2.5 data centre" KRaft controller platform on Azure**
  from first commit to Production: CIS-hardened RHEL 9 VMs, short-lived
  Vault-issued Azure credentials, automated Venafi certificate renewal, and
  persistent metadata disks with idempotent VM rebuild.
- **Pioneered agentic AI delivery and drove its adoption across the engineering
  chapter**: wired 9+ enterprise systems (Jira, Bitbucket, CloudBees,
  ServiceNow, Splunk, Azure) into GitHub Copilot through reusable skills, and
  built a self-correcting agent loop that files the ticket, applies Terraform via
  CloudBees, verifies the result and raises human-reviewable PRs. Used it to
  stand up a stretched dual-DC Kafka cluster in a day.
- **Set engineering standards** (conventional commits, automated changelogs,
  rollback-safe pipelines, runbooks), mentored engineers, and represented Event
  Streaming to Cloud, Security, Vault and the Confluent vendor relationship.

### Platform Engineer, Westpac New Zealand

**June 2021 – May 2025 · Event Streaming · Auckland** · [westpac.co.nz](https://westpac.co.nz/)

Architected, automated and operated the bank's event-streaming platform on
Confluent Kafka across on-prem, AWS and Confluent Cloud.

- **Delivered a six-month programme migrating 20+ internal customers to new data
  centres** on a stretched cluster: strategy, unified deployment pipeline,
  topic-placement tooling (Kafka Self-Balancing rebalancer), runbooks, customer
  comms, and the Sandpit-to-Production cut-over.
- **Led the Confluent Cloud migration** off on-prem Kafka: AWS EKS + Confluent
  Cloud over PrivateLink/VPC endpoints, cross-cluster linking with consumer-offset
  sync, private Schema Registry, BYOK and RBAC, with self-service migration docs
  and a `make workload` onboarding target so customers could migrate themselves.
- **Built bring-your-own CloudBees EC2 build agents** with IAM-based access,
  removing a manual SSO step and on-prem dependency, and moved pipeline secrets
  from Vault to AWS Secrets Manager for cloud segregation.
- **Built "BrokerRolla"** (automated rolling-restart for Confluent Kafka on
  Kubernetes) and shipped internal products Skibidi and 20Weeks On-Call
  (Next.js, PagerDuty, Kubernetes) that removed manual on-call and timesheet toil.
- **Ran 24×7 on-call** for the platform, leading incident response,
  troubleshooting and blameless postmortems.

### Earlier career

- **Platform Engineer, Fraedom (now Visa) · 2019–2021.** Built Octopus Deploy
  pipelines, including an offline-deployment pipeline and a PowerShell module
  automating release packaging and FTP transfer to production servers.
- **Applications Engineer, HealthLink · 2017–2019.** Supported core
  health-messaging services for 15,000+ medical organisations across AU/NZ; built
  WASUP (PowerShell) to auto-update 30+ machines and an Apigee/Docker developer
  onboarding tool.
- **Applications Engineer, 2degrees · 2012–2017.** Ran 24×7 support for CRM,
  payments and self-care systems; built 30+ "UFO" operations tools (Oracle,
  Shell, SOAP) that let Customer Care self-serve and cut Operations workload.

## Other

References available on request · [borisAsCode.com](https://borisascode.com)

