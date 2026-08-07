# FlexNode - README Specification

## Project Overview

FlexNode is a lightweight, pluggable storage virtualization API designed for **edge computing and IoT environments**. It provides a unified REST interface for managing local storage resources such as pools, volumes, snapshots, and clones across heterogeneous backend systems.

The system is designed to abstract storage complexity while remaining minimal enough to run on constrained edge hardware. FlexNode does not provide replication or distributed storage; instead, it focuses on **local-node storage control with extensible backend support**.

---

## Core Design Principles

- **Edge-first architecture** — optimized for low-resource devices
- **Local storage only** — no built-in replication or clustering
- **Backend abstraction** — unified API over multiple storage systems
- **Minimal footprint** — lightweight deployment suitable for IoT
- **Extensibility** — plugin-based driver system for storage backends
- **API-driven control** — REST-first design for automation and integration

---

## Full Feature List

### 1. Core Storage Virtualization
- Pluggable backend architecture
  - ZFS support
  - LVM-thin support
  - Future backends: btrfs, NVMe-oF, cloud gateway adapters
- Unified storage abstraction layer
- Volume lifecycle management
  - Create, delete, resize
  - Attach metadata
- Pool management system
  - Create and manage storage pools
  - Backend-aware configuration

---

### 2. Snapshot & Clone System
- Point-in-time snapshots
- Snapshot listing and deletion
- Volume cloning from snapshots
- Snapshot retention policies (configurable)
- Snapshot metadata tracking

---

### 3. REST API Layer
- Full CRUD operations for:
  - Pools
  - Volumes
  - Snapshots
  - Clones
- Backend selection via API
- JSON-based request/response structure
- Stateless API design
- Versioned endpoints for backward compatibility

---

### 4. Edge & IoT Optimization
- Lightweight runtime footprint
- Designed for embedded Linux environments
- Minimal dependency stack
- Local-only storage operations
- Offline-capable node operation

---

### 5. Automation & Integration (#8)
- Webhook event system for:
  - Volume creation
  - Snapshot events
  - Pool changes
- Template-based volume provisioning
- Integration hooks for orchestration systems
- CLI automation support for scripting workflows

---

### 6. Developer & Community Features (#10)
- Plugin system for custom storage drivers
- Standardized driver interface specification
- Versioned API schema evolution
- Example deployments for edge nodes
- Contributor documentation and roadmap visibility

---

### 7. Observability & Operations
- Health checks for pools and volumes
- Storage usage metrics
- Logging system for API and backend events
- Basic audit trail for storage operations
- Status reporting per node

---

### 8. Security Features
- API authentication support (token-based)
- Role-based access control (RBAC)
- Optional volume encryption support (backend dependent)
- Secure configuration handling
- Audit logging for sensitive operations

---

### 9. Performance & Optimization
- Thin provisioning support (backend dependent)
- Compression and deduplication (backend dependent)
- Volume tiering hints (future capability)
- Efficient snapshot handling
- Lightweight API execution model

---

## Non-Goals

- No distributed storage system
- No replication between nodes
- No cloud-native orchestration layer
- No full hypervisor or VM management

---

## Specification Branding License (SBL):  
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

Optional:
- Specification Branding License (SBL)
  - attribution-free commercial deployment
  - pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/flexnode/](https://roxanneardary.com/flexnode/)  

---

## License & Notice Requirements

FlexNode is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- FlexNode specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
