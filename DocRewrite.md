# DocRewrite 
**Rewrite Documents with Rules and AI**

---

## Overview

DocRewrite is an open-source AI-powered document and content transformation platform for finding specific phrases, patterns, concepts, or semantic matches and rewriting them according to user-defined rules and instructions.

DocRewrite combines traditional search, pattern matching, semantic analysis, AI-assisted rewriting, document processing, website processing, review workflows, automation, and version control into a modular system.

The platform is designed to work locally, through self-hosted deployments, or as an integrated service. Users can process individual documents, collections of files, websites, documentation repositories, and other supported content sources while maintaining control over their data and AI infrastructure.

DocRewrite is designed around a modular architecture. Core modules provide the fundamental document transformation capabilities, while optional plugins extend the platform with additional file formats, integrations, AI providers, specialized workflows, industry-specific capabilities, and external services.

---

## Core Design Principles

### Open Source

DocRewrite is developed as open-source software under the AGPL-3.0+ license.

### Modular Architecture

Capabilities are separated into independent modules so that users can enable only the functionality they need and contributors can develop new capabilities without modifying the entire platform.

### Local-First Processing

DocRewrite is designed to support local processing and locally hosted AI models for users who need greater control over documents and content.

### AI Provider Independence

The platform should not depend on a single AI provider. AI capabilities can be connected to local models, self-hosted inference servers, or compatible external providers.

### Human-in-the-Loop

AI-generated changes should remain reviewable. Users can inspect, approve, reject, modify, or roll back proposed changes.

### Preservation of Source Content

Document structure, formatting, metadata, links, tables, headings, and other supported content should be preserved whenever possible.

### Automation Without Losing Control

DocRewrite supports automation while providing configurable approval requirements, previews, audit trails, and rollback capabilities.

### Extensibility

New formats, AI providers, rewrite strategies, integrations, workflows, and analysis systems can be added through the plugin architecture.

---

# Core Modules

## 1. Document Ingestion Module

The Document Ingestion Module provides a unified interface for importing content into DocRewrite.

### Capabilities

- Document upload
- File validation
- MIME-type detection
- Encoding detection
- Content extraction
- Document normalization
- Metadata extraction
- Batch document ingestion
- Directory ingestion
- Drag-and-drop ingestion
- Document preprocessing
- Source identification
- Content provenance tracking
- Duplicate detection
- Document fingerprinting

### Supported Core Formats

- Microsoft Word (.docx)
- PDF
- Markdown (.md)
- Plain text (.txt)
- HTML
- Structured text formats

Additional formats can be provided through plugins.

---

## 2. Content Parsing Module

The Content Parsing Module converts source documents into structured content while preserving relationships between content elements.

### Capabilities

- Paragraph extraction
- Heading detection
- List extraction
- Table extraction
- Link extraction
- Metadata extraction
- Footnote handling
- Section detection
- Text block identification
- Content hierarchy detection
- Formatting preservation
- Document structure mapping

The parser creates an internal representation that allows the rewriting engine to modify text without unnecessarily destroying the original document structure.

---

## 3. Search & Detection Module

The Search & Detection Module identifies content that matches user-defined criteria.

### Exact Search

- Exact phrase matching
- Case-sensitive matching
- Case-insensitive matching
- Whole-word matching
- Phrase occurrence counting

### Pattern Search

- Regular expressions
- Wildcards
- Pattern matching
- Structural patterns
- Custom detection rules

### Fuzzy Search

- Typographical variations
- Spelling variations
- Minor wording differences
- Approximate phrase matching

### Semantic Search

- Meaning-based matching
- Concept detection
- Similar phrase detection
- Intent-based matching
- Context-aware matching
- Embedding-based retrieval

### AI Detection

Users can instruct DocRewrite to identify concepts such as:

- Outdated language
- Passive voice
- Excessive complexity
- Redundant statements
- Inconsistent terminology
- Unclear language
- Negative tone
- Missing context
- Repetitive content
- Brand-inconsistent language

---

## 4. Rewrite Rules Module

The Rewrite Rules Module defines what DocRewrite should change and how it should change it.

### Rule Types

- Exact replacement rules
- Pattern replacement rules
- Regex rules
- Semantic rules
- AI instruction rules
- Style rules
- Formatting rules
- Terminology rules
- Conditional rules
- Multi-step rules

### Rule Components

A rule can define:

- Name
- Description
- Search criteria
- Matching method
- Rewrite instructions
- Preservation requirements
- Protected terminology
- Excluded content
- Priority
- Confidence threshold
- Approval requirements
- Execution order

### Custom Rules

Users can create custom rules for specific projects, organizations, websites, brands, documentation systems, or workflows.

Rules can be stored and reused across documents.

---

## 5. AI Rewrite Engine

The AI Rewrite Engine performs instruction-based content transformation.

### Core Capabilities

- Sentence rewriting
- Paragraph rewriting
- Section rewriting
- Document rewriting
- Context-aware rewriting
- Meaning preservation
- Terminology preservation
- Tone transformation
- Style transformation
- Readability improvement
- Clarity improvement
- Conciseness improvement
- Grammar correction
- Spelling correction
- Redundancy reduction
- Active voice conversion
- Language simplification
- Content expansion
- Content summarization

### AI Instructions

Users can provide natural-language instructions describing exactly how content should be rewritten.

Examples include:

- Rewrite this in plain English.
- Make this more concise.
- Convert passive voice to active voice.
- Preserve all technical terminology.
- Rewrite this in a professional tone.
- Make the language easier to understand.
- Replace outdated terminology.
- Maintain the original meaning.
- Rewrite headings while preserving their purpose.

---

## 6. Context Management Module

The Context Management Module ensures that rewriting decisions remain consistent with surrounding content.

### Capabilities

- Sentence context
- Paragraph context
- Section context
- Document context
- Cross-document context
- Terminology consistency
- Named entity preservation
- Protected phrase handling
- Cross-page context
- Project-wide style context

Users can define terms, phrases, names, concepts, or facts that must not be changed.

---

## 7. Style & Voice Module

The Style & Voice Module manages consistent writing characteristics.

### Capabilities

- Brand voice
- Professional tone
- Academic tone
- Technical tone
- Conversational tone
- Marketing tone
- Formal tone
- Plain-language style
- Reading-level targeting
- Sentence-length preferences
- Vocabulary preferences
- Terminology standards
- Style consistency scoring

### Style Profiles

Users can create reusable style profiles and apply them to:

- Documents
- Folders
- Websites
- Projects
- Documentation repositories
- Organizations

---

## 8. Content Analysis Module

The Content Analysis Module evaluates source and rewritten content.

### Analysis Capabilities

- Readability analysis
- Complexity analysis
- Tone analysis
- Sentiment analysis
- Grammar analysis
- Spelling analysis
- Terminology consistency
- Sentence-length analysis
- Word-frequency analysis
- Redundancy detection
- Content quality scoring
- Structural analysis

### Comparative Analysis

DocRewrite can compare the original and rewritten versions and report changes in:

- Word count
- Sentence count
- Readability
- Complexity
- Tone
- Terminology
- Structure
- Detected issues

---

## 9. Review & Diff Module

The Review & Diff Module provides human oversight of AI-generated changes.

### Capabilities

- Side-by-side comparison
- Inline comparison
- Added-text highlighting
- Removed-text highlighting
- Modified-text highlighting
- Per-change approval
- Per-change rejection
- Batch approval
- Batch rejection
- Manual editing
- Rewrite regeneration
- Change explanations
- Confidence indicators

Users can review individual changes before they become part of the final document.

---

## 10. Document Reconstruction Module

The Document Reconstruction Module converts rewritten content back into its original or requested format.

### Capabilities

- Formatting preservation
- Heading preservation
- Table preservation
- List preservation
- Link preservation
- Metadata preservation
- Document structure preservation
- Export validation
- File integrity checks

The system should preserve unsupported content whenever possible rather than silently discarding it.

---

## 11. Version Control Module

The Version Control Module maintains document transformation history.

### Capabilities

- Original version preservation
- Rewritten version preservation
- Revision history
- Change tracking
- Version comparison
- Rollback
- Restore
- Revision labels
- Rewrite-session history

Each rewrite session can record:

- Source document
- Rules applied
- AI model used
- Configuration
- Timestamp
- User
- Approved changes
- Rejected changes
- Final output

---

## 12. Website Processing Module

The Website Processing Module allows DocRewrite to operate on web content.

### Capabilities

- URL ingestion
- Sitemap discovery
- Website crawling
- Page extraction
- Internal-link discovery
- Page selection
- Domain restrictions
- Crawl depth controls
- Rate limiting
- Robots.txt awareness
- HTML structure preservation
- Metadata extraction
- Page-by-page rewriting
- Website-wide rewrite rules

### Website Rewrite Workflow

1. Enter a website URL.
2. Discover available pages.
3. Select pages or content categories.
4. Identify matching content.
5. Apply rewrite rules.
6. Generate proposed changes.
7. Review changes.
8. Approve or reject changes.
9. Export rewritten content.

DocRewrite should provide controls to prevent accidental rewriting of navigation, scripts, structured data, forms, or other protected elements.

---

## 13. Batch Processing Module

The Batch Processing Module enables large-scale content transformation.

### Capabilities

- Multiple file processing
- Folder processing
- Website-wide processing
- Project-wide processing
- Rule-based batch rewriting
- Parallel processing
- Processing queues
- Job status tracking
- Retry handling
- Failure reporting
- Batch export

---

## 14. Workflow Pipeline Module

The Workflow Pipeline Module allows users to create multi-step transformations.

Example workflow:

1. Detect outdated terminology
2. Replace approved terminology
3. Simplify complex sentences
4. Convert passive voice
5. Apply brand voice
6. Check terminology consistency
7. Run quality analysis
8. Generate review package

### Pipeline Capabilities

- Sequential rules
- Conditional rules
- Branching workflows
- Approval checkpoints
- Automated validation
- Failure handling
- Retry policies
- Pipeline templates
- Reusable workflows

---

## 15. Rule Library Module

The Rule Library Module provides reusable rewrite rules and workflow templates.

### Capabilities

- Personal rule libraries
- Project rule libraries
- Organization rule libraries
- Import/export
- Rule versioning
- Rule validation
- Rule dependencies
- Rule categories
- Rule documentation

---

## 16. User Interface Module

The User Interface Module provides the primary web application.

### Capabilities

- Dashboard
- Document manager
- Website manager
- Rule manager
- Rewrite workspace
- Diff viewer
- Workflow builder
- Project management
- Version history
- Analytics dashboard
- Settings
- Model configuration

### Editing Interface

- Inline suggestions
- Side-by-side comparison
- Accept/reject controls
- Manual editing
- Regenerate rewrite
- Compare alternatives
- Explain change
- Lock content
- Protect terminology

---

## 17. Collaboration Module

The Collaboration Module supports teams working on shared documents and rules.

### Capabilities

- Shared projects
- Shared documents
- Shared rules
- User activity
- Change attribution
- Review assignments
- Approval workflows
- Comments
- Review status
- Collaborative editing
- Permission controls

---

## 18. Authentication & Authorization Module

The Authentication & Authorization Module manages access to self-hosted installations.

### Capabilities

- User accounts
- Authentication
- Session management
- Role-based access
- Project permissions
- Document permissions
- Rule permissions
- Administrative permissions
- API authentication

---

## 19. Audit & Governance Module

The Audit & Governance Module provides traceability for automated and AI-assisted changes.

### Capabilities

- Audit logs
- Rewrite history
- User activity tracking
- Rule execution history
- Model tracking
- Approval records
- Rejection records
- Export history
- Configuration history

The audit system should make it possible to determine how a particular change was produced.

---

## 20. Security Module

The Security Module provides safeguards for documents, credentials, AI services, and integrations.

### Capabilities

- Secure file handling
- Input validation
- Output validation
- Encryption support
- Secret management
- Access controls
- Session security
- API security
- Upload restrictions
- Sandboxed processing
- Local-only processing
- Secure deletion options

---

## 21. Local AI Module

The Local AI Module allows users to connect DocRewrite to locally hosted models.

### Capabilities

- Local LLM support
- Local embedding models
- Local inference servers
- Configurable model selection
- Model-specific settings
- Offline operation
- No-external-data mode

DocRewrite should be designed so users are not forced to send documents to external AI providers.

---

## 22. AI Provider Module

The AI Provider Module provides an abstraction layer between DocRewrite and AI systems.

### Capabilities

- Model registration
- Provider selection
- Model routing
- Fallback models
- Token management
- Context-window management
- Temperature controls
- Prompt templates
- Embedding providers
- Provider-specific configuration

This abstraction allows users to change AI providers without redesigning the application.

---

## 23. Prompt Management Module

The Prompt Management Module manages AI instructions and templates.

### Capabilities

- Prompt templates
- Prompt variables
- System instructions
- Rewrite instructions
- Context injection
- Prompt versioning
- Prompt testing
- Prompt validation
- Prompt libraries

Dynamic variables can include values such as:

- Brand name
- Product name
- Audience
- Reading level
- Required terminology
- Preferred tone
- Industry
- Language

---

## 24. Semantic Search Module

The Semantic Search Module provides meaning-based content discovery.

### Capabilities

- Embedding generation
- Vector search
- Similarity search
- Semantic phrase matching
- Concept matching
- Context retrieval
- Document retrieval
- Cross-document search

The module should support pluggable vector databases and embedding providers.

---

## 25. Analytics Module

The Analytics Module measures rewriting activity and outcomes.

### Capabilities

- Documents processed
- Pages processed
- Rules executed
- Changes proposed
- Changes accepted
- Changes rejected
- Words rewritten
- Processing time
- Model usage
- Error rates
- Readability changes
- Style changes
- Tone changes

Analytics should be configurable so privacy-sensitive deployments can disable collection.

---

## 26. API Module

The API Module exposes DocRewrite functionality to external applications.

### Capabilities

- Document upload
- Search
- Rule execution
- Rewrite requests
- Workflow execution
- Job status
- Version retrieval
- Export
- Analytics
- Project management

The API should support authentication, permissions, rate limiting, and configurable access policies.

---

## 27. CLI Module

The Command-Line Module provides automation for developers and system administrators.

### Capabilities

- File processing
- Directory processing
- Search
- Rule execution
- Rewrite pipelines
- Website processing
- Batch jobs
- Export
- Validation
- Dry-run mode
- Configuration management

The CLI should support Unix-style pipelines and scripting.

---

## 28. SDK Module

The SDK Module provides programmatic access to DocRewrite.

### Planned SDKs

- Python
- JavaScript / TypeScript

SDK functionality should mirror the public API where practical.

---

## 29. Automation Module

The Automation Module connects DocRewrite to external events and scheduled tasks.

### Capabilities

- Scheduled jobs
- Cron-compatible jobs
- Webhooks
- Event triggers
- File-system triggers
- Git triggers
- CMS triggers
- API triggers
- Automated rewrite pipelines

---

## 30. Integration Module

The Integration Module provides standardized connections to external systems.

Potential integrations include:

- Git repositories
- GitLab
- GitHub
- WordPress
- Joomla
- Notion
- Confluence
- MediaWiki
- Documentation systems
- Content management systems
- Communication platforms
- Storage systems

Specific integrations can be implemented as plugins.

---

# Optional Plugin Modules

DocRewrite's plugin system allows additional functionality to be installed without making every deployment depend on every integration or capability.

## Plugin Architecture

Plugins can provide:

- File format support
- AI providers
- Embedding providers
- Vector databases
- CMS integrations
- Cloud storage integrations
- Rewrite rules
- Industry-specific workflows
- Analytics providers
- Authentication providers
- Export formats
- Notification services
- Specialized analysis engines

Plugins should expose defined interfaces and avoid modifying the core system directly whenever possible.

---

## Optional Document Format Plugins

Potential plugins include:

- Microsoft PowerPoint (.pptx)
- Microsoft Excel (.xlsx)
- OpenDocument Text (.odt)
- OpenDocument Spreadsheet (.ods)
- OpenDocument Presentation (.odp)
- EPUB
- RTF
- CSV
- XML
- JSON
- LaTeX
- Additional structured document formats

---

## Optional AI Provider Plugins

Potential plugins include connectors for:

- Local LLM servers
- Open-source model runtimes
- External AI APIs
- Enterprise AI platforms
- Specialized language models
- Domain-specific models

Users should be able to install AI provider plugins without changing the DocRewrite core.

---

## Optional Vector Database Plugins

Potential plugins include:

- Qdrant
- Chroma
- Weaviate
- Milvus
- Other compatible vector stores

---

## Optional CMS Plugins

Potential plugins include:

- WordPress
- Joomla
- Drupal
- Ghost
- Notion
- Confluence
- MediaWiki
- Other content management systems

---

## Optional Git Plugins

Potential capabilities include:

- Git repository scanning
- GitLab integration
- GitHub integration
- Commit generation
- Branch creation
- Merge request generation
- Pull request generation
- Documentation rewrite automation
- CI/CD integration

---

## Optional SEO Plugin

The SEO Plugin can provide:

- SEO content analysis
- Heading analysis
- Meta description rewriting
- Title rewriting
- Internal-link analysis
- Anchor-text improvement
- Keyword consistency
- Search-intent analysis
- Content structure analysis

---

## Optional Accessibility Plugin

The Accessibility Plugin can provide:

- Accessibility language analysis
- Plain-language transformation
- Heading hierarchy analysis
- Alternative text analysis
- Screen-reader optimization
- Link-text analysis
- Accessibility-oriented content recommendations

---

## Optional Translation Plugin

The Translation Plugin can provide:

- Translation
- Translation-aware rewriting
- Multi-language workflows
- Terminology preservation
- Brand voice preservation
- Translation comparison
- Language detection

---

## Optional Compliance Plugin

The Compliance Plugin can provide configurable analysis for organizational requirements and applicable regulatory frameworks.

Potential capabilities include:

- Sensitive-information detection
- Privacy-oriented content checks
- Accessibility checks
- Policy language checks
- Required disclosure detection
- Compliance terminology checks
- Compliance reporting

Compliance plugins should provide configurable rules rather than claiming that AI-generated output automatically guarantees legal or regulatory compliance.

---

## Optional Academic & Research Plugin

Potential capabilities include:

- Citation analysis
- Reference checking
- Academic style analysis
- Research terminology consistency
- Literature-document processing
- Research dataset generation
- Experimental rewrite evaluation

---

## Optional Legal Language Plugin

Potential capabilities include:

- Legal terminology consistency
- Plain-language transformation
- Defined-term detection
- Clause consistency analysis
- Cross-document terminology checking
- Contract language comparison

The plugin should assist with document analysis and rewriting without representing AI output as legal advice.

---

## Optional Marketing Plugin

Potential capabilities include:

- Marketing tone transformation
- Campaign-specific style profiles
- Audience-specific rewriting
- Call-to-action analysis
- Headline alternatives
- Landing-page optimization
- Product-description rewriting

---

## Optional Communication Plugin

Potential capabilities include:

- Email rewriting
- Announcement rewriting
- Internal communication rewriting
- Social media rewriting
- Message tone adjustment
- Audience-specific versions

---

## Optional Plagiarism & Similarity Plugin

Potential capabilities include:

- Similarity analysis
- Duplicate-content detection
- Internal document comparison
- Phrase overlap detection
- Content originality analysis

External plagiarism services should remain optional integrations.

---

## Optional Text-to-Speech Plugin

Potential capabilities include:

- Text-to-speech optimization
- Narration preparation
- Pronunciation metadata
- Spoken-language rewriting
- Audio generation through compatible providers

---

## Optional Fine-Tuning & Learning Plugin

The optional Learning Plugin can support:

- User-provided examples
- Preferred rewrite examples
- Style datasets
- Evaluation datasets
- Fine-tuning workflows
- Preference modeling
- Custom embedding generation

Learning features should provide explicit controls over what content is retained and used.

---

## Optional Adaptive Learning Plugin

The Adaptive Learning Plugin can analyze user decisions such as:

- Accepted rewrites
- Rejected rewrites
- Manually edited rewrites
- Preferred alternatives
- Frequently protected terminology

The system can use this information to improve future suggestions while allowing users to disable or reset adaptive behavior.

---

## Optional Collaboration Plugin

Advanced collaboration functionality can be provided as a plugin where deployments need it.

Potential capabilities include:

- Real-time collaborative editing
- Shared review sessions
- Comments
- Assignments
- Team workspaces
- Approval workflows
- Collaborative rule development

---

## Optional Notification Plugin

Potential notification integrations include:

- Email
- Slack
- Microsoft Teams
- Webhooks
- In-app notifications
- System notifications

---

## Optional Enterprise Deployment Plugin

Potential enterprise functionality includes:

- Advanced identity providers
- Single sign-on
- LDAP
- Enterprise directory integration
- Advanced audit controls
- Multi-tenant management
- Organization-level policies
- Advanced administrative controls

---

# Plugin Management

The plugin system should support:

- Plugin discovery
- Plugin installation
- Plugin removal
- Plugin activation
- Plugin deactivation
- Plugin configuration
- Plugin versioning
- Dependency management
- Compatibility checks
- Permission declarations
- Plugin security metadata

Plugins should clearly identify what data they access and which external services they communicate with.

---

# Protected Content System

DocRewrite should allow users to identify content that must never be rewritten.

### Protected Content

- Names
- Product names
- Company names
- Legal terms
- Technical terms
- URLs
- Email addresses
- Code
- Identifiers
- Variables
- Shortcodes
- HTML elements
- Metadata
- Structured data
- User-defined phrases

Protected content should be respected throughout all rewrite workflows.

---

# AI Safety & Quality Controls

DocRewrite should provide safeguards against unintended AI changes.

### Controls

- Meaning-preservation checks
- Protected terminology
- Required terminology
- Maximum change thresholds
- Confidence thresholds
- Human approval requirements
- Source-versus-output comparison
- Automated validation
- Rollback
- Audit logging
- Dry-run mode

AI-generated text should always be treated as a proposed transformation unless the user explicitly enables automated publishing.

---

# Content Preservation

Where supported, DocRewrite should preserve:

- Formatting
- Headings
- Lists
- Tables
- Links
- Images
- Captions
- Metadata
- Document structure
- HTML structure
- Code blocks
- Embedded elements

Content that cannot safely be preserved should be reported to the user rather than silently discarded.

---

# Privacy

DocRewrite is designed to support privacy-conscious deployments.

### Privacy Features

- Local processing
- Self-hosted deployment
- Local AI models
- Configurable retention
- Document deletion
- Audit controls
- External-provider opt-out
- Configurable telemetry
- Data-processing policies

Deployments should allow administrators to determine whether document content, prompts, outputs, logs, and analytics are retained.

---

# Deployment

DocRewrite should support multiple deployment models.

### Local Desktop Environment

Designed for users who want to process documents entirely on their own machine.

### Self-Hosted Server

Designed for individuals, teams, organizations, and institutions operating their own DocRewrite instance.

### Containerized Deployment

Docker-based deployments can provide consistent environments for development and production.

### Orchestrated Deployment

Larger installations can optionally use container orchestration systems such as Kubernetes.

---

# Technology Architecture

DocRewrite is designed around a modular service architecture.

### Backend

- Python
- FastAPI
- Pydantic
- Async processing
- Modular service interfaces

### Natural Language Processing

- spaCy
- Sentence Transformers
- Configurable NLP libraries

### AI Orchestration

- Provider abstraction layer
- Configurable model routing
- Prompt management
- Local model support
- External provider plugins

### Document Processing

- python-docx
- PDF processing libraries
- Markdown processing
- HTML parsing

### Search

- Exact search
- Regex
- Fuzzy matching
- Semantic search
- Vector retrieval

### Vector Storage

The core system should provide an abstraction layer that allows different vector databases to be connected.

Qdrant can be used as one supported implementation.

### Frontend

- Next.js
- React
- Tailwind CSS

### Background Processing

- Redis
- Celery or compatible task-processing architecture

### Deployment

- Docker
- Docker Compose
- Optional Kubernetes deployment

---

# Development Architecture

The project should maintain clear separation between:

- Interface layer
- API layer
- Authentication
- Document ingestion
- Parsing
- Search
- Rules
- AI rewriting
- Context management
- Analysis
- Review
- Reconstruction
- Versioning
- Workflow processing
- Storage
- Plugins
- Integrations

Core services should communicate through defined interfaces rather than tightly coupling implementation details.

---

# Example Rewrite Workflow

A typical workflow can be:

1. Import a document or website.
2. Parse and normalize the content.
3. Select a rewrite rule.
4. Search for matching content.
5. Retrieve relevant context.
6. Generate proposed rewrites.
7. Validate protected terminology.
8. Analyze the proposed changes.
9. Display the differences.
10. Allow the user to approve, reject, or modify changes.
11. Reconstruct the document.
12. Save a new version.
13. Generate an audit record.
14. Export or publish the result.

---

# Example Rule Concepts

DocRewrite can support rules such as:

### Terminology Replacement

Find outdated terminology and replace it with approved terminology while preserving sentence structure.

### Plain Language

Find unnecessarily complex language and rewrite it for a specified reading level.

### Active Voice

Identify passive constructions and rewrite them using active voice without changing meaning.

### Brand Voice

Rewrite selected content to match a defined organizational style profile.

### SEO Content

Identify specified content patterns and rewrite them according to configured SEO requirements.

### Accessibility

Identify unnecessarily complex or ambiguous language and propose clearer alternatives.

### Consistency

Find inconsistent terminology across a collection of documents and standardize it.

---

# CLI & Automation

DocRewrite should provide a command-line interface for automation and scripting.

Supported operations should include:

- Search
- Analyze
- Rewrite
- Validate
- Preview
- Export
- Batch processing
- Website processing
- Workflow execution
- Rule management

A dry-run mode should allow users to see proposed changes without modifying source files.

---

# API

The API should expose modular DocRewrite functionality to external applications.

Potential API operations include:

- Create project
- Upload document
- Search document
- Create rule
- Execute rule
- Create workflow
- Run rewrite
- Retrieve results
- Review changes
- Approve changes
- Reject changes
- Export document
- Retrieve versions
- Retrieve audit history

---

# Testing

DocRewrite should maintain comprehensive automated testing.

### Test Categories

- Unit tests
- Integration tests
- Document parsing tests
- Reconstruction tests
- Search tests
- Rule tests
- AI workflow tests
- API tests
- Plugin tests
- Security tests
- Regression tests
- End-to-end tests

Document fixtures should be used to verify that rewriting does not unnecessarily damage document structure or formatting.

---

# Documentation

Documentation should cover:

- Installation
- Configuration
- Architecture
- Core modules
- Plugin development
- Rule development
- AI provider development
- API usage
- CLI usage
- Deployment
- Security
- Privacy
- Contribution guidelines

---

# Roadmap

Development can be organized around modular milestones.

## Phase 1 — Core Engine

- Document ingestion
- Parsing
- Exact search
- Regex search
- Rewrite rules
- AI rewrite engine
- Document reconstruction
- Basic CLI

## Phase 2 — Review & Web Interface

- Web application
- Upload interface
- Rewrite workspace
- Diff viewer
- Approval workflow
- Version history

## Phase 3 — Semantic Intelligence

- Embeddings
- Semantic search
- Context management
- Style profiles
- Content analysis

## Phase 4 — Website Processing

- URL ingestion
- Sitemap processing
- Website crawling
- HTML rewriting
- Website-wide rules

## Phase 5 — Automation

- Batch processing
- Workflow pipelines
- Scheduling
- Webhooks
- API
- SDK

## Phase 6 — Plugin Ecosystem

- Plugin architecture
- Plugin manager
- AI provider plugins
- Document format plugins
- CMS plugins
- Git plugins
- Specialized analysis plugins

## Phase 7 — Collaboration

- User accounts
- Projects
- Permissions
- Shared rules
- Review workflows
- Collaboration

## Phase 8 — Advanced Intelligence

- Adaptive learning
- Style transfer
- Cross-document context
- Domain-specific modules
- Advanced quality analysis

---

# Contributing

Contributions are welcome.

Developers can contribute:

- Core modules
- Plugins
- Rewrite rules
- AI provider integrations
- Document format support
- Tests
- Documentation
- User interface improvements
- Security improvements
- Performance improvements

New functionality should preferably be implemented as a module or plugin when it does not belong in the core system.

See `CONTRIBUTING.md` for contribution requirements and development guidelines.

---

# Project

**DocRewrite — Rewrite documents with rules and AI.**

DocRewrite is designed to become an extensible open-source platform for intelligent document transformation, combining deterministic rules with AI while keeping users in control of their content and workflows.

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
  - [https://roxanneardary.com/docrewrite/](https://roxanneardary.com/docrewrite/)

---

## License & Notice Requirements

DocRewrite is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- DocRewrite specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
