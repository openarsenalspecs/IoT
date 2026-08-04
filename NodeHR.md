# NodeHR

**Built for Organizations That Own Their Stack.**

NodeHR is an open-source, AI-powered HR concierge and workflow automation platform designed to replace repetitive HR work with secure, policy-aware automation. It runs inside your infrastructure, connects to your internal systems, and turns employee questions into completed workflows.

No SaaS lock-in. No black box HR bots. Full control, full transparency.

---

## 🚀 Core Capabilities

NodeHR is modular by design. Every system can be enabled, disabled, or extended independently.

### 🧠 AI HR Concierge
- Natural language HR assistant for employees
- Answers policy, benefits, and payroll questions
- Multi-turn contextual conversations
- Role-aware responses based on permissions
- AI escalation to human HR staff when needed
- Multi-language support

### 📚 Policy & Knowledge Engine
- HR handbook ingestion and indexing
- Retrieval-Augmented Generation (RAG) system
- Clause-level policy citation
- Versioned policy management
- Policy conflict detection
- Semantic search across internal documents

### 👥 Employee Self-Service
- Employee dashboard portal
- Benefits and compensation lookup
- Internal document access
- Company announcements feed
- Profile and dependency management
- Task and notification center

### 🕒 PTO & Leave Management
- PTO balance tracking
- Leave request submission via chat or UI
- Approval routing (manager → HR → admin)
- Calendar sync (Google / Outlook)
- Leave policy enforcement engine
- Conflict detection across teams

### 💰 Payroll & Compensation Support
- Pay stub retrieval integrations
- Compensation band visibility controls
- Reimbursement workflows
- Bonus and adjustment approvals
- Payroll issue routing system
- Tax form access links

### 🧾 Workflow Automation Engine
- Visual workflow builder
- Conditional logic routing
- Multi-step approval chains
- Automated task assignment
- SLA tracking and escalation rules
- Parallel and sequential workflows
- Workflow versioning

### 📝 Form & Document Automation
- Dynamic form generation
- AI-assisted form completion
- Secure file uploads
- Digital signatures support
- Template-based forms
- Auto-validation rules engine

### 🔐 Security & Compliance Layer
- AES-256 encryption at rest
- TLS 1.3 encryption in transit
- Field-level encryption for sensitive data
- Vault-based key management
- SSO / MFA authentication
- Role-Based Access Control (RBAC)
- Tamper-evident audit logs
- PII redaction before AI inference
- Air-gapped deployment support

### 🔌 Integrations Layer
- Slack integration
- Microsoft Teams integration
- Email + webhook support
- HRIS connectors (BambooHR, Workday, ADP, etc.)
- Google Workspace integration
- Microsoft 365 integration
- Calendar sync (Google / Outlook)
- Internal API + plugin SDK

### 📊 Analytics & Reporting
- HR ticket volume analytics
- Employee request pattern detection
- Workflow efficiency metrics
- Department-level insights
- AI usage and performance metrics
- Custom report builder
- Exportable compliance reports

### 🧩 Plugin Architecture
- Fully modular plugin system
- Organization-specific HR modules
- Regional compliance packs
- Union/workforce rule extensions
- Custom workflow plugins
- Sandboxed plugin execution

### 🖥️ Deployment & Infrastructure
- Docker-based deployment
- Kubernetes-ready architecture
- Helm charts included
- Self-hosted or private cloud
- Air-gapped enterprise support
- Horizontal scaling support
- High availability configurations

---

## 🧩 Architecture Overview

NodeHR is built as a layered system:

- **AI Layer** → LLM + RAG + policy reasoning  
- **Workflow Layer** → automation + approvals + routing  
- **Data Layer** → encrypted HR data + vector search  
- **Integration Layer** → HRIS, Slack, Teams, payroll systems  
- **Security Layer** → identity, encryption, audit logs  

Everything is designed to be modular and replaceable.

---

## 🔐 Security First Design

NodeHR assumes HR data is highly sensitive.

- No training on customer data
- All sensitive fields encrypted individually
- Identity-based access control for every request
- Full audit logs for every AI and human action
- Zero-trust architecture model

---

## ⚙️ Tech Stack

**Backend**
- Python
- FastAPI
- PostgreSQL + pgvector
- Redis
- Celery / Temporal

**AI Layer**
- Ollama / vLLM (local models)
- Retrieval-Augmented Generation (RAG)
- Structured policy graph engine

**Frontend**
- React
- Slack + Teams integrations
- Embeddable web widget

**Security**
- Keycloak (SSO / IAM)
- Vault (secrets + key management)
- OpenSSL (TLS / crypto layer)

**Deployment**
- Docker
- Kubernetes
- Helm charts

---

## 🧩 Modular Philosophy

Every feature in NodeHR is a module:

- Enable only what your organization needs
- Extend via plugins
- Replace components without breaking core system
- Deploy minimal or enterprise-scale configurations

---

## Specification Branding License (SBL)

### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/nodehr/](https://roxanneardary.com/nodehr/)  

---

## ⚖️ License & Notice Requirements

NodeHR is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

---
