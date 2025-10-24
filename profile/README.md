# 🚀 Cerberus - Internal Developer Platform

<div align="center">

**Unleashing the Full Potential of Every Venture**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-AWS%20EKS-orange.svg)](https://aws.amazon.com/eks/)
[![GitOps](https://img.shields.io/badge/GitOps-ArgoCD-blue.svg)](https://argo-cd.readthedocs.io/)
[![IaC](https://img.shields.io/badge/IaC-OpenTofu-purple.svg)](https://opentofu.org/)

*From idea to production in hours, not weeks*

[Get Started](#-quick-start) • [Documentation](https://github.com/cerberus-platform-mop/cerberus) • [Architecture](#-platform-architecture) • [Contributing](CONTRIBUTING.md)

</div>

---

## 🎯 What is Cerberus?

**Cerberus** is a unified, multi-tenant Internal Developer Platform (IDP) designed specifically for venture studio operations. Built on modern cloud-native technologies, it empowers engineering teams to deploy and manage infrastructure with confidence, enabling **92% reduction in lead time** for new features and services—from 2-4 days down to 2-4 hours.

### ⚡ Why Cerberus?

We believe that every startup deserves to focus on what makes them unique—their vision, their customers, their breakthrough ideas. Not on solving the same engineering problems that have been solved many times before.

**The Problem:**
- Too many brilliant entrepreneurs spend weeks wrestling with deployment pipelines
- Security configurations become blockers instead of enablers
- Identical features are rebuilt across projects
- Innovation is strangled by "undifferentiated heavy lifting"

**The Solution:**
Cerberus provides **Golden Paths**—pre-configured, battle-tested templates that embody years of best practices. Developers go from "I have an idea" to "I have a running service" in under one hour.

### 🎁 What We Deliver

| Metric | Before Cerberus | With Cerberus | Improvement |
|--------|----------------|---------------|-------------|
| **New Service Deployment** | Weeks | < 1 hour | 98% faster |
| **Lead Time for Features** | 2-4 days | 2-4 hours | **92% reduction** |
| **Developer Productivity** | Baseline | +10-20% | Reduced friction |
| **Infrastructure Cost** | Baseline | -20-30% | Shared resources |
| **Incident Response** | Hours | < 15 minutes | 95% faster |
| **Support Cost** | Baseline | -40-60% | Automation |

---

## 🏗️ Platform Architecture

### Core Technology Stack

```
┌─────────────────────────────────────────────────────────────┐
│                    Developer Portal (GetPort.io)            │
│        Service Catalog • Golden Paths • Self-Service        │
└─────────────────────────────────────────────────────────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
┌───────▼────────┐   ┌────────▼────────┐   ┌───────▼────────┐
│   CI/CD        │   │  Infrastructure │   │  Kubernetes    │
│ GitHub Actions │   │ OpenTofu/TG     │   │  AWS EKS       │
│ GitOps/ArgoCD  │   │ Multi-Tenant    │   │  Multi-Tenant  │
└────────────────┘   └─────────────────┘   └────────────────┘
        │                     │                     │
        └─────────────────────┼─────────────────────┘
                              │
        ┌─────────────────────▼─────────────────────┐
        │         Observability & Security          │
        │  Prometheus • Grafana • OpenTelemetry     │
        │     Fluent Bit • Vault • Falco            │
        └───────────────────────────────────────────┘
```

### 🌟 Key Features

- **🎯 Golden Path Templates**: Pre-built, tested infrastructure templates for common patterns
- **🚀 Self-Service Portal**: Single interface for service discovery, deployment, and monitoring
- **🔒 Security by Default**: Built-in security scanning, policy enforcement, and compliance
- **📊 Enterprise Observability**: Centralized logging, metrics, and distributed tracing
- **🔄 GitOps Workflows**: Declarative deployments with ArgoCD
- **🤖 AI-Enhanced Development**: Cursor rules-based standardization for consistent code generation
- **🏢 Multi-Tenant Architecture**: Complete isolation with shared infrastructure efficiency
- **📦 Portable by Design**: Clean detachment when ventures graduate

---

## 🚀 Quick Start

### Prerequisites

```bash
# Install required tools (macOS)
brew install gh terraform opentofu terragrunt kubectl

# Authenticate with GitHub
gh auth login
```

### Clone the Platform

```bash
# Clone main repository
git clone git@github.com:cerberus-platform-mop/cerberus.git
cd cerberus

# Run automated workspace setup (clones all components)
./setup-workspace.sh
```

### Get Your Interactive AI Introduction

Paste this into Cursor to get a role-specific introduction:

```markdown
Hello! I'm a new engineer joining the Cerberus Internal Developer Platform team. I'd like an interactive introduction customized to my role.

**My Details:**
- Role: [Platform Engineer | DevOps Engineer | Infrastructure Engineer | Kubernetes Engineer]
- Primary Interest: [AWS Account Factory | Infrastructure as Code | CI/CD Automation | Kubernetes & GitOps]

**What I'd like from this session:**
- [ ] Platform overview and architecture understanding
- [ ] Role-specific workspace navigation
- [ ] Resource discovery (docs, templates, guides)
- [ ] Next steps and learning path recommendations

Let's begin!
```

### Deploy Your First Service

```bash
# Coming soon: One-command service deployment
cerberus deploy --template golang-rest-api --name my-service
```

---

## 📦 Platform Components

Cerberus is organized into domain-specific repositories:

### 🔧 AWS Account Factory (AFT)
Automated AWS account provisioning and management using AWS Control Tower.

- [`aft-account-request`](https://github.com/cerberus-platform-mop/aft-account-request) - Account provisioning definitions
- [`aft-account-customizations`](https://github.com/cerberus-platform-mop/aft-account-customizations) - Account-specific configurations
- [`aft-global-customizations`](https://github.com/cerberus-platform-mop/aft-global-customizations) - Organization-wide settings

### 🏗️ Infrastructure as Code (IaC)
OpenTofu/Terragrunt modules and live infrastructure configurations.

- [`platform-iac-catalog`](https://github.com/cerberus-platform-mop/platform-iac-catalog) - Reusable infrastructure modules
- [`platform-iac-live`](https://github.com/cerberus-platform-mop/platform-iac-live) - Environment-specific deployments

### ⚙️ CI/CD Automation
Reusable GitHub Actions workflows and templates.

- [`gha-templates-iac`](https://github.com/cerberus-platform-mop/gha-templates-iac) - IaC workflow templates
- [`gha-action-semver`](https://github.com/cerberus-platform-mop/gha-action-semver) - Semantic versioning automation

### ☸️ Kubernetes & GitOps
Kubernetes configurations and GitOps deployments.

- [`platform-k8s-dev-live`](https://github.com/cerberus-platform-mop/platform-k8s-dev-live) - Development cluster configurations
- ArgoCD-based continuous delivery

---

## 🎭 Role-Based Navigation

### 👷 Platform Engineers
Build and maintain the core platform infrastructure.

**Start Here:**
- [Platform Architecture](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/cerberus-technical-architecture.md)
- [Workspace Setup Guide](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/guides/workspace-setup-guide.md)
- AFT Components (AWS Account Factory)

### 🔧 DevOps Engineers
Design and implement CI/CD pipelines and automation.

**Start Here:**
- [CI/CD Overview](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/guides/ci-cd-overview.md)
- [GitHub Actions Guide](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/guides/github-actions-guide.md)
- CI/CD Components

### 🏗️ Infrastructure Engineers
Build infrastructure modules and manage deployments.

**Start Here:**
- [IaC Catalog Guide](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/guides/iac-catalog-guide.md)
- [Terragrunt Documentation](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/guides/terragrunt-docs.md)
- IaC Components

### ☸️ Kubernetes Engineers
Manage Kubernetes clusters and GitOps workflows.

**Start Here:**
- [Kubernetes Overview](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/guides/kubernetes-overview.md)
- [GitOps Guide](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/guides/gitops-guide.md)
- K8s Components

---

## 📚 Documentation

### 📖 Essential Reading
- [Why Cerberus?](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/why-cerberus.md) - Platform philosophy and goals
- [Technical Architecture](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/cerberus-technical-architecture.md) - Comprehensive technical design
- [Architecture Decision Records](https://github.com/cerberus-platform-mop/cerberus/tree/main/_workspace/decisions) - Key architectural decisions

### 🎓 Learning Resources
- [New Engineer Onboarding](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/onboarding/new-engineer-onboarding.md)
- [Quick Start Guides](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/onboarding/quick-start-guides.md)
- [Implementation Guides](https://github.com/cerberus-platform-mop/cerberus/tree/main/_workspace/guides)

### 🔧 Technical Guides
- [IaC Catalog Template Guide](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/docs/iac-catalog-template-guide.md)
- [Repository Bootstrapping](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/docs/repository-bootstrapping-guide.md)
- [DNS Implementation Guide](https://github.com/cerberus-platform-mop/cerberus/blob/main/_workspace/docs/cerb3rus-dns-implementation-guide.md)

---

## 🤝 Contributing

We welcome contributions from engineers at all levels! Cerberus is built by the community, for the community.

### How to Contribute

1. **📚 Documentation**: Improve guides, add examples, clarify concepts
2. **🔧 Components**: Build new platform components or enhance existing ones
3. **🐛 Bug Reports**: Identify issues and help us improve
4. **💡 Feature Requests**: Suggest new capabilities and improvements
5. **🎓 Knowledge Sharing**: Share your experiences and best practices

### Contribution Guidelines

Please read our [Contributing Guide](CONTRIBUTING.md) for details on:
- Code of conduct
- Development workflow
- Pull request process
- Coding standards
- Testing requirements

**Quick Start for Contributors:**
```bash
# Fork the repository
gh repo fork cerberus-platform-mop/cerberus

# Create a feature branch
git checkout -b feature/amazing-feature

# Make your changes and commit
git commit -m "feat: add amazing feature"

# Push and create PR
git push origin feature/amazing-feature
gh pr create
```

---

## 🛡️ Security

Security is a top priority for Cerberus. We implement security best practices at every layer:

- **🔒 Zero Trust Architecture**: mTLS, Network Policies, Pod Security Standards
- **🔐 Secrets Management**: HashiCorp Vault integration
- **🔍 Security Scanning**: SAST, DAST, SCA, container vulnerability scanning
- **📋 Compliance**: Built-in SOC2, GDPR, PCI-DSS compliance patterns
- **🚨 Runtime Security**: Falco for threat detection and response

**Found a security vulnerability?** Please see our [Security Policy](SECURITY.md) for responsible disclosure procedures.

---

## 📊 Project Status

### Current Phase: Foundation (Months 1-3)

- ✅ Core infrastructure design complete
- ✅ Architecture Decision Records established
- 🚧 EKS cluster setup in progress
- 🚧 GetPort.io portal deployment
- 📅 First Golden Path template (Q1 2025)

### Roadmap

**Phase 1 (Months 1-3)**: Core Infrastructure
- EKS cluster with basic monitoring
- Developer portal deployment
- First Golden Path template
- Basic tenant provisioning

**Phase 2 (Months 4-6)**: Golden Paths Expansion
- Multiple service templates
- Enhanced CI/CD pipelines
- Advanced monitoring and alerting
- Self-service provisioning

**Phase 3 (Months 7-12)**: Enterprise Features
- ML-powered monitoring
- Automated tenant offboarding
- Policy-as-code enforcement
- Advanced deployment strategies

**Phase 4 (Months 13+)**: AI-Enhanced Operations
- Autonomous infrastructure optimization
- Predictive capacity planning
- Self-healing systems
- Advanced business intelligence

---

## 🌐 Community & Support

### Get Help

- **📚 Documentation**: Check our comprehensive docs in the main repository
- **💬 Discussions**: Join conversations in GitHub Discussions
- **🐛 Issues**: Report bugs or request features via GitHub Issues
- **📧 Email**: Contact the Platform Engineering team

### Stay Connected

- **GitHub Organization**: [@cerberus-platform-mop](https://github.com/cerberus-platform-mop)
- **Main Repository**: [cerberus](https://github.com/cerberus-platform-mop/cerberus)

---

## 📄 License

Cerberus is open source software licensed under the [Apache License 2.0](LICENSE).

---

## 🙏 Acknowledgments

Cerberus is built on the shoulders of giants. We're grateful to the open source community and these amazing projects:

- [Kubernetes](https://kubernetes.io/) - Container orchestration
- [ArgoCD](https://argo-cd.readthedocs.io/) - GitOps continuous delivery
- [OpenTofu](https://opentofu.org/) - Infrastructure as Code
- [GetPort.io](https://www.getport.io/) - Developer portal
- [Prometheus](https://prometheus.io/) & [Grafana](https://grafana.com/) - Observability
- And many more...

---

<div align="center">

**Built with ❤️ by the Ministry of Programming Platform Engineering Team**

*Empowering ventures to build the future, faster*

[Get Started](https://github.com/cerberus-platform-mop/cerberus) • [Documentation](https://github.com/cerberus-platform-mop/cerberus/tree/main/_workspace) • [Contributing](CONTRIBUTING.md) • [License](LICENSE)

</div>

