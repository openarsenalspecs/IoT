# VeritasVote

**Open. Auditable. Verifiable.**

VeritasVote is an open-source, end-to-end election platform for secure in-person voting. It provides a modular architecture for both hardware and software, enabling election jurisdictions, researchers, and manufacturers to build transparent, auditable, and verifiable voting systems using standardized components. Every vote is backed by a voter-verifiable paper ballot, cryptographic integrity protections, and reproducible open-source software.

Unlike proprietary voting systems, VeritasVote is designed around public trust through transparency. Every hardware design, software component, security protocol, and manufacturing specification is openly available for inspection, verification, and improvement by the community.

---

# Objectives

- Open hardware and software
- Air-gapped operation
- Voter-verifiable paper ballots
- Cryptographically verifiable elections
- Transparent audit processes
- Reproducible software builds
- Modular architecture
- Long-term maintainability
- Accessibility for every voter
- Vendor-neutral deployment

---

# System Architecture

VeritasVote separates the platform into independently maintainable modules.

```
Election Management
        │
Ballot Definition
        │
Polling Station
        │
Voting Terminal
        │
Paper Ballot
        │
Encrypted Cast Vote Record
        │
Tabulation
        │
Auditing
        │
Election Certification
```

---

# Hardware Architecture

Hardware is divided into interchangeable modules.

## Core Hardware Modules

### Compute Module

Responsible for:

- Secure boot
- Election application execution
- Hardware monitoring
- Local storage management
- Cryptographic operations

---

### Touchscreen Module

Provides:

- Ballot presentation
- Accessibility controls
- Multiple language support
- Touch input
- Visual verification

---

### Ballot Printer Module

Responsible for:

- Human-readable ballots
- QR code generation
- Spoiled ballot printing
- Ballot serial generation
- Paper verification

---

### Ballot Box Interface

Provides:

- Ballot insertion detection
- Ballot acceptance confirmation
- Secure ballot storage
- Ballot accounting

---

### Secure Storage Module

Stores:

- Election configuration
- Cryptographic keys
- Encrypted cast vote records
- Audit logs
- Event logs

---

### Power Management Module

Provides:

- Battery backup
- Graceful shutdown
- Power monitoring
- Low-power alerts

---

### Tamper Detection Module

Responsible for:

- Enclosure monitoring
- Seal validation
- Intrusion detection
- Hardware event logging

---

### Accessibility Hardware Module

Supports:

- Audio ballots
- Headphones
- Sip-and-puff devices
- Accessible buttons
- Alternative navigation devices

---

# Optional Hardware Plugin Modules

## Smart Card Reader

- Poll worker authentication
- Election official credentials

---

## Biometric Poll Worker Authentication

- Fingerprint authentication
- Multi-factor authorization

---

## Receipt Scanner

- Ballot verification
- Poll worker validation

---

## UPS Expansion Module

- Extended battery runtime
- Automatic power monitoring

---

## Environmental Monitoring

- Temperature sensors
- Humidity sensors
- Hardware health monitoring

---

## Diagnostic Display

- Service information
- Maintenance mode
- Hardware diagnostics

---

# Software Architecture

Each software component is independently versioned.

## Core Software Modules

### Election Management Engine

Responsible for:

- Election configuration
- Poll management
- Precinct configuration
- Election lifecycle

---

### Ballot Definition Engine

Provides:

- Ballot templates
- Candidate configuration
- Referendum management
- Language support

---

### Voting Application

Responsible for:

- Ballot rendering
- Voter interaction
- Vote validation
- Ballot review
- Ballot confirmation

---

### Accessibility Engine

Supports:

- Screen reader
- Adjustable text
- High contrast
- Audio guidance
- Keyboard navigation
- Multiple languages

---

### Cryptography Engine

Provides:

- Vote encryption
- Digital signatures
- Hash verification
- Threshold cryptography
- Key management

---

### Secure Boot Manager

Responsible for:

- Image verification
- Firmware validation
- Integrity measurements
- Boot verification

---

### Audit Engine

Generates:

- Audit logs
- Chain-of-custody records
- Event history
- Verification reports

---

### Cast Vote Record Manager

Responsible for:

- Encrypted vote storage
- Ballot indexing
- Record integrity
- Export packages

---

### Tabulation Engine

Provides:

- Vote counting
- Result aggregation
- Public reporting
- Export formats

---

### Risk-Limiting Audit Engine

Supports:

- Random sampling
- Statistical verification
- Manual recount support
- Audit reporting

---

### Device Management

Responsible for:

- Hardware discovery
- Health monitoring
- Diagnostics
- Configuration management

---

### Logging Framework

Records:

- Security events
- System events
- Administrative actions
- Election events

---

# Optional Software Plugin Modules

## Electronic Poll Book Integration

- Voter lookup
- Check-in workflows
- Poll synchronization

---

## Election Results Portal

- Public result publishing
- Live reporting
- Downloadable reports

---

## Observer Dashboard

Provides:

- Election monitoring
- Audit status
- Device health
- Chain-of-custody tracking

---

## Geographic Reporting

- Precinct maps
- District reporting
- Geographic analytics

---

## Translation Packs

- Community language packs
- Regional terminology
- Accessibility localization

---

## Advanced Accessibility Plugins

- Eye tracking
- Switch devices
- Voice navigation

---

## Hardware Manufacturer Drivers

Supports:

- Alternative printers
- Display controllers
- Secure storage devices
- Scanner hardware

---

## Cryptographic Provider Plugins

Supports:

- Multiple audited cryptographic implementations
- National cryptographic standards
- Future cryptographic algorithms

---

## Reporting Plugins

Generate:

- PDF reports
- CSV exports
- Election summaries
- Audit packages

---

## Research Sandbox

Provides:

- Experimental algorithms
- Prototype interfaces
- Academic research support

---

# Security Features

- Air-gapped architecture
- Secure boot
- Immutable operating system
- Read-only root filesystem
- Memory-safe application code
- Cryptographically signed software
- Threshold cryptography
- Tamper-evident hardware
- Hardware intrusion detection
- Dual-record voting
- Voter-verifiable paper ballots
- Public cryptographic verification
- Reproducible builds
- Risk-limiting audits
- Comprehensive event logging

---

# Technology Stack

## Hardware

- ARM-based secure compute platform
- Capacitive touchscreen
- Thermal ballot printer
- Tamper detection sensors
- Secure storage
- Battery backup
- Accessibility peripherals

## Software

- Rust
- Immutable Linux (Yocto or Buildroot)
- SQLite
- OpenSSL or RustCrypto
- QR Code libraries
- PDF generation
- Secure boot chain
- Reproducible build pipeline

---

# Development Goals

- Publicly auditable codebase
- Independent security reviews
- Reproducible releases
- Long-term hardware compatibility
- Open manufacturing specifications
- Cross-jurisdiction deployment
- Community-driven development
- Transparent governance  

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
  - [https://roxanneardary.com/veritasvote/](https://roxanneardary.com/veritasvote/)

---

## License & Notice Requirements

VeritasVote is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- VeritasVote specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
