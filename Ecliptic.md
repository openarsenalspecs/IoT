# Ecliptic

**A New Orbit for the Internet.**

Ecliptic is a fully decentralized, encrypted, and self-healing web hosting and networking system designed to eliminate reliance on centralized data centers. Every participating machine becomes part of a global mesh that stores, mirrors, and serves web content securely and redundantly.

---

## 🌐 Overview

Ecliptic transforms the internet into a distributed system where:
- Websites are not hosted in one place
- Data is not controlled by centralized servers
- Every node contributes storage, routing, and redundancy
- Content remains available even during outages or network failures

It is a peer-to-peer infrastructure layer for the next generation of the web.

---

## 🚀 Core Features

### 🌐 Decentralized Web Hosting
- Fully peer-to-peer hosting with no central servers
- Every node can store and serve web content
- Static websites supported in early versions (HTML, CSS, JS)
- Future support for dynamic applications via sandboxed execution

---

### 📦 Distributed Storage System
- Content-addressed storage using cryptographic hashes
- Automatic chunking of files into encrypted segments
- Distributed replication across multiple nodes
- Erasure coding for recovery of missing data fragments
- Compression and deduplication for storage efficiency

---

### 🔁 Redundancy & Self-Healing Network
- Automatic replication based on node reliability
- Continuous peer-to-peer health monitoring
- Auto-repair of missing or corrupted data
- Adaptive replication scaling based on network conditions
- No single point of failure in the system

---

### 🔐 End-to-End Encryption & Security
- All data encrypted before leaving the originating device
- Zero-trust architecture across all nodes
- Public/private key cryptography for identity and access control
- Secure peer communication using Noise Protocol framework
- Encrypted chunk storage requiring valid keys for access

---

### 🌍 Peer-to-Peer Networking Layer
- Built on libp2p for modular networking
- NAT traversal for seamless global connectivity
- Distributed Hash Table (DHT) for content discovery
- Gossip-based propagation for network state synchronization
- Multi-transport support (QUIC, TCP, UDP where applicable)

---

### 🧠 Smart Network Intelligence Layer
- Adaptive routing based on latency, bandwidth, and reliability
- Predictive node selection for optimal performance
- Dynamic replication tuning based on demand and health
- Load balancing across geographically distributed nodes
- Network heat mapping for congestion and failure detection
- Proactive redundancy before node outages occur

---

### 🆔 Decentralized Identity Layer
- Cryptographic identity system based on public/private keys
- Self-sovereign identity control (users own their identity)
- Multi-device identity linking without central accounts
- Permissioned content access using encryption keys
- Separation of node identity and user identity
- Optional identity-based groups and private circles
- Reputation-ready identity framework for future trust systems

---

### 🧩 Modular Plugin System
- Extensible architecture for community development
- WASM-based sandboxed plugin execution
- Plugins for storage, routing, indexing, and UI extensions
- Secure isolation between core system and plugins
- Hot-swappable modules without network disruption

---

### 🔎 Decentralized Indexing & Discovery
- No centralized search engines required
- Distributed indexing across participating nodes
- Content lookup via cryptographic hashes
- Local caching for fast retrieval
- Bloom filter-based existence checks

---

### 🖥️ Ecliptic Node Runtime
- Lightweight node client for desktop, server, and embedded devices
- Written primarily in Rust for performance and safety
- Handles storage, routing, replication, and serving
- Modular feature toggles per node
- Designed for low resource usage and wide hardware support

---

### 🧭 Networking Intelligence & Optimization
- Bandwidth-aware routing decisions
- Reputation-based node prioritization
- Geographic and latency-aware peer selection
- Self-organizing mesh topology
- Automatic rerouting during failures or congestion

---

### ⚡ Performance & Efficiency
- Compact encrypted storage design
- Streaming-based content delivery (no full downloads required)
- Lazy-loading distributed chunk retrieval
- Parallel fetching from multiple peers
- Local caching of frequently accessed content

---

### 🧭 Future Expansion Capabilities
- WASM-based decentralized application runtime
- Optional distributed compute layer
- Encrypted messaging and identity ecosystem
- Web publishing tools for non-technical users
- Federated governance and protocol evolution system

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
  - [https://roxanneardary.com/ecliptic/](https://roxanneardary.com/ecliptic/)

---

## 📜 License & Notice Requirements

Ecliptic is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- Ecliptic specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, refer to the AGPL-3.0+ license and the project's `notice.md`.

---

## 📡 Project Vision

Ecliptic is not just a hosting system—it is a shift in how the internet itself is structured.

Instead of centralized infrastructure, the web becomes:
- Distributed
- Self-healing
- Encrypted by default
- Owned collectively by its participants

**A New Orbit for the Internet.**  
