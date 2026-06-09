# Platform Ansible

Enterprise Platform Engineering Framework built with Ansible.

A modular Infrastructure as Code (IaC) project designed to automate the deployment and lifecycle management of enterprise infrastructure, Kubernetes platforms, core services, DevOps tooling, security services, and observability stacks across development, staging, and production environments.

---

## Overview

Platform Ansible provides a phased deployment model that separates infrastructure concerns into independent automation domains.

The project follows Platform Engineering principles:

* Infrastructure as Code (IaC)
* Immutable Infrastructure
* GitOps-ready Architecture
* Security by Default
* Reusable Ansible Roles
* Multi-Environment Support
* CI/CD Integration
* Enterprise Observability

---

## Architecture

```text
Platform Ansible
│
├── Phase 1 - Foundation
│   ├── Users
│   ├── SSH Hardening
│   ├── DNS
│   ├── NTP
│   ├── Firewall
│   └── Kernel Tuning
│
├── Phase 2 - Platform
│   ├── Containerd
│   ├── Kubernetes (Kubespray)
│   ├── MetalLB
│   ├── Ingress NGINX
│   └── Cert Manager
│
├── Phase 3 - Core Services
│   ├── Ceph
│   ├── MinIO
│   ├── PostgreSQL
│   ├── Redis
│   ├── RabbitMQ
│   ├── Vault
│   └── Keycloak
│
├── Phase 4 - DevOps
│   ├── GitLab
│   ├── GitLab Runner
│   ├── Harbor
│   ├── ArgoCD
│   ├── Nexus
│   └── SonarQube
│
└── Phase 5 - Observability
    ├── Prometheus
    ├── Grafana
    ├── AlertManager
    ├── Loki
    ├── Elasticsearch
    ├── Kibana
    ├── Fluent Bit
    └── OpenTelemetry
```

---

## Repository Structure

```text
platform-ansible/
│
├── phase1-foundation/
├── phase2-platform/
├── phase3-services/
├── phase4-devops/
└── phase5-observability/
```

Each phase is designed as an independent Ansible project and can be executed individually or integrated into a complete platform deployment pipeline.

---

## Features

### Infrastructure Foundation

* Operating System Baseline
* User Management
* SSH Hardening
* DNS Configuration
* Time Synchronization
* Firewall Management
* Kernel Optimization

### Kubernetes Platform

* Multi-Node Kubernetes Deployment
* High Availability Architecture
* Ingress Management
* Certificate Automation
* Load Balancer Integration

### Core Services

* Object Storage
* Distributed Storage
* Databases
* Message Brokers
* Authentication Services
* Secret Management

### DevOps Platform

* Git Repository Management
* CI/CD Pipelines
* GitOps Workflows
* Container Registry
* Artifact Management
* Code Quality Analysis

### Observability

* Metrics Collection
* Centralized Logging
* Distributed Tracing
* Dashboards
* Alerting
* Performance Monitoring

---

## Supported Platforms

### Operating Systems

* Debian 12
* Ubuntu 22.04 LTS
* Ubuntu 24.04 LTS

### Kubernetes

* Kubernetes 1.30+
* Kubespray

### Databases

* PostgreSQL
* Redis

### Storage

* Ceph
* MinIO

---

## Quick Start

Clone the repository:

```bash
git clone https://github.com/<your-account>/platform-ansible.git
cd platform-ansible
```

Install required collections:

```bash
ansible-galaxy collection install -r requirements.yml
```

Deploy Foundation Phase:

```bash
cd phase1-foundation
ansible-playbook playbooks/site.yml
```

Deploy Kubernetes Platform:

```bash
cd ../phase2-platform
ansible-playbook playbooks/site.yml
```

---

## Security

Security is integrated into every deployment phase:

* SSH Hardening
* Least Privilege Access
* Secret Management with Vault
* TLS Everywhere
* Firewall Enforcement
* Secure Defaults

---

## CI/CD Roadmap

* GitHub Actions
* GitLab CI
* Molecule Testing
* Ansible Lint
* YAML Lint
* Trivy Security Scanning
* Gitleaks Secret Detection

---

## Project Status

Current Version: **Active Development**

The project is being developed as a production-grade platform engineering framework and serves both as a personal portfolio project and a reusable automation platform for enterprise deployments.

---

## Author

**Soroush Hazeq Daneshvar**

Senior DevOps / Platform Engineer

Specializing in:

* Kubernetes
* Cloud Infrastructure
* Platform Engineering
* DevSecOps
* Infrastructure Automation
* Golang Development

---

## License

MIT License
