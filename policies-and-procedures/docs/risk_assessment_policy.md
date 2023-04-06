## Risk Assessment Policy (C.2.1)

Version Draft 0.1

Issued: 2022-01-01

Last Updated and Approved 2022-01-01

##### Purpose

Develop and document Risk assessment procedures for ZFM.

##### Scope

ZFM System

##### Roles and Responsibilities

Management team and technical team must develop the plan.

Same must review and update the plan on an annual basis.

Same must perform the risk assessment and document the results.

##### Management Commitment

Management must ensure that the plan is developed, maintained, reviewed,
understood and implemented by appropriate staff.

### Security Categorization (C.2.2)

Upon review of NIST 800-60, ZFM stores, transmits, and processes information 
that closely maps to the Reporting and Information Type. 
Based on this type of data, the following impact levels are applicable for ZFM:

The highest level of data and information contained on the ZFM is considered Low. 

The assigned impact levels for each security objective (confidentiality,
integrity, and availability) for
ZFM are described below:

**Confidentiality**: Data confidentiality refers to the protection of information from unauthorized
disclosure. The confidentiality is ranked as Low.

**Integrity**: Data integrity refers to the requirement that information be protected from
unauthorized, unanticipated, or unintentional modification. The integrity is ranked as Low.

**Availability**: Timeliness and constant update are essential to the functional operation of ZFM.
The availability is ranked as Low.

### Risk Assessment (C.2.3)

Whenever there is a major functionality change or at a minimum of every three
years, assess the likelihood and impact of the following risks.

Document the likelihood of the risk coming to fruition, the impact of the risk,
the available mitigations and any actions required as result of the assessment.

Also the set of possible risks should be re-considered for expansion.

- unauthorized access of ZFM system and data through the ZFM client
- unauthorized use of ZFM system and data through the ZFM client
- unauthorized disclosure of ZFM system and data through the ZFM client
- unauthorized destruction of ZFM system and data through the ZFM client
- unauthorized destruction of ZFM system and data through direct host login
- unauthorized destruction of ZFM system and data through the system's API
- failure of the ZFM system or parts thereof (disaster recovery)

### Vulnerability Scanning (C.2.4)

Both the zf-server and zf-client software packages are to be scanned
regularly for security vulnerabilities.

#### Process for scanning

At this point we only use automated scanning at GitHub with dependabot.
All significant vulnerabilities are patched with the next release of the system.

Under extraordinary circumstances patches will be completed within a week
outside the regular release cycle.
