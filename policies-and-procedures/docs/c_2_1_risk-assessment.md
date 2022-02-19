## Risk Assessment Policy (C.2.1)

Version Draft 0.1

Issued: TBD

Last Updated and Approved TBD

##### Purpose

Develop and document Risk assessment procedures for ZFM.

##### Scope

ZFM System

##### Responsibilities

Management team and technical team must develop the plan.

Same must review and update the plan on an annual basis.

Same must perfomr the risk assessment and document the results.

#### Management Commitment

Management must ensure that the plan is developed, maintained, reviewed,
understood and implemented by appropriate staff.

### Security Categorization (C.2.2)

Since the data in the system can be released to the general public without harming
customer, we do not perform a formal security categorization.

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
