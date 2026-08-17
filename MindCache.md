# MindCache Specification
**Snippets. Stories. Synapses.**
- HTML Mirror:  [https://roxanneardary.com/mindcache-specification/](https://roxanneardary.com/mindcache-specification/)

---

## Specification Overview

MindCache is an open-source, modular specification for persistent AI memory and long-term state management.

MindCache defines a standardized architecture for storing, indexing, retrieving, sharing, versioning, archiving, governing, and recovering memory across individual AI agents and collaborative multi-agent systems.

Traditional AI systems commonly rely on context windows, temporary conversation histories, vector stores, or application-specific checkpoints. These approaches do not provide a complete, standardized memory infrastructure for persistent knowledge, granular retrieval, historical reconstruction, relationships between memories, cross-agent collaboration, archival storage, and controlled forgetting.

MindCache treats memory as durable infrastructure.

The specification is implementation independent, storage agnostic, model agnostic, and framework independent. Implementations may use different databases, vector engines, object stores, AI models, APIs, or orchestration frameworks while maintaining compatibility with the MindCache memory model.

---

# Objectives

MindCache establishes a common standard for:

- Persistent long-term agent memory
- Multi-modal memory
- Granular snippet retrieval
- Story and contextual memory reconstruction
- Synaptic relationship mapping
- Cross-agent memory sharing
- Version-controlled memory
- Memory archival
- On-demand archive retrieval
- Configurable forgetting policies
- Configurable retention policies
- Memory compression
- Modular storage backends
- Semantic and hybrid retrieval
- Memory provenance
- Memory security
- Privacy-aware memory management
- Auditable memory lifecycle management
- Interoperable agent memory infrastructure

---

# Core Design Principles

## Modular

Each major capability is implemented as an independent module with defined interfaces.

## Storage Agnostic

MindCache does not require a specific database, vector store, object store, or storage technology.

## Model Agnostic

Memory must not depend on a particular AI model or model provider.

## Framework Independent

MindCache can operate independently of agent frameworks and orchestration systems.

## Multi-Agent Native

Shared memory, private memory, permissions, synchronization, and cross-agent retrieval are first-class capabilities.

## Persistent

Memory must survive individual sessions, process restarts, agent redeployment, and infrastructure changes when configured for persistent storage.

## Granular

The system must support retrieving the smallest useful unit of information instead of requiring complete memory records or conversations.

## Version Controlled

Memory changes must be traceable through versions, revisions, snapshots, and historical states.

## Privacy Aware

Memory access, sharing, retention, redaction, and deletion must be controllable.

## Human Understandable

Memory structures, metadata, relationships, provenance, and lifecycle states should remain understandable to humans.

## Extensible

Implementations may add capabilities through optional plugins without changing the core specification.

## Open Standard

The specification defines interoperable concepts and interfaces rather than requiring a proprietary implementation.

---

# Memory Model

MindCache organizes persistent memory into three primary logical structures:

- Snippets
- Stories
- Synapses

These structures may exist independently or be connected to form a larger memory system.

---

# Core Modules

## Core Memory Module

The Core Memory Module defines the fundamental MindCache memory model.

It provides:

- Memory identifiers
- Memory types
- Memory content
- Memory metadata
- Memory timestamps
- Memory ownership
- Agent associations
- Session associations
- Workspace associations
- Memory status
- Memory provenance
- Memory confidence
- Memory importance
- Memory relationships
- Memory lifecycle state

The Core Memory Module establishes the common representation used by other MindCache modules.

---

## Snippet Module

The Snippet Module manages small, independently retrievable pieces of information.

A snippet may represent:

- A fact
- A sentence
- A paragraph
- A quote
- An instruction
- A note
- An observation
- A code fragment
- An API response
- A search result
- An individual record
- An embedded object
- A section of a larger document

The Snippet Module provides:

- Unique snippet identifiers
- Semantic indexing
- Metadata tagging
- Partial retrieval
- Granular retrieval
- Independent version history
- Source references
- Provenance
- Context references
- Relevance scoring
- Snippet relationships

Implementations should allow an agent to retrieve only the relevant portion of stored information when a complete memory record is unnecessary.

---

## Story Module

The Story Module combines snippets and events into meaningful contextual memory.

Stories may represent:

- Conversations
- Workflows
- Research sessions
- Projects
- Customer histories
- Agent task histories
- Decision histories
- Long-running processes

The Story Module provides:

- Timeline reconstruction
- Context preservation
- Event ordering
- Historical playback
- Story summarization
- Incremental updates
- Related snippet retrieval
- Story versioning
- Context reconstruction
- Event relationships

Stories should allow agents to recover meaningful context without requiring every underlying memory item to be loaded.

---

## Synapse Module

The Synapse Module defines relationships between memories.

Synapses may represent:

- Parent-child relationships
- Related concepts
- References
- Causal relationships
- Dependencies
- Similarity relationships
- Temporal relationships
- Knowledge graph relationships
- Cross-agent references

The Synapse Module provides:

- Relationship creation
- Relationship weighting
- Relationship metadata
- Graph traversal
- Multi-hop retrieval
- Association discovery
- Related-memory discovery
- Dependency tracing
- Cross-agent relationships
- Relationship versioning

Synapses allow MindCache to represent connections between otherwise independent pieces of memory.

---

## Persistence Module

The Persistence Module provides durable storage for memory.

It provides:

- Cross-session persistence
- Durable state
- Automatic recovery
- Incremental updates
- Persistent agent state
- Persistent workspace state
- Persistent shared memory
- Storage transactions
- Recovery after interruption

The Persistence Module must separate memory semantics from the underlying storage implementation.

---

## Index Module

The Index Module creates searchable representations of memory.

It supports:

- Semantic indexing
- Vector indexing
- Keyword indexing
- Metadata indexing
- Temporal indexing
- Agent indexing
- Session indexing
- Workspace indexing
- Relationship indexing
- Full-text indexing

The Index Module may use multiple indexes simultaneously.

---

## Retrieval Module

The Retrieval Module provides on-demand access to stored memory.

It supports:

- Semantic search
- Keyword search
- Hybrid search
- Similarity search
- Metadata filtering
- Time filtering
- Agent filtering
- Workspace filtering
- Relationship-aware retrieval
- Context-aware retrieval
- Ranking
- Re-ranking
- Citation support
- Snippet extraction
- Story reconstruction
- Multi-hop retrieval

Retrieval must support both broad and granular queries.

An implementation should be able to return:

- Complete memories
- Individual snippets
- Relevant paragraphs
- Specific facts
- Related memories
- Story segments
- Connected memory chains
- Historical versions

The Retrieval Module should minimize unnecessary context retrieval when a smaller segment can satisfy the request.

---

## Version Module

The Version Module manages memory history.

It provides:

- Revision history
- Immutable versions
- Version identifiers
- Change tracking
- Difference comparison
- Rollback
- Snapshots
- Snapshot restoration
- Historical retrieval
- Version provenance
- Concurrent change tracking

Memory versions must remain distinguishable from the current memory state.

---

## Archive Module

The Archive Module provides long-term archival storage.

It defines three logical storage tiers.

### Hot Storage

Frequently accessed memory optimized for rapid retrieval.

### Warm Storage

Less frequently accessed memory maintained for continued availability.

### Cold Storage

Long-term archived memory optimized for durability and storage efficiency.

The Archive Module provides:

- Tiered storage
- Automatic migration
- Configurable migration policies
- Archive creation
- Archive indexing
- Archive retrieval
- On-demand restoration
- Archive lifecycle management
- Cold storage support
- Archive metadata
- Archive integrity verification

Archived information must remain retrievable according to its retention and access policies.

Archiving must not automatically mean forgetting.

---

## Retention and Forgetting Module

The Retention and Forgetting Module controls how long memory remains active, archived, compressed, or deleted.

Policies may consider:

- Age
- Importance
- Usage frequency
- Confidence
- Memory score
- Relevance
- Access history
- Organizational policy
- User policy
- Agent policy
- Legal or compliance requirements

The module supports:

- Retention policies
- Expiration policies
- Soft deletion
- Hard deletion
- Archival instead of deletion
- Manual deletion
- Policy-based deletion
- Memory restoration where permitted
- Deletion auditing

Forgetting must be distinguishable from archival.

---

## Compression Module

The Compression Module reduces memory volume while preserving useful information.

It supports:

- Summarization
- Story condensation
- Duplicate detection
- Duplicate removal
- Similarity clustering
- Context compression
- Memory consolidation
- Historical consolidation
- Storage optimization

Compressed memory should preserve provenance and relationships to the original information where technically possible.

---

## Collaboration Module

The Collaboration Module provides multi-agent memory capabilities.

It supports:

- Private memory
- Shared memory
- Team memory
- Agent workspaces
- Shared workspaces
- Cross-agent retrieval
- Cross-agent references
- Memory synchronization
- Shared context
- Collaborative knowledge
- Memory permissions
- Workspace permissions

The module must support separation between private and shared memory.

---

## Security Module

The Security Module protects memory and memory operations.

It supports:

- Authentication
- Authorization
- Encryption
- Access control
- Memory isolation
- Workspace isolation
- Permission-aware retrieval
- Audit logging
- Digital signatures
- Secure memory sharing

Security policies must be applicable to individual memories, snippets, stories, relationships, agents, users, and workspaces where supported.

---

## Privacy Module

The Privacy Module manages privacy-sensitive memory operations.

It supports:

- Private memory
- Shared memory
- Organizational memory
- Redaction
- Data masking
- Consent policies
- Privacy-aware retention
- Controlled information sharing
- Memory access restrictions
- Privacy-aware deletion

---

## Metadata and Provenance Module

The Metadata and Provenance Module maintains information describing each memory.

Metadata may include:

- Identifier
- Author
- Agent
- User
- Session
- Workspace
- Timestamp
- Version
- Tags
- Categories
- Confidence
- Importance
- Provenance
- Source
- Security level
- Access permissions
- Retention policy
- Lifecycle state

Provenance should allow an implementation to identify where memory originated and how it was transformed.

---

## API Module

The API Module defines standard interfaces for interacting with MindCache.

Core operations include:

- Create Memory
- Read Memory
- Update Memory
- Delete Memory
- Search Memory
- Retrieve Snippets
- Retrieve Stories
- Navigate Synapses
- Archive Memory
- Restore Memory
- Link Memories
- Version Memory
- Export Memory
- Import Memory

Implementations may expose these operations through:

- REST
- GraphQL
- gRPC
- SDK interfaces
- Local APIs
- Internal service interfaces

---

## Import and Export Module

The Import and Export Module provides interoperability between MindCache implementations.

Supported formats may include:

- JSON
- Markdown
- YAML
- CSV
- SQL
- Binary snapshots

The module supports:

- Full memory export
- Selective memory export
- Full memory import
- Selective memory import
- Version preservation
- Metadata preservation
- Provenance preservation
- Relationship preservation
- Archive migration
- Backup restoration

---

## Analytics Module

The Analytics Module provides operational and memory-quality measurements.

It may track:

- Memory growth
- Storage utilization
- Retrieval latency
- Retrieval frequency
- Retrieval success
- Memory quality
- Relationship density
- Agent memory usage
- Archive utilization
- Retention statistics
- Compression statistics
- Memory lifecycle activity

Analytics must not require exposing memory contents when aggregate metrics are sufficient.

---

## Governance Module

The Governance Module provides policy and administrative controls.

It supports:

- Memory governance policies
- Organizational policies
- Compliance controls
- Retention enforcement
- Access policy enforcement
- Approval workflows
- Audit history
- Data lifecycle policies
- Administrative controls
- Policy versioning

---

# Optional Plugin Modules

Optional plugins extend MindCache without requiring changes to the core memory specification.

## Embedding Plugin

Provides configurable embedding generation.

Capabilities may include:

- Text embeddings
- Image embeddings
- Multi-modal embeddings
- Local embedding models
- Remote embedding services
- Embedding versioning
- Embedding migration

---

## Reranking Plugin

Improves retrieval ordering.

Capabilities may include:

- Semantic reranking
- Cross-encoder reranking
- Relevance scoring
- Context-aware ranking
- Agent-specific ranking

---

## Knowledge Graph Plugin

Extends Synapses into a dedicated knowledge graph system.

Capabilities may include:

- Entity extraction
- Relationship extraction
- Graph construction
- Graph traversal
- Entity resolution
- Knowledge graph querying

---

## OCR Plugin

Extracts memory from visual documents.

Capabilities may include:

- Image OCR
- PDF OCR
- Document OCR
- Region extraction
- Text provenance
- Layout-aware extraction

---

## Audio Memory Plugin

Adds audio ingestion and retrieval.

Capabilities may include:

- Speech transcription
- Speaker identification
- Timestamped segments
- Audio embeddings
- Transcript snippets
- Audio segment retrieval

---

## Video Memory Plugin

Adds video memory processing.

Capabilities may include:

- Scene detection
- Frame extraction
- Video transcription
- Object detection
- Timestamped events
- Video segment retrieval
- Multi-modal video indexing

---

## Document Intelligence Plugin

Adds advanced document processing.

Capabilities may include:

- Document parsing
- Section extraction
- Table extraction
- Metadata extraction
- Document summarization
- Document relationship mapping

---

## Agent Framework Plugin

Provides integrations with external agent frameworks.

Plugins may provide:

- Memory adapters
- Checkpoint adapters
- Context adapters
- Agent lifecycle hooks
- Retrieval hooks
- Memory synchronization

MindCache remains independent of any particular framework.

---

## Model Provider Plugin

Provides optional integrations with AI model providers.

Capabilities may include:

- Embedding generation
- Summarization
- Memory classification
- Importance scoring
- Relevance scoring
- Compression
- Extraction

---

## Storage Provider Plugin

Provides additional storage backends.

A storage plugin may implement:

- Memory persistence
- Index persistence
- Archive storage
- Object storage
- Vector storage
- Distributed storage

---

## Sync Plugin

Provides synchronization between MindCache installations.

Capabilities may include:

- Agent synchronization
- Workspace synchronization
- Device synchronization
- Conflict detection
- Conflict resolution
- Incremental synchronization

---

## Backup Plugin

Provides external backup capabilities.

Capabilities may include:

- Scheduled backups
- Incremental backups
- Encrypted backups
- Snapshot backups
- Remote backup storage
- Backup verification
- Disaster recovery

---

## Encryption Plugin

Provides additional encryption capabilities.

Capabilities may include:

- At-rest encryption
- Field-level encryption
- Memory-level encryption
- Key management integration
- Key rotation
- Encrypted export

---

## Compliance Plugin

Provides specialized compliance controls.

Capabilities may include:

- Retention enforcement
- Data classification
- Audit reporting
- Policy validation
- Access reporting
- Deletion verification

---

# Storage Compatibility

MindCache does not require a particular storage engine.

Possible implementations include:

- PostgreSQL
- SQLite
- MySQL
- MongoDB
- Redis
- Cassandra
- Elasticsearch
- OpenSearch
- FAISS
- Milvus
- Weaviate
- Chroma
- Qdrant
- Object storage
- Distributed storage systems

Storage providers should be implemented through the Storage Module or Storage Provider Plugin.

---

# Memory Lifecycle

A MindCache implementation should support the following lifecycle:

1. Creation
2. Validation
3. Metadata assignment
4. Indexing
5. Versioning
6. Retrieval
7. Sharing
8. Updating
9. Archiving
10. Compression
11. Forgetting
12. Recovery

Memory may move between lifecycle states according to configured policies.

---

# Retrieval Requirements

MindCache retrieval must support both complete and partial memory access.

A query may request:

- A complete memory
- A snippet
- A range of information
- A story segment
- A historical version
- Related memories
- A connected memory path
- A specific time period
- A specific agent's memory
- A specific workspace's memory

Retrieval systems should return the smallest useful memory unit when requested.

Retrieval results should provide sufficient metadata to identify:

- What was retrieved
- Where it originated
- Which version was retrieved
- When it was created or modified
- Which agent or source produced it
- Which relationships connect it to other memories

---

# Cross-Agent Memory

MindCache supports multiple memory scopes.

## Private Memory

Memory available only to its owner or authorized agent.

## Shared Memory

Memory explicitly shared between authorized agents.

## Team Memory

Memory available to a defined group of agents or users.

## Organizational Memory

Memory governed by organizational policies and permissions.

Memory scopes must support independent access policies.

---

# Conflict Management

Multi-agent systems may modify the same memory concurrently.

Implementations should support:

- Concurrent version detection
- Revision identification
- Conflict detection
- Conflict preservation
- Conflict resolution
- Merge operations
- Version comparison
- Audit history

Implementations should avoid silently overwriting concurrent memory changes.

---

# Memory Integrity

MindCache implementations should provide mechanisms for verifying memory integrity.

Capabilities may include:

- Checksums
- Content hashes
- Version identifiers
- Digital signatures
- Provenance records
- Snapshot validation
- Archive integrity verification

---

# Interoperability

MindCache implementations should expose standardized memory concepts independently of their internal implementation.

An implementation should be able to exchange:

- Memory
- Snippets
- Stories
- Synapses
- Metadata
- Versions
- Provenance
- Permissions
- Archive information

The specification does not require implementations to use the same database, programming language, AI model, framework, or infrastructure.

---

# Example Use Cases

MindCache may be implemented for:

- Personal AI assistants
- Enterprise AI systems
- Multi-agent orchestration
- Autonomous research agents
- Robotics
- Healthcare assistants
- Customer support systems
- Legal research
- Financial analysis
- Knowledge management
- Scientific collaboration
- Educational platforms
- Long-running autonomous systems
- Agent development platforms

---

# Benefits

MindCache provides a common foundation for:

- Persistent long-term agent intelligence
- Reduced context window dependency
- Granular information retrieval
- Historical context preservation
- Cross-agent knowledge sharing
- Explainable memory relationships
- On-demand archive retrieval
- Reusable knowledge
- Reduced redundant inference
- Lower memory retrieval overhead
- Vendor independence
- Framework independence
- Model independence
- Storage independence
- Modular implementation
- Multi-agent interoperability

---

# Conformance

A MindCache implementation conforms to the specification when it implements the required core memory concepts and interfaces defined by the specification.

Conformance may be evaluated by capability areas including:

- Persistent memory
- Snippet retrieval
- Story reconstruction
- Synapse relationships
- Version management
- Archival
- Retrieval
- Memory lifecycle management
- Multi-agent access
- Metadata and provenance
- Security and privacy controls

Optional plugins may extend an implementation without being required for core conformance.

---

# Extension Model

MindCache extensions should:

- Preserve the core memory model
- Use defined module interfaces
- Avoid requiring proprietary infrastructure
- Maintain interoperability where practical
- Clearly identify optional dependencies
- Preserve memory provenance
- Preserve version information
- Respect configured access controls
- Respect retention and deletion policies

Plugins must not silently alter core memory semantics.

---

# Implementation Independence

The specification does not prescribe:

- A programming language
- A database
- A vector database
- An embedding model
- An AI model
- An agent framework
- A cloud provider
- A deployment model
- A specific API technology

Implementations may select technologies appropriate to their requirements while adhering to the MindCache specification.

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
  - [https://roxanneardary.com/mindcache/](https://roxanneardary.com/mindcache/)

---

## License & Notice Requirements

MindCache is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- MindCache specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
