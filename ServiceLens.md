# ServiceLens
**Every service, in one view.**
- HTML Mirror:  [https://roxanneardary.com/servicelens-specification/](https://roxanneardary.com/servicelens-specification/)

---

ServiceLens is an open-source local services platform that enables independent contractors, service providers, and small businesses to create a single provider profile and become discoverable across relevant searches. The platform combines a structured service directory, natural-language search, secure transactions, invoicing, receipts, tax reporting, trust tools, and data portability into a modular system that can be self-hosted and extended.

## Purpose

ServiceLens is designed to improve how people discover and hire local service providers while giving providers greater control over their information, business relationships, transactions, and data.

Providers should be able to enter their information once and have that information used throughout the platform. A single provider profile can support multiple services, search terms, related tasks, locations, availability settings, transactions, invoices, receipts, reports, and optional integrations.

Clients should be able to describe what they need in natural language and discover relevant local providers without needing to understand a specific category structure or exact keyword.

The platform prioritizes transparency, accessibility, privacy, portability, security, and community-oriented deployment.

## Design Principles

- Open-source and self-hostable
- Modular architecture
- Local service discovery
- Provider-controlled profiles and business information
- Natural-language interaction
- Transparent search and ranking logic
- Privacy-conscious data handling
- Secure financial workflows
- Accessible and mobile-friendly interfaces
- Data portability
- Extensible through optional plugins
- No mandatory vendor lock-in
- Community and organization deployment support

---

# Core Modules

## Provider Directory

The Provider Directory manages the central directory of independent contractors, service providers, and small businesses.

Providers must be able to create and maintain a single profile containing relevant business and service information.

Provider profiles may include:

- Individual or business name
- Provider type
- Business description
- Service descriptions
- Skills and specialties
- Service categories
- Service areas
- Geographic service radius
- Availability
- Contact preferences
- Pricing information
- Portfolio media
- Certifications
- Licenses
- Insurance information
- Optional verification status

Providers must be able to update their information from a central profile interface.

Updates to provider information should automatically propagate throughout relevant areas of the platform.

Providers must be able to export their profile data in portable formats.

## Service Intelligence

The Service Intelligence module converts provider information into structured and searchable service data.

The module should analyze provider service descriptions and associate them with:

- Relevant keywords
- Synonyms
- Related services
- Skills
- Common customer requests
- Problem descriptions
- Service categories
- Task types
- Seasonal relevance where applicable

Providers should not be required to manually create duplicate listings for every possible search phrase.

A provider who describes a service once should be discoverable through multiple relevant searches.

Service intelligence must support human review and provider correction of generated associations.

## Natural-Language Search

The Natural-Language Search module allows users to search for services using ordinary language.

Users should be able to enter requests such as:

- Someone who can repair drywall this weekend
- A local plumber for a leaking sink
- An electrician for a small home project
- Someone to mow my lawn every week

The search system should identify relevant intent, including:

- Requested service
- Task or problem
- Location
- Distance
- Urgency
- Availability
- Price preferences
- Required certifications
- Provider qualifications

Search should combine semantic matching, structured search, keyword matching, and geographic filtering.

The platform must provide a fallback search method when semantic or AI-assisted services are unavailable.

## Search Ranking

Search results must use transparent and auditable ranking logic.

Ranking factors may include:

- Relevance to the request
- Service match
- Geographic proximity
- Service area
- Availability
- Verification status
- Verified customer reviews
- Provider responsiveness
- User-selected filters

The platform must not require providers to purchase higher search placement.

Search ranking rules should be documented and available for review.

## Geographic Discovery

The Geographic Discovery module supports local service discovery.

Users should be able to search based on:

- Current location
- Address
- Postal code
- City
- Region
- Selected service area
- Custom distance

Providers must be able to define the geographic areas in which they offer services.

The platform should support map-based browsing and location-aware search results.

Location information must be handled with privacy controls appropriate to the sensitivity of the data.

## Provider Availability and Scheduling

The Availability and Scheduling module allows providers to manage when they are available for work.

Providers should be able to define:

- Available days
- Available hours
- Time off
- Booking windows
- Emergency availability
- Recurring availability
- Service-specific availability

Clients should be able to view available times when providers choose to make them visible.

The module may support appointment requests, booking confirmations, reminders, and calendar synchronization.

## Quotes and Estimates

The Quotes and Estimates module allows providers to create service estimates.

Providers should be able to:

- Create itemized estimates
- Define fixed prices
- Define hourly prices
- Add materials or service charges
- Define deposits
- Define estimate expiration dates
- Update or revise estimates
- Send estimates to clients
- Track acceptance or rejection

Clients should be able to review and approve estimates before payment or work begins.

Accepted estimates may be converted into invoices.

## Secure Transactions

The Secure Transactions module supports purchasing and payment workflows between clients and providers.

The platform should support modular payment providers rather than requiring a single payment processor.

Payment capabilities may include:

- One-time payments
- Deposits
- Partial payments
- Recurring payments
- Refunds
- Milestone payments
- Escrow-compatible workflows where supported
- Provider payouts

Sensitive payment information should be handled through secure tokenization or approved payment provider systems.

The platform should avoid storing unnecessary payment credentials.

Transaction records must be securely retained and associated with relevant invoices, receipts, and reporting records.

## Invoices

The Invoice module automatically creates and manages itemized invoices.

Invoices may include:

- Unique invoice identifier
- Provider information
- Client information
- Service description
- Line items
- Quantities
- Prices
- Taxes where applicable
- Discounts
- Deposits
- Payment status
- Due dates
- Issue dates

Providers should be able to create manual invoices when necessary.

Invoices should be available in human-readable and machine-readable formats.

Providers and clients should be able to access their relevant invoice history.

## Receipts

The Receipt module generates receipts for completed payments.

Receipts should include:

- Unique receipt identifier
- Transaction date
- Payment amount
- Payment status
- Associated invoice
- Provider information
- Client information
- Payment reference where appropriate

Receipts should be available for download, export, and long-term record keeping.

## Tax Reporting

The Tax Reporting module provides service providers with organized financial records and reporting tools.

Reports may include:

- Gross income
- Refunds
- Fees
- Expenses when entered or supported
- Net income summaries
- Client payment totals
- Transaction history
- Monthly summaries
- Quarterly summaries
- Annual summaries

The system should support accountant-friendly exports.

Reports may be available in:

- CSV
- PDF
- JSON
- Other portable formats

Tax reporting features must clearly distinguish between record preparation and professional tax, legal, or accounting advice.

## Provider Dashboard

The Provider Dashboard gives service providers access to their activity and business information.

The dashboard may include:

- Profile status
- Search visibility information
- Service listings
- Appointment activity
- Quote activity
- Invoice status
- Payments
- Earnings
- Reviews
- Tax summaries
- Verification status
- Saved reports

Providers should be able to understand how their profile is performing without requiring opaque analytics.

## Client Accounts

The Client Accounts module manages client information and service activity.

Clients should be able to:

- Manage account information
- Save favorite providers
- Review service history
- Track quotes
- Track appointments
- Access invoices
- Access receipts
- Manage payment activity
- Leave verified reviews
- Save searches
- Receive service alerts

Clients should retain access to their own records and data exports.

## Messaging

The Messaging module enables communication between clients and providers.

Messaging should support:

- Direct conversations
- Service inquiries
- Quote discussions
- Appointment communication
- Transaction-related communication

Security and privacy controls should protect message content and account information.

The architecture should allow support for encrypted messaging where technically appropriate.

## Reviews and Reputation

The Reviews and Reputation module supports trustworthy feedback.

The system should prioritize reviews associated with verified service activity or completed transactions.

Reviews may include:

- Overall rating
- Written feedback
- Communication
- Reliability
- Quality of work
- Other service-specific criteria

Providers should have the ability to respond to reviews.

The platform should provide moderation and dispute mechanisms for fraudulent, abusive, or misleading reviews.

Reputation systems must not create undisclosed or opaque scoring systems.

## Verification

The Verification module supports optional verification of provider information.

Verification categories may include:

- Identity
- Business registration
- Professional licenses
- Certifications
- Insurance
- Background verification where legally appropriate

Verification must be optional unless required by applicable law or the nature of a specific service.

The platform should minimize public exposure of sensitive documents and personal information.

## Dispute Management

The Dispute Management module provides structured workflows for disagreements related to services or transactions.

The module may support:

- Client complaints
- Provider responses
- Evidence submission
- Transaction history review
- Resolution tracking
- Refund workflows
- Escalation procedures

Communities and self-hosted deployments should be able to configure dispute policies.

## Notifications

The Notifications module manages platform alerts and reminders.

Notifications may include:

- New messages
- Booking requests
- Appointment reminders
- Quote updates
- Invoice updates
- Payment confirmations
- Refund notifications
- Search alerts
- Service availability alerts

Users should be able to control notification preferences.

## Data Portability

The Data Portability module ensures that users can access and export their information.

Providers should be able to export:

- Profile information
- Service information
- Reviews where legally appropriate
- Appointments
- Quotes
- Invoices
- Receipts
- Transactions
- Tax reports

Clients should be able to export their account records and transaction history.

Portable data formats should be prioritized.

## Accessibility and Localization

ServiceLens must support accessible interfaces and inclusive design.

The platform should support:

- Keyboard navigation
- Screen readers
- Responsive design
- Mobile devices
- Clear language
- Localization
- Multiple languages
- Adjustable interface settings where practical

Natural-language search should support multiple languages as language capabilities become available.

# Optional Plugin Modules

## Portfolio Plugin

The Portfolio Plugin allows providers to showcase examples of completed work.

Supported content may include:

- Images
- Videos
- Project descriptions
- Before and after examples
- Service examples

Providers must control the visibility of portfolio content.

## Advanced Calendar Plugin

The Advanced Calendar Plugin provides expanded scheduling capabilities.

Features may include:

- External calendar synchronization
- Advanced booking rules
- Buffer periods
- Service duration rules
- Multi-provider scheduling
- Recurring appointments

## AI Listing Assistant Plugin

The AI Listing Assistant Plugin helps providers improve service descriptions.

The plugin may assist with:

- Writing descriptions
- Improving clarity
- Identifying missing information
- Generating search-friendly terminology
- Translating service descriptions

Provider approval must be required before generated content is published.

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
  - [https://roxanneardary.com/servicelens/](https://roxanneardary.com/servicelens/)

---

## License & Notice Requirements

ServiceLens is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.  
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- ServiceLens specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
