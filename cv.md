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

Platform engineer. 14 years in New Zealand banks, telcos and health IT. I look
after the platforms other teams depend on: Kafka, API gateways, the edge and the
pipelines around them. Most of my work is moving old, hand-built systems onto
managed platforms without breaking anything, then writing it down so the next
person doesn't have to ask me.

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
| Practice             | Runbooks, postmortems, wikis, DR planning |

## Experience

### ASB Bank

[asb.co.nz](https://www.asb.co.nz/) · Public API Squad · Auckland

#### Software Consultant - SRE (Contract) | August 2026 - Present

Joined the Public API squad in August. Most of the work below I picked up
myself.

- Moving legacy Kafka off physical hosts in two data centres to Confluent Cloud.
  Agreed the plan with the Kafka owners and the target platform team: topics
  first, then producers and consumers, then the cluster. GitOps all the way. I
  did the same migration at Westpac.
- Moving our public-facing Kong Gateway from home-built containers on RHEL 7 to
  the bank's managed Kong on AKS. Ansible runbooks, GitOps, Elastic dashboards
  and a rollback path for every step. One less custom stack for a small team to
  patch.
- Patching was a four-layer job done by hand: Ansible config, RHEL hosts,
  Qualys sidecars and code scan findings. The bank was rolling out AI agents on
  AKS that check out code and fix vulnerabilities on their own. I asked senior
  leadership to put our squad on it early. We were one of the first squads in,
  and manual patching went away.
- ASB has no Akamai team. Three or four squads click around the Akamai console,
  each in their own way. I am writing Terraform modules for network lists,
  client lists, EdgeWorkers and rules, plus a GitHub repo template, and using
  them for Public API first. Security agreed to the approach. Next is a demo at
  the fortnightly Akamai community so other squads can copy it.
- Payments NZ now requires CRL revocation checks on client certificates. I lead
  ASB's response: an EdgeWorker that rejects revoked certificates at the edge,
  and a scheduled GitHub Actions job that does the same checks on our side until
  the edge version is live.
- Found two wikis, one a copy of the other, with pages from 2015 to 2026 and no
  structure. Started a new one instead of fixing the old one. Recorded handover
  calls with senior engineers who had left the squad and turned them into wiki
  pages with a Whisper pipeline. Turned my own onboarding notes into the
  onboarding guide. Started writing postmortems from the Google template and got
  others writing them too.

### Westpac New Zealand

[westpac.co.nz](https://westpac.co.nz/) · Event Streaming · Auckland

#### Senior Platform Engineer | May 2025 - July 2026

Ran a 12-broker Confluent Kafka platform across two OpenShift data centres and
Azure.

- Built the monitoring: Grafana, Thanos and Splunk dashboards for Kafka, KRaft
  and broker logs, plus alerts and DLQ monitoring. It paid off when replication
  broke after KRaft patching. I found the cause, brought the brokers and Kafka
  Connect back, and wrote the PIR.
- Led the move from ZooKeeper to KRaft. Redesigned the controller quorum across
  three failure domains with a witness in Azure, so we can lose a data centre.
  Cut production over in stages and switched ZooKeeper off.
- Built the Azure witness properly: CMK-encrypted storage, safe rebuilds and
  credentials from Vault.
- Wrote migration scripts with dry-run mode and environment locks, and a safe
  rolling restart for all 12 brokers.
- Got the engineering chapter using AI agents. Connected GitHub Copilot to Jira,
  Bitbucket, CloudBees, ServiceNow, Splunk and Azure. Built a loop where the
  agent raises the ticket, applies Terraform, checks the result and opens a PR
  for a human. Used it to build a stretched dual-DC Kafka cluster in one day.

#### Platform Engineer | June 2021 - May 2025

Kafka migrations and delivery across on-prem OpenShift, AWS and Confluent Cloud.

- Moved 20+ teams to new data centres in six months. Built the pipeline, topic
  placement tooling, runbooks and cutover playbooks.
- Built the path to Confluent Cloud: EKS over PrivateLink, cluster linking with
  consumer offset sync, private Schema Registry, BYOK, RBAC and self-service
  onboarding.
- Wrote BrokerRolla for safe Kafka rolling restarts. Did on-call, ran incidents
  and postmortems.

### Earlier career

- **Platform Engineer, Fraedom (now Visa) · 2019-2021.** Octopus Deploy release
  pipelines and PowerShell release automation.
- **Applications Engineer, HealthLink · 2017-2019.** Health messaging for
  15,000+ medical organisations across AU/NZ. Wrote WASUP in PowerShell to
  auto-update 30+ machines.
- **Applications Engineer, 2degrees · 2012-2017.** 24×7 support for CRM,
  payments and self-care. Built 30+ ops tools (Oracle, Shell, SOAP) so Customer
  Care could sort things out without us.
