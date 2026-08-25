# Taskivo
**Better conversations. Better outcomes.**
- HTML Mirror: [https://roxanneardary.com/taskivo-specification/](https://roxanneardary.com/taskivo-specification/)  

---

## Purpose

Taskivo is an open source AI platform designed to transform real-world requests into structured tasks, standardized service scopes, guided conversations, comparable quotes, and actionable outcomes.

Taskivo operates as a modular system. The core modules provide the foundational capabilities required by the platform, while optional plugin modules extend functionality without requiring changes to the core system.

Taskivo is designed around human-in-the-loop operation. The AI acts as a co-pilot that helps users communicate, gather information, clarify requirements, compare results, and make informed decisions while keeping the user in control of consequential actions.

---

## Design Principles

- Modular architecture
- Human-in-the-loop operation
- User authorization and control
- Structured task definition
- Standardized service scopes
- Comparable outcomes
- Provider-neutral operation
- Extensible AI capabilities
- Interoperable data
- Transparent data provenance
- Privacy-conscious operation
- Local-first deployment support
- Open source extensibility
- Provider-independent integrations
- Versioned interfaces
- Schema-driven data handling

---

## Core Modules

### Task Intelligence Module

The Task Intelligence Module shall interpret natural language requests and convert them into structured tasks.

Features shall include:

- Natural language task interpretation
- Task intent recognition
- Task category identification
- Task decomposition
- Task expansion
- Identification of commonly purchased goods and services
- Product and service discovery
- Core service identification
- Optional service identification
- Seasonal service identification
- Conditional service identification
- One-time versus recurring service identification
- Task prioritization
- Task dependency identification
- Task refinement
- User clarification prompts
- Context-aware task expansion
- Multi-service task support
- Multi-provider task support
- Task templates
- Task duplication
- Task editing
- Task history
- Task status tracking
- Task completion tracking
- Task scheduling
- Recurring task support
- Related task management

### Service Intelligence Module

The Service Intelligence Module shall provide structured knowledge about goods and services relevant to a task.

Features shall include:

- Service taxonomies
- Product taxonomies
- Frequently purchased service libraries
- Frequently purchased goods libraries
- Service relationships
- Product relationships
- Service dependencies
- Service bundles
- Common add-ons
- Seasonal services
- Specialty services
- Service terminology
- Product terminology
- Common customer requirements
- Common provider requirements
- Common pricing models
- Common exclusions
- Common additional fees
- Regional variations
- Seasonal variations
- Service-specific knowledge

### Scope Engine Module

The Scope Engine Module shall convert task requirements into a structured scope that can be presented consistently to service providers.

Features shall include:

- Structured service scope generation
- Standardized scope definitions
- Core service requirements
- Optional service requirements
- Conditional requirements
- Product requirements
- Quantity requirements
- Size requirements
- Property requirements
- Equipment requirements
- Usage requirements
- Frequency definitions
- Duration definitions
- Service-specific requirements
- Customer-specific requirements
- Provider-specific conditions
- Inclusion tracking
- Exclusion tracking
- Scope validation
- Scope comparison
- Scope history
- Scope versioning
- Scope reuse
- Scope templates
- Scope-to-quote alignment

### Question Intelligence Module

The Question Intelligence Module shall determine what information needs to be gathered to properly define and evaluate a task.

Features shall include:

- Dynamic question generation
- Required question identification
- Optional question identification
- Conditional questions
- Question prioritization
- Industry-specific questions
- Service-specific questions
- Follow-up questions
- Clarification questions
- Missing-information detection
- Contradiction detection
- Pricing clarification questions
- Availability questions
- Scope confirmation questions
- Provider response verification questions
- Progressive questioning
- User-editable questions

### Communication Skills Module

The Communication Skills Module shall provide pre-programmed communication behaviors that enable Taskivo to assist users during real-world conversations.

Features shall include:

- Professional communication
- Friendly communication
- Active listening assistance
- Clarification techniques
- Question sequencing
- Conversation state tracking
- Context retention
- Interruption handling
- Follow-up management
- Objection handling assistance
- Price clarification
- Availability clarification
- Scope confirmation
- Provider response confirmation
- Closing assistance
- Conversation summarization
- Communication tone controls
- User-defined communication preferences

### Taskivo Pilot Module

Taskivo Pilot shall provide the real-time AI co-pilot experience.

Features shall include:

- Real-time conversation assistance
- Live transcription
- Conversation context awareness
- Suggested responses
- Suggested questions
- Suggested follow-up questions
- Clarification recommendations
- Missing-information alerts
- Pricing clarification prompts
- Service inclusion verification
- Hidden-fee detection
- Contradiction detection
- Real-time information extraction
- Conversation summaries
- User-controlled AI responses
- Push-to-speak AI assistance
- User override controls
- Immediate call termination controls
- User approval before AI speech
- Manual correction
- User-controlled conversation flow

### Communication Orchestration Module

The Communication Orchestration Module shall manage interactions between Taskivo and external parties.

Features shall include:

- User-authorized outbound calling
- Call preparation
- Call scripts
- Dynamic call scripts
- Business contact management
- Call scheduling
- Business-hours awareness
- Call attempt tracking
- Call status tracking
- Call notes
- Call history
- Call outcome recording
- Follow-up scheduling
- Multiple provider calls
- Multi-provider comparison
- Call session management
- Transfer handling
- Escalation handling
- Voice communication support
- Text communication support
- Hybrid communication support

### Quote Collection Module

The Quote Collection Module shall gather structured pricing and service information from providers.

Features shall include:

- Quote request generation
- Structured quote requests
- Provider-specific quote tracking
- Price collection
- Labor price collection
- Material price collection
- Flat-rate pricing
- Hourly pricing
- Per-visit pricing
- Monthly pricing
- Recurring pricing
- Package pricing
- Minimum service charges
- Trip charges
- Diagnostic fees
- Additional fees
- Taxes and applicable charges
- Discounts
- Promotions
- Deposits
- Payment terms
- Warranty information
- Cancellation terms
- Scheduling requirements

### Data Normalization Module

The Data Normalization Module shall convert unstructured provider responses into standardized information.

Features shall include:

- Structured quote extraction
- Automatic price extraction
- Service inclusion extraction
- Service exclusion extraction
- Fee extraction
- Condition extraction
- Frequency normalization
- Unit normalization
- Quantity normalization
- Duration normalization
- Recurring-cost normalization
- One-time-cost normalization
- Quote completeness checking
- Missing-information detection
- Quote consistency checking
- Provider response comparison
- Apples-to-apples quote comparison

### Provider Comparison Module

The Provider Comparison Module shall compare providers using the same task scope and evaluation criteria.

Features shall include:

- Multi-provider comparison
- Standardized comparison criteria
- Price comparison
- Scope comparison
- Included-service comparison
- Excluded-service comparison
- Fee comparison
- Availability comparison
- Warranty comparison
- Payment-term comparison
- Contract-term comparison
- Value analysis
- Difference highlighting
- Missing-service alerts
- Quote confidence indicators
- User-defined comparison priorities

### Outcome Module

The Outcome Module shall convert gathered information into structured, actionable results.

Features shall include:

- Structured task outcomes
- Quote summaries
- Provider summaries
- Comparison reports
- Cost summaries
- Recurring-cost projections
- One-time versus recurring cost analysis
- Scope differences
- Important conditions
- Follow-up requirements
- Outstanding questions
- User-defined decision criteria
- User-confirmed outcomes
- Task completion status

### Agreement Module

The Agreement Module shall provide optional structured agreement preparation based on an accepted scope and quote.

Features shall include:

- Accepted quote capture
- Final scope generation
- Scope confirmation
- Agreement-ready structured data
- Pricing terms
- Payment terms
- Service frequency
- Service inclusions
- Service exclusions
- Conditions and requirements
- Provider information
- Customer requirements
- Agreement versioning
- Agreement history
- User approval before acceptance

The Agreement Module shall not assume that a generated agreement is legally binding. Execution and legal validity shall depend on applicable law, user actions, provider acceptance, and any required signature or authorization process.

### Data Management Module

The Data Management Module shall manage Taskivo's structured task, service, provider, quote, conversation, scope, and outcome data.

Features shall include:

- Structured data storage
- Provider records
- Service records
- Product records
- Quote records
- Conversation records
- Task records
- Scope records
- Agreement records
- Historical pricing data
- Historical service data
- Data provenance
- Data timestamps
- Source tracking
- User corrections
- Data versioning
- Import capabilities
- Export capabilities
- Data deletion
- Data retention controls

### Provenance and Transparency Module

The Provenance and Transparency Module shall maintain the origin and history of information processed by Taskivo.

Features shall include:

- Source tracking
- Conversation provenance
- Quote provenance
- Timestamp tracking
- Provider attribution
- User corrections
- AI-generated data identification
- User-entered data identification
- Confidence indicators
- Change history
- Scope history
- Quote history
- Agreement history
- Audit trails

### Human Control Module

The Human Control Module shall ensure that users retain control over consequential Taskivo operations.

Features shall include:

- User authorization for calls
- User authorization for communications
- User-controlled communication
- User review before AI speech
- User override
- User correction
- User approval of scopes
- User approval of quotes
- User approval of agreements
- Manual data editing
- Manual provider selection
- Manual task completion
- Call termination controls
- Transparent AI assistance

### Privacy and Security Module

The Privacy and Security Module shall provide controls for protecting user, provider, conversation, and task information.

Features shall include:

- Local-first deployment support
- User-controlled data storage
- Data minimization
- Access controls
- Permission management
- Encryption support
- Secure credential handling
- Conversation-data controls
- Data retention controls
- Data deletion
- Exportable user data
- Audit logging
- Provider-data protection
- Configurable privacy policies

### Integration Module

The Integration Module shall provide provider-independent interfaces for external services and infrastructure.

Features shall include:

- Telephony integrations
- Voice provider integrations
- Speech-to-text integrations
- Text-to-speech integrations
- AI model integrations
- Calendar integrations
- Email integrations
- Messaging integrations
- CRM integrations
- Business directory integrations
- Payment integrations
- Document-generation integrations
- External API integrations
- Webhook support
- Provider abstraction
- AI-provider abstraction
- Database-provider abstraction

### Analytics Module

The Analytics Module shall provide measurement and analysis of Taskivo activity and outcomes.

Features shall include:

- Task completion analytics
- Quote collection analytics
- Provider response rates
- Call success rates
- Conversation analytics
- Pricing trends
- Service pricing history
- Module performance
- Module usage
- Quote completeness
- Data-quality metrics
- User correction rates
- Task efficiency metrics
- Outcome metrics

---

## Optional Plugin Modules

Taskivo shall support optional plugin modules that extend functionality without requiring the corresponding capability to be part of the core system.

### Industry Service Modules

Optional industry modules may provide specialized intelligence for categories including:

- Lawn care
- Landscaping
- Tree services
- House cleaning
- Plumbing
- HVAC
- Electrical services
- Roofing
- Pest control
- Auto repair
- Auto maintenance
- Mobile detailing
- Home improvement
- Appliance repair
- Moving services
- Pool services
- Pressure washing
- Carpet cleaning
- Locksmith services
- Professional services
- Personal services
- Healthcare-related administrative services
- Dental-related administrative services
- Optometry-related administrative services
- Other service categories

Each industry module may define:

- Service taxonomy
- Product taxonomy
- Common purchases
- Common services
- Service bundles
- Required information
- Optional information
- Question sets
- Conversation flows
- Pricing models
- Normalization rules
- Output schemas
- Industry-specific validation rules

### Voice Provider Plugins

Optional voice plugins may provide:

- Outbound calling
- Inbound calling
- Call routing
- Audio streaming
- Voice transcription
- Text-to-speech
- Call recording where legally permitted
- Call metadata
- Call status information

### AI Model Plugins

Optional AI model plugins may provide:

- Language models
- Reasoning models
- Speech recognition
- Speech synthesis
- Embedding models
- Classification models
- Extraction models
- Local AI models
- Remote AI services

### Business Discovery Plugins

Optional business discovery plugins may provide:

- Business search
- Business directories
- Business contact information
- Service categories
- Business hours
- Location information
- Provider discovery
- Provider filtering

### Scheduling Plugins

Optional scheduling plugins may provide:

- Calendar synchronization
- Appointment scheduling
- Availability tracking
- Reminder generation
- Follow-up scheduling
- Recurring appointment management

### Messaging Plugins

Optional messaging plugins may provide:

- SMS
- Email
- Messaging platforms
- Automated follow-ups
- Provider notifications
- User notifications

### Payment Plugins

Optional payment plugins may provide:

- Payment processing
- Recurring payments
- Deposits
- Payment authorization
- Escrow functionality
- Payment status tracking

### Document Plugins

Optional document plugins may provide:

- Quote documents
- Service summaries
- Agreements
- Reports
- Invoices
- Receipts
- Export formats
- Digital signature integrations

### Marketplace Plugins

Optional marketplace functionality may provide:

- Module discovery
- Module installation
- Module publishing
- Module ratings
- Module reviews
- Publisher profiles
- Module usage statistics
- Module verification
- Module moderation
- Module reporting

### Developer Tools Plugins

Optional developer plugins may provide:

- Module creation assistants
- Module testing tools
- Schema validators
- Documentation generators
- Development environments
- Module packaging
- Compatibility testing
- Module publishing tools

### Advanced Negotiation Plugins

Optional negotiation modules may provide:

- Negotiation assistance
- Counteroffer suggestions
- Price comparison
- Value comparison
- Negotiation question generation
- Concession tracking
- User-defined negotiation limits

Negotiation capabilities shall remain subject to user authorization and control.

### Booking and Purchasing Plugins

Optional booking and purchasing modules may provide:

- Service booking
- Product purchasing
- Appointment confirmation
- Order creation
- Purchase authorization
- Vendor confirmation
- Transaction tracking

Any purchase or booking action that creates a financial or contractual obligation shall require explicit user authorization unless the user has configured an applicable authorization policy.

## Module Standards

All Taskivo modules shall use standardized interfaces and schemas.

Modules should define:

- Module name
- Module version
- Module description
- Module category
- Dependencies
- Required capabilities
- Input schema
- Scope schema
- Question definitions
- Conversation definitions
- Normalization rules
- Output schema
- Validation rules
- Compatibility requirements
- Configuration options

Modules shall not be permitted to silently bypass core security, privacy, authorization, validation, or human-control requirements.

## Module Versioning

Taskivo modules shall support semantic versioning.

Module versions shall identify:

- Major changes that may break compatibility
- Minor changes that add backward-compatible functionality
- Patch changes that provide backward-compatible fixes

Taskivo shall support:

- Version selection
- Version locking
- Compatibility checking
- Dependency management
- Update notifications
- Change histories
- Rollback support where practical

## Module Validation

Taskivo shall validate modules before activation or publication.

Validation may include:

- Schema validation
- Interface validation
- Dependency validation
- Compatibility validation
- Security validation
- Permission validation
- Output validation
- Question validation
- Scope validation
- Documentation validation
- Test execution

## Module Marketplace

The optional Taskivo Marketplace shall provide a distribution mechanism for third-party modules.

Marketplace capabilities may include:

- Module discovery
- Search
- Categories
- Publisher information
- Module documentation
- Version information
- Compatibility information
- Ratings
- Reviews
- Usage information
- Community modules
- Verified modules
- Module reporting
- Module moderation

Modules may be classified as:

- Community
- Verified
- Publisher
- Private

## AI-Assisted Module Creation

Taskivo may provide tools that allow developers and users to describe a service category in natural language and generate a proposed module definition.

Generated modules may include:

- Service taxonomies
- Product taxonomies
- Scope schemas
- Questions
- Conversation flows
- Normalization rules
- Output schemas
- Validation rules
- Documentation

Generated modules shall remain subject to validation and human review before being treated as trusted or verified modules.

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
  - [https://roxanneardary.com/taskivo/](https://roxanneardary.com/taskivo/)

---

## License & Notice Requirements

Taskivo is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+).**   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- Taskivo specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
