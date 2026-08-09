# LotusGraph

**Rust-core power. Python simplicity.**

## Overview

LotusGraph is an open-source hybrid graph database designed to combine Property Graph and RDF capabilities within a unified, modular architecture. A high-performance Rust core provides the foundation for storage, transactions, query execution, graph processing, and concurrency, while a Python API provides an accessible development experience.

LotusGraph is designed for applications ranging from knowledge graphs and AI systems to real-time analytics, distributed data processing, scientific research, enterprise applications, and edge computing. Its modular architecture allows the core database to remain focused and efficient while optional plugins extend LotusGraph with specialized capabilities.

## Design Philosophy

LotusGraph is built around several principles:

- **Hybrid by design**: Property Graph and RDF data models work within one platform.
- **Rust-powered**: Performance-critical database operations run through the Rust core.
- **Python-friendly**: Developers can interact with LotusGraph through an expressive Python API.
- **Modular architecture**: Core database capabilities are separated into independent modules.
- **Extensible by plugins**: Specialized functionality can be installed without bloating the core system.
- **Local-first capable**: LotusGraph can support embedded and edge deployments as well as larger distributed environments.
- **AI-ready**: Graph, semantic, vector, and analytical capabilities can work together as a foundation for intelligent applications.
- **Open source**: The platform is designed to remain transparent, extensible, and community-driven.

# Architecture

LotusGraph uses a layered modular architecture.

## Rust Core

The Rust core provides the high-performance foundation of LotusGraph. It is responsible for performance-sensitive operations including storage, indexing, transactions, query execution, graph traversal, concurrency, and memory management.

The Python layer provides developer-facing access to these capabilities without requiring developers to work directly with the underlying Rust implementation.

## Python API

The Python API provides an intuitive interface for creating, querying, updating, analyzing, and managing graphs.

The API is designed to support:

- Graph creation and management
- Node and edge operations
- Property management
- Graph traversal
- Query execution
- Transactions
- Analytics
- Vector operations
- Administrative operations
- Plugin management

# Core Modules

LotusGraph's core functionality is organized into modules. Core modules provide the foundational capabilities required by the database itself.

## Core Graph Module

Provides the fundamental graph data model.

Features include:

- Nodes
- Edges
- Labels
- Properties
- Relationships
- Directed and undirected graph support
- Multiple graph namespaces
- Graph metadata
- Graph traversal primitives
- Subgraph operations

## Hybrid Data Model Module

Provides unified support for Property Graph and RDF data.

Features include:

- Property Graph storage
- RDF triple storage
- Subject, predicate, and object relationships
- Shared identifiers
- Hybrid graph representation
- Semantic relationships
- Graph-to-triple interoperability
- Property-to-RDF mappings

## Storage Module

Provides persistent and in-memory graph storage.

Features include:

- In-memory storage
- Persistent disk storage
- Storage abstraction layers
- Efficient serialization
- Compression
- Storage statistics
- Data integrity checks
- Configurable storage policies
- Memory-efficient graph representation

## Transaction Module

Provides transactional database operations.

Features include:

- ACID transactions
- Transaction isolation
- Commit and rollback
- Atomic graph updates
- Concurrent transactions
- Transaction recovery
- Write-ahead logging
- Consistency validation

## Indexing Module

Provides indexes for fast graph access.

Features include:

- Node indexes
- Edge indexes
- Property indexes
- Label indexes
- Relationship indexes
- Composite indexes
- Full-text indexes
- Configurable indexing strategies
- Index maintenance

## Query Module

Provides LotusGraph's query infrastructure.

Features include:

- Query parsing
- Query planning
- Query optimization
- Query execution
- Parameterized queries
- Query caching
- Explain plans
- Query statistics
- Hybrid query planning

The query architecture is designed to support a Cypher-compatible query language and SPARQL capabilities without requiring separate database engines.

## Traversal Module

Provides high-performance graph traversal.

Features include:

- Breadth-first traversal
- Depth-first traversal
- Multi-hop traversal
- Shortest-path traversal
- Weighted paths
- Relationship filtering
- Property filtering
- Traversal limits
- Subgraph extraction
- Parallel traversal

## RDF and Semantic Module

Provides semantic graph functionality.

Features include:

- RDF triples
- RDF schemas
- SPARQL support
- Namespaces
- Ontologies
- Semantic relationships
- Inference foundations
- RDF import and export
- Turtle support
- RDF/XML support

## Graph Analytics Module

Provides built-in graph algorithms and analytical operations.

Features include:

- PageRank
- Degree centrality
- Betweenness centrality
- Closeness centrality
- Community detection
- Connected components
- Shortest paths
- Graph density
- Similarity analysis
- Network analysis
- Parallel graph algorithms

## Vector Module

Provides native vector-aware graph functionality.

Features include:

- Vector storage
- Node embeddings
- Edge embeddings
- Similarity search
- Vector indexes
- Hybrid graph and vector queries
- Embedding metadata
- Configurable distance metrics
- Vector filtering

## Temporal Graph Module

Provides time-aware graph capabilities.

Features include:

- Temporal nodes
- Temporal edges
- Validity intervals
- Event timestamps
- Historical graph states
- Time-based traversal
- Temporal queries
- Graph history
- Change tracking

## Versioning Module

Provides graph state management.

Features include:

- Graph snapshots
- Version history
- Graph diffs
- State restoration
- Change tracking
- Historical queries
- Snapshot management

## Streaming Module

Provides real-time graph ingestion and updates.

Features include:

- Event-based graph updates
- Streaming ingestion
- Batch ingestion
- Event processing
- Change streams
- Graph update notifications
- Stream monitoring

## Import and Export Module

Provides interoperability with common graph and data formats.

Supported formats can include:

- CSV
- JSON
- GraphML
- RDF/XML
- Turtle
- N-Triples
- N-Quads
- Property Graph formats

The import and export architecture is extensible so additional formats can be introduced without modifying the database core.

## Security Module

Provides foundational security capabilities.

Features include:

- Authentication
- Authorization
- Role-based access control
- Fine-grained permissions
- Secure connections
- Encryption support
- Access policies
- Security auditing

## Provenance Module

Provides data lineage and provenance tracking.

Features include:

- Data origin tracking
- Change provenance
- Source attribution
- Transformation history
- Query provenance
- Import provenance
- Graph lineage

## Backup and Recovery Module

Provides database resilience capabilities.

Features include:

- Database backups
- Incremental backups
- Snapshot restoration
- Recovery procedures
- Transaction recovery
- Backup verification
- Disaster recovery support

## API Module

Provides application access to LotusGraph.

Interfaces can include:

- Python API
- Rust API
- REST API
- gRPC API
- CLI access

The API architecture is designed so additional interfaces can be introduced without changing the underlying graph engine.

## CLI Module

Provides command-line administration and exploration.

Features include:

- Database creation
- Database management
- Query execution
- Import and export
- Backup management
- Graph inspection
- Configuration management
- Plugin management
- Performance diagnostics

# Optional Plugin Modules

Optional plugins extend LotusGraph beyond its foundational database capabilities. Plugins are independently developed modules that can be installed when their functionality is required.

Plugins should communicate with LotusGraph through defined extension interfaces rather than modifying the core engine.

## AI Plugin

Provides AI-assisted graph capabilities.

Potential features include:

- Natural language graph queries
- LLM-assisted query generation
- AI graph summaries
- AI-assisted graph exploration
- Semantic recommendations
- AI-assisted data enrichment
- AI reasoning workflows

## Graph Neural Network Plugin

Provides GNN integration.

Potential features include:

- Graph neural network training
- Graph embeddings
- Node classification
- Edge prediction
- Graph classification
- Link prediction
- GNN inference
- Model integration

## Predictive Analytics Plugin

Provides predictive graph analysis.

Potential features include:

- Predictive edge creation
- Relationship forecasting
- Trend detection
- Graph evolution forecasting
- Predictive node analysis
- What-if graph simulations

## Anomaly Detection Plugin

Provides graph-based anomaly detection.

Potential features include:

- Structural anomaly detection
- Relationship anomaly detection
- Behavioral anomaly detection
- Temporal anomaly detection
- AI-assisted anomaly scoring
- Anomaly alerts

## Recommendation Plugin

Provides graph-based recommendation functionality.

Potential features include:

- Similar-node recommendations
- Relationship recommendations
- Personalized graph traversal
- Collaborative graph analysis
- Semantic recommendations
- Recommendation explanations

## Federation Plugin

Provides federated graph capabilities.

Potential features include:

- Cross-database queries
- Cross-instance graph traversal
- Federated SPARQL
- Remote graph sources
- Graph synchronization
- Distributed query execution

## Distributed Graph Plugin

Provides advanced distributed deployment capabilities.

Potential features include:

- Graph sharding
- Distributed storage
- Distributed query execution
- Cluster management
- Replication
- Failover
- Distributed transactions
- Cluster monitoring

## GPU Plugin

Provides optional GPU acceleration.

Potential features include:

- GPU vector operations
- GPU graph analytics
- Parallel graph algorithms
- Embedding acceleration
- AI workload acceleration

## Streaming Connector Plugins

Provides integrations with external streaming platforms.

Potential integrations include:

- Kafka
- RabbitMQ
- MQTT
- Event streaming systems
- Webhooks
- Custom event sources

## Database Connector Plugins

Provides interoperability with external databases and graph systems.

Potential connectors include:

- Neo4j
- ArangoDB
- RDF databases
- SQL databases
- Document databases
- Vector databases
- Data warehouses

## Visualization Plugin

Provides interactive graph visualization.

Potential features include:

- Interactive graph exploration
- Dynamic graph layouts
- Force-directed layouts
- Hierarchical layouts
- Cluster visualization
- Subgraph exploration
- Graph filtering
- Graph dashboards
- SVG export
- PNG export
- Web-based visualization

## Notebook Plugin

Provides enhanced notebook integration.

Potential integrations include:

- Jupyter
- JupyterLab
- Interactive graph visualization
- Query notebooks
- Graph analytics notebooks
- AI-assisted exploration

## Collaboration Plugin

Provides collaborative graph workflows.

Potential features include:

- Shared graph workspaces
- Graph annotations
- Node and edge comments
- Shared subgraphs
- Collaborative editing
- Role-specific graph views
- Change review

## Privacy Plugin

Provides advanced privacy capabilities.

Potential features include:

- Differential privacy
- Privacy-aware graph queries
- Data masking
- Sensitive-property controls
- Privacy-preserving analytics
- Federated privacy controls

## Compliance Plugin

Provides configurable governance and compliance tooling.

Potential features include:

- Policy enforcement
- Compliance reporting
- Retention policies
- Data governance
- Audit reporting
- Configurable regulatory controls

## Edge and IoT Plugin

Provides lightweight deployment capabilities.

Potential features include:

- Embedded graph databases
- Low-memory operation
- Offline operation
- Edge synchronization
- Intermittent connectivity support
- Local graph analytics
- Edge AI integration

## Serverless Functions Plugin

Provides event-driven graph functions.

Potential features include:

- Python functions
- Rust functions
- Graph event triggers
- Scheduled graph functions
- Serverless execution
- Webhook execution

## Advanced Visualization Plugin

Provides specialized graph exploration environments.

Potential features include:

- 3D graph visualization
- Large-scale graph rendering
- Advanced clustering
- AI-assisted graph highlighting
- Graph storytelling
- Interactive analytical dashboards

# Plugin Architecture

LotusGraph plugins should follow a consistent extension model.

Plugins should:

- Have clearly defined interfaces
- Be independently installable
- Declare their dependencies
- Avoid unnecessary modifications to core modules
- Provide their own documentation
- Provide tests
- Follow LotusGraph security requirements
- Respect the project's licensing requirements

The plugin system is intended to allow LotusGraph to evolve without turning the core database into a monolithic system.

# Performance and Scalability

LotusGraph is designed to support multiple deployment models.

These include:

- Embedded databases
- Local development
- Desktop applications
- Server deployments
- Cloud deployments
- Distributed clusters
- Edge devices
- AI infrastructure

Performance-sensitive operations are implemented through the Rust core, while Python provides a productive interface for application development and orchestration.

# AI Architecture

AI functionality is intentionally separated from the database foundation.

The core provides the graph, semantic, vector, temporal, and analytical primitives required by AI systems. Optional AI plugins can build higher-level capabilities on top of those primitives.

This separation allows LotusGraph to support AI applications without requiring every deployment to install AI-specific dependencies.

# Extensibility

LotusGraph is designed as a platform rather than a monolithic database.

Core modules provide stable foundational capabilities. Optional plugins provide specialized functionality. This approach allows users to build installations that contain only the capabilities they require while giving the broader ecosystem a mechanism for extending LotusGraph.

Potential future extensions can include:

- New query languages
- New storage engines
- New graph algorithms
- New AI frameworks
- New data formats
- New connectors
- New visualization systems
- New deployment targets

# Development

LotusGraph uses Rust for its performance-critical database engine and Python for its primary developer-facing API.

Development should maintain a clear boundary between:

- Rust engine implementation
- Python API
- Core database modules
- Optional plugins
- External integrations
- Developer tooling
- Documentation

New foundational database capabilities should generally become core modules. Specialized or independently deployable functionality should generally be implemented as plugins.

# Contributing

Contributions are welcome.

Before contributing:

1. Review the project documentation.
2. Review the existing module architecture.
3. Determine whether the proposed functionality belongs in a core module or optional plugin.
4. Open an issue for substantial architectural changes.
5. Add appropriate tests and documentation.
6. Submit a Merge Request.

See `CONTRIBUTING.md` for contribution requirements.

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
  - [https://roxanneardary.com/lotusgraph/](https://roxanneardary.com/lotusgraph/)

---

## License & Notice Requirements

LotusGraph is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- LotusGraph specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.  
