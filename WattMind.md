# WattMind

**The mesh intelligence of energy.**

WattMind is an open-source distributed energy exchange platform that coordinates decentralized energy production, storage, and consumption through a modular, intelligent marketplace. Designed for homes, businesses, utilities, cooperatives, and AI infrastructure, WattMind provides a flexible foundation for building modern distributed energy ecosystems while remaining vendor-neutral and extensible.

---

# Specification

## Purpose

WattMind defines a modular architecture for building distributed energy exchanges capable of coordinating energy generation, storage, demand, and market settlement across decentralized infrastructure.

The specification separates physical energy infrastructure from market coordination, allowing organizations to deploy only the components they require while maintaining interoperability across the ecosystem.

---

## Design Principles

- Modular, service-oriented architecture
- Distributed-first design
- Vendor-neutral hardware integration
- Real-time market coordination
- Grid-aware intelligence
- Event-driven communication
- API-first development
- Local-first deployment
- Horizontal scalability
- Fault-tolerant services
- Open standards
- Extensible plugin architecture

---

# Core Modules

## Edge Device Management

Provides communication between WattMind and physical energy infrastructure.

### Features

- Solar inverter integration
- Battery management integration
- EV charger integration
- Smart meter support
- Generator support
- Smart appliance integration
- Device discovery
- Device registration
- Remote device management
- Local edge agents
- Secure telemetry collection
- Device health monitoring
- Firmware compatibility abstraction

---

## Energy Measurement & Verification

Creates trusted measurements used throughout the platform.

### Features

- Interval energy measurements
- Time-series aggregation
- Production verification
- Consumption verification
- Meter normalization
- Device calibration support
- Timestamp validation
- Telemetry validation
- Confidence scoring
- Data integrity verification
- Historical measurements
- Audit-ready measurement records

---

## Distributed Energy Exchange

The marketplace responsible for matching energy supply and demand.

### Features

- Energy marketplace
- Buy and sell orders
- Real-time matching
- Continuous market clearing
- Time-window contracts
- Supply aggregation
- Demand aggregation
- Market depth calculations
- Flexible order types
- Geographic market segmentation
- Market statistics
- Exchange APIs

---

## Pricing Engine

Determines market pricing.

### Features

- Dynamic pricing
- Spot pricing
- Time-of-use pricing
- Local market pricing
- Clearing price calculation
- Supply-demand balancing
- Price forecasting interfaces
- Historical pricing
- Market analytics
- Pricing APIs

---

## Settlement Engine

Handles financial reconciliation between market participants.

### Features

- Trade settlement
- Net settlement
- Credit accounting
- Debit accounting
- Settlement ledger
- Transaction history
- Settlement reconciliation
- Adjustment processing
- Settlement reporting
- Settlement APIs

---

## Grid Intelligence

Coordinates distributed energy resources while respecting grid constraints.

### Features

- Demand forecasting
- Renewable forecasting
- Battery forecasting
- Grid balancing
- Congestion detection
- Capacity modeling
- Constraint modeling
- Dispatch optimization
- Local balancing
- Regional balancing
- System optimization

---

## Identity & Trust

Provides participant identity and trust management.

### Features

- Participant registration
- Organization management
- Device identity
- Digital credentials
- Access control
- Authentication
- Authorization
- Reputation scoring
- Trust scoring
- Security policies

---

## API Gateway

Provides standardized access to the platform.

### Features

- REST APIs
- Event APIs
- Streaming interfaces
- Webhooks
- Authentication
- API versioning
- Rate limiting
- SDK support
- Documentation endpoints

---

## Administration

System management and operational tooling.

### Features

- Configuration management
- Service monitoring
- Audit logs
- Health monitoring
- Diagnostics
- Backup management
- Recovery tools
- System metrics
- Operational dashboards

---

# Optional Plugin Modules

## AI Compute Exchange

Allows AI data centers and compute clusters to participate as dynamic energy consumers.

### Features

- Compute demand scheduling
- AI workload coordination
- Flexible compute contracts
- Energy-aware job scheduling
- Compute demand forecasting

---

## Virtual Power Plant (VPP)

Aggregates distributed assets into coordinated power resources.

### Features

- DER aggregation
- Fleet management
- Capacity pooling
- Virtual dispatch
- Resource orchestration

---

## Microgrid Management

Supports localized independent energy systems.

### Features

- Island mode support
- Local balancing
- Community microgrids
- Campus microgrids
- Industrial microgrids

---

## Battery Optimization

Advanced battery intelligence.

### Features

- Charge optimization
- Discharge optimization
- Battery arbitrage
- Lifecycle optimization
- Storage forecasting

---

## Electric Vehicle Management

Extends support for EV ecosystems.

### Features

- Smart charging
- Fleet charging
- Vehicle-to-grid (V2G)
- Vehicle-to-home (V2H)
- Charging optimization

---

## Renewable Forecasting

Enhanced renewable intelligence.

### Features

- Solar forecasting
- Wind forecasting
- Weather integration
- Irradiance modeling
- Renewable production analytics

---

## Utility Integration

Connects WattMind with existing utility infrastructure.

### Features

- Utility APIs
- ISO/RTO integration
- SCADA integration
- Grid operator interfaces
- Regulatory reporting

---

## Carbon Intelligence

Environmental reporting and optimization.

### Features

- Carbon intensity tracking
- Renewable attribution
- Emissions reporting
- Sustainability dashboards
- Carbon analytics

---

## Marketplace Extensions

Additional market capabilities.

### Features

- Forward contracts
- Capacity markets
- Ancillary services
- Flexibility markets
- Renewable energy certificates
- Energy credit markets

---

## Financial Services

Advanced financial functionality.

### Features

- Billing
- Invoicing
- Escrow support
- Revenue distribution
- Cooperative dividend management
- Financial reporting

---

## Analytics

Business intelligence and reporting.

### Features

- Operational dashboards
- Market analytics
- Participant analytics
- Forecast analytics
- Historical reporting
- Export tools

---

## Notifications

Communication services.

### Features

- Email notifications
- SMS notifications
- Push notifications
- Market alerts
- Dispatch alerts
- System alerts

---

## Mapping & GIS

Geospatial intelligence.

### Features

- Interactive maps
- Asset visualization
- Service territories
- Network topology
- Geographic analytics

---

## Developer Tools

Platform extension toolkit.

### Features

- SDKs
- Plugin framework
- Testing tools
- Simulation tools
- Mock services
- API explorer

---

# Modular Deployment

Organizations can deploy only the modules they require.

Example deployments include:

- Residential energy exchange
- Community energy cooperative
- Municipal energy marketplace
- Utility-scale distributed exchange
- AI data center energy marketplace
- Industrial energy optimization platform
- Campus microgrid
- Regional distributed energy network

---

# Target Users

- Homeowners
- Energy cooperatives
- Utilities
- Independent power producers
- Municipal governments
- Commercial property owners
- Industrial facilities
- AI data centers
- Renewable energy developers
- Research institutions

---

# Vision

WattMind creates the intelligence layer that enables distributed energy systems to operate as coordinated markets rather than isolated infrastructure. Through a modular architecture, organizations can build interoperable energy exchanges that improve efficiency, resilience, transparency, and participation while supporting the next generation of decentralized energy networks.

**WattMind — The mesh intelligence of energy.**

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
  - [https://roxanneardary.com/wattmind/](https://roxanneardary.com/wattmind/)  

---

## License & Notice Requirements

WattMind is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
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
