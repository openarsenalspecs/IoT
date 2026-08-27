# MedFair Specification
**Search Every Avenue. Find the Fairest Outcome.**
- HTML Mirror: [https://roxanneardary.com/medfair-specification/](https://roxanneardary.com/medfair-specification/)  

---

## Overview

MedFair is an AI-powered medical financial rights, obligation verification, cost-reduction, dispute, and repayment optimization specification. MedFair is designed to determine the lowest legally and contractually supportable medical obligation before recommending how that obligation should be resolved or repaid.

MedFair does not assume that the amount shown on a medical bill represents the amount a patient ultimately owes. The system evaluates insurance contracts, EOBs, negotiated rates, financial assistance, charity care, government programs, billing errors, medical necessity, good-faith estimates, No Surprises Act protections, coordination of benefits, state and federal protections, debt-collection activity, and other applicable factors that may affect the actual obligation.

The system follows a patient-centered optimization process:

**Discover → Verify → Reconcile → Identify Rights → Identify Errors → Identify Reductions → Challenge → Appeal → Negotiate → Optimize → Resolve → Monitor**

---

## Design Principles

- Patient-centered financial advocacy
- Modular architecture
- Open source implementation
- Local-first processing where practical
- Vendor-neutral design
- Interoperability
- Evidence-based analysis
- Explainable AI
- Human-in-the-loop governance
- Privacy and data minimization
- Auditable calculations
- Source and evidence provenance
- Separation of facts, assumptions, and conclusions
- Separation of financial analysis from medical judgment
- Separation of legal information from legal advice
- User control over decisions and actions
- No repayment recommendation before obligation analysis
- No unsupported legal or medical conclusions
- No unnecessary collection or monetization of sensitive information

---

## Core Modules

### Medical Bill Intake

The Medical Bill Intake module shall provide mechanisms for importing, processing, classifying, and extracting information from medical financial documents.

Features include:

- Hospital bill import
- Physician bill import
- Specialist bill import
- Laboratory bill import
- Imaging bill import
- Ambulance bill import
- Emergency-service bill import
- Pharmacy-related medical bill import where applicable
- Insurance EOB import
- Insurance claim document import
- Payment record import
- Collection notice import
- Settlement offer import
- Financial assistance correspondence import
- Good-faith estimate import
- Prior authorization documentation import
- Paper-document OCR
- Automatic document classification
- Automatic field extraction
- Date extraction
- Amount extraction
- Provider identification
- Account identification
- Document version tracking
- Duplicate document detection

### Medical Encounter Reconstruction

The Medical Encounter Reconstruction module shall reconstruct the financial and service relationships associated with an episode of care.

Features include:

- Complete episode reconstruction
- Service-to-date matching
- Provider-to-encounter matching
- Facility-to-encounter matching
- Emergency encounter identification
- Inpatient encounter identification
- Outpatient encounter identification
- Elective encounter identification
- Ancillary service identification
- Facility and professional charge separation
- Related bill linking
- Related EOB linking
- Missing documentation identification
- Encounter inconsistency detection
- Chronological encounter records

### Provider Identity and Ownership Analyzer

The Provider Identity and Ownership Analyzer shall identify the entities involved in billing and determine relationships between them.

Features include:

- Billing entity identification
- Rendering provider identification
- Facility identification
- Physician group identification
- Affiliated organization identification
- Third-party billing company identification
- Collection agency identification
- Nonprofit hospital identification
- For-profit hospital identification
- Hospital ownership identification
- Billing relationship identification
- Duplicate billing entity detection
- Ownership and billing relationship history

### Insurance Contract Analyzer

The Insurance Contract Analyzer shall evaluate insurance plan provisions and determine how contractual requirements affect patient responsibility.

Features include:

- Applicable insurance plan identification
- Plan document analysis
- Insurance contract analysis
- Deductible analysis
- Copayment analysis
- Coinsurance analysis
- Network status analysis
- Out-of-network provision analysis
- Negotiated rate analysis
- Allowed amount analysis
- Contractual adjustment analysis
- Coverage requirement analysis
- Exclusion analysis
- Limitation analysis
- Claim-processing requirement analysis
- Incorrect patient responsibility detection
- Appeal rights identification
- Appeal deadline identification

### EOB Reconciliation Engine

The EOB Reconciliation Engine shall reconcile insurance explanations of benefits with provider billing records.

Features include:

- Provider bill and EOB comparison
- Individual service matching
- Billed amount matching
- Allowed amount matching
- Insurance payment matching
- Contractual adjustment matching
- Deductible recalculation
- Coinsurance recalculation
- Copayment recalculation
- Out-of-pocket responsibility recalculation
- Discrepancy detection
- Unexplained balance identification
- Incorrect balance transfer identification
- Insurance calculation discrepancy identification
- Patient responsibility reconciliation reports

### Medical Necessity Review

The Medical Necessity Review module shall identify potential coverage disputes involving medical necessity without independently making clinical determinations.

Features include:

- Medical necessity denial analysis
- Applicable coverage criteria analysis
- Potential coverage dispute identification
- Documentation gap identification
- Plan provision identification
- Relevant clinical criteria identification
- Supporting documentation organization
- Appeal evidence preparation
- Inconsistency detection between denial reasoning and available documentation
- Medical necessity appeal tracking
- Financial and clinical analysis separation
- Professional escalation for clinical determinations

### Prior Authorization Analyzer

The Prior Authorization Analyzer shall evaluate authorization requirements and their potential financial consequences.

Features include:

- Prior authorization requirement identification
- Authorization status verification
- Authorization documentation analysis
- Authorization-related denial identification
- Missing authorization information detection
- Potential retroactive authorization identification
- Authorization requirement tracking
- Authorization deadline tracking
- Authorization appeal support
- Authorization evidence management

### Claim Appeal Engine

The Claim Appeal Engine shall support structured insurance claim disputes and appeals.

Features include:

- Denial reason analysis
- Claim code analysis
- Denial and plan provision comparison
- Appeal right identification
- Internal appeal deadline identification
- External review opportunity identification
- Appeal document generation
- Supporting evidence organization
- Appeal status tracking
- Insurer response tracking
- Additional information request tracking
- Escalation opportunity identification
- Appeal history preservation

### Good-Faith Estimate Engine

The Good-Faith Estimate Engine shall evaluate estimates provided for medical services and compare them with resulting charges.

Features include:

- Good-faith estimate requirement analysis
- Estimate document analysis
- Final bill comparison
- Significant discrepancy detection
- Unexpected charge identification
- Missing service identification
- Applicable dispute procedure identification
- Dispute deadline tracking
- Dispute documentation generation
- Estimate evidence preservation
- Dispute outcome tracking

### No Surprises Protection Analyzer

The No Surprises Protection Analyzer shall evaluate whether federal or state surprise-billing protections may affect an obligation.

Features include:

- Protected emergency service identification
- Protected non-emergency service identification
- Provider network verification
- Facility network verification
- Protected ancillary service identification
- Potential balance billing detection
- Patient consent requirement analysis
- Federal protection identification
- State protection identification
- Dispute procedure identification
- Dispute deadline tracking
- Supporting documentation generation
- Legal uncertainty escalation

### Coordination of Benefits Engine

The Coordination of Benefits Engine shall identify potentially responsible payers and evaluate whether insurance coordination has been properly performed.

Features include:

- Responsible payer identification
- Primary insurance identification
- Secondary insurance identification
- Tertiary coverage identification
- Medicare coordination analysis
- Medicaid coordination analysis
- Commercial insurance coordination analysis
- Supplemental coverage analysis
- Employer-sponsored coverage analysis
- Automobile-related coverage identification
- Workers' compensation coverage identification
- Other payer identification
- Coordination-of-benefits error detection
- Improper patient responsibility identification
- Post-coordination responsibility recalculation
- Payer communication tracking

### Medical Billing Error Detection

The Medical Billing Error Detection module shall identify discrepancies and anomalies that may affect the validity or amount of a medical obligation.

Features include:

- Duplicate charge detection
- Duplicate service detection
- Duplicate bill detection
- Impossible date detection
- Inconsistent date detection
- Incorrect quantity detection
- Procedure code inconsistency detection
- Diagnosis and procedure relationship analysis
- Unsupported service identification
- Potentially unreceived service identification
- Incorrect insurance payment detection
- Incorrect deductible application detection
- Incorrect coinsurance detection
- Incorrect copayment application detection
- Incorrect network status detection
- Incorrect patient responsibility detection
- Billing anomaly identification
- Billing dispute evidence generation

### Financial Assistance Engine

The Financial Assistance Engine shall identify and evaluate hospital and provider financial assistance programs.

Features include:

- Financial assistance policy identification
- Eligibility requirement analysis
- Household income analysis
- Household size analysis
- Application procedure identification
- Application deadline identification
- Presumptive eligibility identification
- Retroactive assistance identification
- Potential assistance calculation
- Assistance program comparison
- Application generation
- Supporting documentation generation
- Application tracking
- Additional information request tracking
- Application outcome tracking

### Charity Care Engine

The Charity Care Engine shall identify charitable and income-based programs that may reduce medical obligations.

Features include:

- Charity care program identification
- Nonprofit hospital assistance identification
- Charity care policy analysis
- Sliding-scale program identification
- Income-based reduction identification
- Hospital foundation identification
- Community assistance identification
- Disease-specific assistance identification
- Charitable organization identification
- Program comparison
- Eligibility tracking
- Application tracking
- Award tracking
- Denial tracking

### Government Benefits and Assistance Engine

The Government Benefits and Assistance Engine shall identify public programs that may reduce or satisfy medical obligations.

Features include:

- Medicaid eligibility analysis
- Medicare eligibility analysis
- CHIP eligibility analysis
- ACA Marketplace assistance analysis
- State medical assistance analysis
- County assistance analysis
- Government program identification
- Retroactive eligibility analysis
- Application requirement identification
- Deadline identification
- Coordination requirement analysis
- Application tracking
- Determination tracking
- Post-approval obligation recalculation

### Federal Rights Engine

The Federal Rights Engine shall identify applicable federal laws, regulations, requirements, and protections affecting medical financial obligations.

Features include:

- Federal protection identification
- Federal medical billing requirement analysis
- Federal insurance protection analysis
- Federal debt collection protection analysis
- Federal credit reporting protection analysis
- No Surprises Act analysis
- Nonprofit hospital requirement analysis
- Federal complaint mechanism identification
- Federal agency identification
- Federal regulatory change monitoring
- Federal guidance monitoring

### State Law Engine

The State Law Engine shall identify state-specific requirements and protections affecting medical obligations.

Features include:

- Applicable state identification
- State medical debt protection analysis
- State balance billing protection analysis
- State insurance requirement analysis
- State charity care requirement analysis
- State hospital requirement analysis
- State debt collection restriction analysis
- State credit reporting protection analysis
- State regulatory agency identification
- State complaint procedure identification
- State legislation monitoring
- State regulation monitoring
- State enforcement action monitoring

### Statute of Limitations Analyzer

The Statute of Limitations Analyzer shall identify potentially applicable limitation periods and related deadlines while recognizing jurisdictional uncertainty.

Features include:

- Potential limitation period identification
- Jurisdiction identification
- Relevant debt date identification
- Obligation date tracking
- State rule analysis
- Potential deadline tracking
- Limitation issue classification
- Debt validity distinction
- Jurisdiction-dependent issue identification
- Potential tolling consideration identification
- Consequential-action warnings
- Limitation evidence tracking
- Professional legal review escalation

### Legal Obligation Calculator

The Legal Obligation Calculator shall calculate and classify the potentially supportable medical obligation based on verified evidence.

Features include:

- Original billed amount calculation
- Insurance adjustment calculation
- Insurance payment calculation
- Contractual adjustment calculation
- Disputed amount calculation
- Billing error reduction calculation
- Financial assistance reduction calculation
- Charity care reduction calculation
- Government assistance calculation
- Protected amount calculation
- Potentially invalid amount calculation
- Remaining supportable obligation calculation
- Confirmed amount classification
- Probable amount classification
- Potential amount classification
- Disputed amount classification
- Unresolved amount classification
- Calculation methodology display
- Calculation history preservation

### Debt Validation Engine

The Debt Validation Engine shall evaluate whether a debt presented for collection corresponds with the underlying verified obligation.

Features include:

- Original creditor identification
- Current creditor identification
- Collection agency identification
- Debt ownership verification
- Account information verification
- Balance verification
- Date verification
- Duplicate debt identification
- Inconsistent account information detection
- Validation request generation
- Validation response tracking
- Validated information comparison
- Unresolved discrepancy identification

### Collection Activity Monitor

The Collection Activity Monitor shall track actions associated with medical debt collection.

Features include:

- Collection letter tracking
- Collection call tracking
- Payment demand tracking
- Settlement offer tracking
- Collection lawsuit tracking
- Reported balance tracking
- Collection deadline tracking
- Dispute deadline tracking
- Collection history preservation
- Inconsistent collection activity identification
- Legal proceeding escalation

### Credit Reporting Analyzer

The Credit Reporting Analyzer shall compare reported medical debt information against verified obligation information.

Features include:

- Medical debt credit-report identification
- Reported debt comparison
- Reported balance comparison
- Validated obligation comparison
- Potentially inaccurate reporting identification
- Credit reporting dispute tracking
- Reporting entity response tracking
- Federal protection identification
- State protection identification
- Credit reporting evidence preservation
- Potential legal issue escalation

### Negotiation Engine

The Negotiation Engine shall generate evidence-based communications for resolving medical financial obligations.

Features include:

- Provider correspondence generation
- Financial assistance request generation
- Charity care request generation
- Billing dispute generation
- Insurance appeal generation
- Collection response generation
- Settlement proposal generation
- Payment plan request generation
- Itemized bill request generation
- Documentation request generation
- Contractual adjustment request generation
- Corrected billing request generation
- Evidence-based citation support
- Policy-based citation support
- Contract-based citation support
- Regulation-based citation support

### Settlement Optimization Engine

The Settlement Optimization Engine shall compare settlement opportunities against other available resolution strategies.

Features include:

- Lump-sum settlement analysis
- Installment settlement analysis
- Payment discount identification
- Settlement offer comparison
- Settlement scenario modeling
- Total settlement cost calculation
- Financial assistance comparison
- Insurance appeal comparison
- Payment plan comparison
- Expected savings calculation
- Settlement condition identification

### Repayment Optimization Engine

The Repayment Optimization Engine shall determine the lowest-cost lawful strategy for resolving the remaining obligation.

Features include:

- Full-payment option comparison
- Payment plan comparison
- Zero-interest plan comparison
- Negotiated settlement comparison
- Financial assistance comparison
- Charity care comparison
- Government assistance comparison
- Insurance appeal comparison
- Billing dispute comparison
- Combined strategy comparison
- Monthly payment calculation
- Total repayment cost calculation
- Expected savings calculation
- Repayment duration calculation
- Lowest-cost resolution identification

### Cash Flow Optimization Engine

The Cash Flow Optimization Engine shall evaluate repayment strategies against sustainable financial capacity.

Features include:

- Sustainable monthly payment analysis
- Available cash analysis
- Recurring income and expense analysis
- Emergency reserve evaluation
- Payment burden calculation
- Interest cost calculation
- Payment timing analysis
- Unsustainable plan detection
- Lower-cost alternative identification
- Repayment scenario modeling

### Bankruptcy Avoidance Analyzer

The Bankruptcy Avoidance Analyzer shall identify potential alternatives to bankruptcy while avoiding unsupported legal conclusions.

Features include:

- Medical debt analysis alongside other obligations
- Financial distress identification
- Repayment alternative modeling
- Settlement alternative modeling
- Assistance opportunity identification
- Debt resolution strategy comparison
- Potential bankruptcy alternatives
- Professional bankruptcy evaluation flagging
- User decision control
- Legal uncertainty escalation

### Provider Transparency Module

The Provider Transparency Module shall organize publicly available information about providers and their financial policies.

Features include:

- Hospital pricing information collection
- Financial assistance policy collection
- Charity care policy collection
- Billing policy collection
- Collection policy collection
- Nonprofit status identification
- Payment option identification
- Published charge comparison
- Assistance comparison
- Payment plan comparison
- Billed charge and supportable obligation comparison

### Regulatory Change Monitor

The Regulatory Change Monitor shall identify changes that may affect existing or future cases.

Features include:

- Federal regulation monitoring
- Federal guidance monitoring
- State legislation monitoring
- State regulation monitoring
- Insurance regulation monitoring
- Hospital policy monitoring
- Regulatory enforcement monitoring
- Affected case identification
- User notification
- Case reassessment
- Obligation recalculation when appropriate

### Evidence and Provenance Engine

The Evidence and Provenance Engine shall provide traceability from source material through findings and recommendations.

Features include:

- Source record management
- Source document preservation
- Evidence-to-finding linking
- Finding-to-rule linking
- Rule-to-calculation linking
- Calculation-to-recommendation linking
- Document version preservation
- Decision history
- Evidence confidence tracking
- Unsupported assumption identification
- Complete audit trails

### Patient Financial Rights Assessment

The Patient Financial Rights Assessment module shall provide an explainable assessment of potential rights, protections, and financial reduction opportunities.

Features include:

- Insurance compliance evaluation
- Billing accuracy evaluation
- Financial assistance eligibility evaluation
- Charity care eligibility evaluation
- Government assistance eligibility evaluation
- Federal protection evaluation
- State protection evaluation
- Collection compliance evaluation
- Reduction opportunity identification
- Unresolved right identification
- Explainable rights assessment

### Human Escalation Engine

The Human Escalation Engine shall identify circumstances where professional review is appropriate.

Features include:

- Lawsuit identification
- Legal deadline identification
- Bankruptcy-related issue identification
- Potential fraud identification
- Complex insurance dispute identification
- Potential malpractice issue identification
- Conflicting legal requirement identification
- Uncertain legal interpretation identification
- High-risk financial decision identification
- Qualified professional review recommendation
- Unsupported legal conclusion prevention

### Case Management

The Case Management module shall provide lifecycle management for medical financial cases.

Features include:

- Patient case creation
- Debt case creation
- Billing dispute creation
- Case status tracking
- Task tracking
- Deadline tracking
- Document tracking
- Correspondence tracking
- Appeal tracking
- Assistance application tracking
- Settlement tracking
- Payment plan tracking
- Resolution tracking
- Complete case history

### Outcome Tracking

The Outcome Tracking module shall capture actual case results for analysis and future optimization.

Features include:

- Original obligation recording
- Identified error recording
- Disputed amount recording
- Successful reduction recording
- Assistance award recording
- Settlement amount recording
- Final obligation recording
- Total savings recording
- Resolution time recording
- Appeal outcome recording
- Dispute outcome recording
- Negotiation outcome recording
- Anonymized outcome intelligence

### Explainable AI

The Explainable AI module shall make recommendations understandable, traceable, and reviewable.

Features include:

- Recommendation explanations
- Supporting evidence identification
- Applicable rule identification
- Calculation display
- Assumption display
- Uncertainty display
- Fact and assumption separation
- Legal information and legal advice distinction
- Financial analysis and professional advice distinction
- Confidence levels
- Information gap identification
- High-risk human review requirements

### Privacy and Security

The Privacy and Security module shall protect medical, financial, insurance, and legal information processed by MedFair.

Features include:

- Local-first processing options
- Encryption
- Data minimization
- User-controlled document storage
- Granular consent
- Permission management
- Document expiration
- Data deletion
- Data export
- Role-based access
- Access auditing
- Case-level privacy controls
- No sale of medical information
- No sale of financial information
- No medical-data-based advertising

### Interoperability

The Interoperability module shall support exchange of information across systems while maintaining a vendor-neutral architecture.

Features include:

- Standards-based document ingestion
- Structured medical billing data
- Structured insurance data
- Structured EOB data
- Structured policy data
- Structured legal-source data
- Exportable case records
- Exportable evidence packages
- API support
- Modular provider integrations
- Vendor-neutral interfaces
- Proprietary lock-in avoidance

### Human-in-the-Loop Governance

The Human-in-the-Loop Governance module shall preserve user control over consequential decisions.

Features include:

- User approval before sending disputes
- User approval before submitting appeals
- User approval before accepting settlements
- User approval before establishing payment plans
- Human review of legal uncertainty
- Human review of clinical uncertainty
- Human review of high-value financial decisions
- Complete decision auditability
- User override capability
- Transparent AI limitations

---

## Optional Plugin Modules

Optional plugins shall extend MedFair without requiring changes to the core specification.

### Legal Research Plugin

- Legal source retrieval
- Statute retrieval
- Regulation retrieval
- Case law retrieval
- Administrative decision retrieval
- Jurisdiction-specific legal research
- Legal source citation
- Legal source version tracking

### Insurance Portal Plugin

- Insurance portal integration
- Claim status retrieval
- EOB retrieval
- Appeal status retrieval
- Coverage information retrieval
- Network status retrieval
- Authorization status retrieval

### Hospital Portal Plugin

- Provider portal integration
- Bill retrieval
- Payment history retrieval
- Financial assistance application support
- Financial assistance status retrieval
- Billing communication retrieval
- Payment plan information retrieval

### Government Benefits Plugin

- Government program discovery
- Eligibility screening
- Application assistance
- Application status tracking
- Program change monitoring

### Credit Bureau Plugin

- Credit report import
- Medical debt identification
- Reported balance comparison
- Dispute workflow support
- Dispute status tracking

### Document Signing Plugin

- Electronic document signing
- Authorization forms
- Appeal submissions
- Financial assistance forms
- Settlement documents
- User approval workflows

### Professional Referral Plugin

- Attorney referral
- Consumer advocate referral
- Insurance advocate referral
- Medical billing specialist referral
- Bankruptcy professional referral
- Financial counselor referral
- Qualified clinical review referral

### Notification Plugin

- Deadline notifications
- Appeal reminders
- Payment reminders
- Document requests
- Regulatory change notifications
- Case status notifications
- Escalation notifications

### Financial Planning Plugin

- Household cash-flow analysis
- Budget analysis
- Debt prioritization
- Payment capacity analysis
- Emergency reserve planning
- Resolution scenario modeling

### Data Export Plugin

- Case export
- Evidence package export
- Appeal package export
- Billing dispute package export
- Financial assistance package export
- Audit report export
- Structured data export

---

## AI Safety and Decision Boundaries

MedFair shall distinguish between:

- Verified facts
- User-provided information
- Extracted information
- AI-generated interpretations
- Legal information
- Legal advice
- Financial analysis
- Financial advice
- Clinical information
- Medical judgment

MedFair shall not represent an AI-generated interpretation as a definitive legal, financial, or medical determination when professional review is required.

The system shall identify uncertainty and missing information rather than silently filling critical gaps with assumptions.

High-risk actions shall require explicit user approval or appropriate professional review.

## Core Optimization Rule

MedFair shall not begin with the question:

**How can the patient pay this bill?**

MedFair shall begin with:

**What is the patient actually responsible for, and what lawful avenues can reduce or eliminate that obligation?**

Only after analyzing the underlying obligation shall MedFair optimize the remaining financial resolution.

## Resolution Framework

MedFair shall evaluate available resolution paths in a prioritized manner:

- Correct the bill
- Correct insurance processing
- Coordinate other available coverage
- Apply contractual adjustments
- Apply legal protections
- Apply financial assistance
- Apply charity care
- Apply government assistance
- Challenge medical necessity determinations
- Challenge improper billing
- Challenge protected surprise billing
- Validate collection debt
- Challenge inaccurate reporting
- Negotiate the remaining obligation
- Establish the lowest-cost repayment plan
- Escalate to qualified professionals when necessary

## Fair Outcome Model

MedFair shall optimize for the fairest achievable outcome rather than the highest provider recovery or the lowest monthly payment alone.

The system may consider:

- Verified obligation
- Legally supportable obligation
- Contractually supportable obligation
- Available reductions
- Available assistance
- Total repayment cost
- Monthly affordability
- Interest
- Fees
- Settlement terms
- Resolution time
- Credit implications
- Legal deadlines
- User-selected financial constraints

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
  - [https://roxanneardary.com/medfair/](https://roxanneardary.com/medfair/)  

---

## License & Notice Requirements

MedFair is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- MedFair specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.
  Any update that adds new contributors or modifies attribution should also update `notice.md`.
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
