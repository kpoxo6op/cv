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

Senior platform engineer with 14+ years in regulated financial services. I move
legacy data and integration platforms onto managed, observable, recoverable
foundations: Kafka to Confluent Cloud, self-hosted Kong to AKS, ClickOps to
Terraform, manual patching to AI agents. I find the gap without being asked,
get the right senior people aligned and deliver without drama, leaving the team
runbooks, a living wiki and automation they can run without me.

## Skills

| Category | Skills |
|----------------------:|--------------------------------------------------|
| Data platforms       | Confluent Kafka & Confluent Cloud (KRaft, Connect, Schema Registry), SQL Server |
| Cloud & containers   | Azure, AKS, AWS, Kubernetes, OpenShift, Helm, Docker |
| Infra as Code        | Terraform, Terraform Enterprise, Terragrunt, Ansible |
| CI/CD & release      | Azure DevOps, GitHub Actions, CloudBees/Jenkins, Octopus Deploy, ArgoCD |
| Observability        | Grafana, Prometheus, Thanos, Elastic, Splunk, Alertmanager, PagerDuty |
| Security             | Vault, CMK/BYOK encryption, RBAC, vulnerability remediation, CIS hardening |
| Edge & API           | Akamai (EdgeWorkers, network/client lists), Kong Gateway, F5 |
| AI engineering       | Autonomous patching agents, GitHub Copilot agents, Whisper pipelines |
| Practice             | DR design, runbooks, blameless postmortems, wiki and knowledge ownership |

## Experience

### ASB Bank

[asb.co.nz](https://www.asb.co.nz/) · Public API Squad · Auckland

#### Software Consultant - SRE (Contract) | August 2026 - Present

Self-directed lead contractor on one of ASB's largest internet-facing
platforms, driving platform modernisation, security automation and engineering
practice across squads.

- **Kafka to Confluent Cloud.** Lead the migration of legacy Kafka on physical
  hosts across two data centres to Confluent Cloud. Agreed the phased plan with
  Kafka SMEs and the target platform team: topics, producers and consumers
  first, then the cluster, delivered through GitOps. Same pattern I delivered
  at Westpac.
- **Kong Gateway to managed AKS.** Lead the move of the public-facing Kong
  Gateway from self-built containers on RHEL 7 hosts in two data centres to
  the bank's managed Kong on AKS, with Ansible runbooks, GitOps, Elastic
  observability, rollback paths and a full audit trail. Removes a four-layer
  patching burden (gateway config, hosts, runtime scanning, code findings) from
  a small team.
- **AI-driven vulnerability patching.** Engaged senior technology leadership
  directly to get the squad onboarded among the first to the bank's AKS-hosted
  AI agents that check out code and patch vulnerabilities autonomously,
  replacing manual laptop patching. Engineers now remediate alongside the AI
  platform team.
- **Akamai as code across the bank.** ASB has no central Akamai team and 3-4
  squads manage it by ClickOps. Building reusable Terraform modules (network
  lists, client lists, EdgeWorkers, rules) and a GitHub repository template,
  proven first on Public API, with Security, Akamai and network engineering on
  board. Demo at the fortnightly Akamai community to win adoption on merit,
  no mandate needed.
- **Payments NZ certificate revocation.** Lead the bank-wide response to CRL
  checks for Payments NZ client certificates: EdgeWorkers enforcement at the
  edge, plus an interim scheduled control that validates the CRL, matches
  revoked certificates to client records, alerts and disables affected clients.
- **Knowledge and ownership uplift.** Replaced two duplicated, unstructured
  wikis (content back to 2015) with a structured knowledge base. Used AI to
  assess the old wiki, built a Whisper pipeline turning recorded handovers with
  departing senior engineers into wiki pages, turned my own onboarding trail
  into the team's onboarding guide, and introduced Google-style blameless
  postmortems that the team now writes too.

### Westpac New Zealand

[westpac.co.nz](https://westpac.co.nz/) · Event Streaming · Auckland

#### Senior Platform Engineer | May 2025 - July 2026

Owned the reliability and modernisation of the bank's 12-broker Confluent Kafka
data platform spanning two OpenShift data centres and Azure.

- Built the platform's observability across Grafana, Thanos and Splunk: dual-DC
  Kafka, KRaft and broker-log dashboards, request-metrics alerts and DLQ
  monitoring. Used it to diagnose a production replication failure, restore
  brokers and Kafka Connect workers, and turn the incident into PIRs and
  follow-up controls.
- Led the ZooKeeper-to-KRaft migration, redesigning the controller quorum across
  three failure domains with an Azure witness so the platform survives the loss
  of a data centre; completed the staged production cutover and retired
  ZooKeeper.
- Delivered the Azure witness as durable infrastructure with CMK-encrypted
  persistent metadata, idempotent rebuilds and dynamic Vault-backed credentials.
- Made high-risk platform changes repeatable through environment-locked
  migration automation with dry-run support, plus safe, selective rolling
  restarts for all 12 brokers.
- Pioneered agentic AI delivery across the engineering chapter: wired 9+
  enterprise systems (Jira, Bitbucket, CloudBees, ServiceNow, Splunk, Azure)
  into GitHub Copilot and built a self-correcting agent loop that files the
  ticket, applies Terraform, verifies the result and raises reviewable PRs.
  Used it to stand up a stretched dual-DC Kafka cluster in a day.

#### Platform Engineer | June 2021 - May 2025

Built and operated Kafka migration and delivery capabilities across on-prem
OpenShift, AWS and Confluent Cloud.

- Migrated 20+ internal teams to new data centres over six months, building the
  deployment pipeline, topic-placement tooling, runbooks and cutover playbooks
  used from sandpit through production.
- Delivered the migration platform to Confluent Cloud: AWS EKS over PrivateLink,
  cluster linking with consumer-offset sync, private Schema Registry, BYOK, RBAC
  and self-service onboarding.
- Built BrokerRolla to automate safe Kafka rolling restarts; on call for the
  platform, leading incident response and blameless postmortems.

### Earlier career

- **Platform Engineer, Fraedom (now Visa) · 2019-2021.** Octopus Deploy release
  pipelines and PowerShell release automation to production.
- **Applications Engineer, HealthLink · 2017-2019.** Core health-messaging
  services for 15,000+ medical organisations across AU/NZ; PowerShell fleet
  auto-update tooling.
- **Applications Engineer, 2degrees · 2012-2017.** 24×7 support for CRM,
  payments and self-care; built 30+ operations tools (Oracle SQL, Shell, SOAP).
