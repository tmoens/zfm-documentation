## Configuration Management Policy

Draft 1.0

Issued TBD

Last Updated and Approved TBD

### Purpose

Establish, maintain, and effectively implement a plan for configuration
management for ZFM.

Configuration Management is the process for controlling modifications to
hardware, firmware, software, and documentation to ensure the information system
is protected against improper modifications before, during, and after system
implementation.

### Scope

ZFM System

### Responsibilities

Management team and technical team must develop the plan for configuration
management.

Same must review and update the plan on an annual basis.

The technical team is responsible for implementing the plan.

### Management Commitment

Management must ensure that the plan is developed, maintained, reviewed,
understood, tested and implemented by appropriate staff.

### Baseline Configuration

#### Baseline Configuration ZFM Software

The following must be stored in configuration management.

1. zfm client software

2. zfm server software

3. usage guidelines

4. installation documentation

The following **must not** be stored under configuration management:

1. customer data (like database backups)
2. passwords
3. private encryption keys
4. tokens
5. any information that could be used to compromise any particular deployment of
   the software
6. any information that should not be publicly exposed

##### Implementation

The system software is stored using git in GitHub. Configuration files that
contain sensitive information like database passwords are excluded using .gitignore
files.

#### Baseline Configuration Client Systems

There is no baseline configuration for clients using the ZFM software. Most
devices that support modern browsers can run it.

#### Baseline Configuration Production Server System

There is no baseline for a ZFM server system under configuration management.
Instead, a new server is installed with a recent bare-bones Debian OS. The
installation guide describes how to add and configure any additional features
required to deploy a system.

After installation, changes must be restricted to appropriate personnel and
performed through secure connections.

##### Implementation

A baseline installation for a new system is achieved by following the
installation guide.

After installation, access to the administration of the system is limited to ZFM
personnel, exclusively using SSL through server configuration. 

Password based access is disabled. 

Servers OS software is frequently updated using "apt".

### Security Impact Analysis

Any changes to the system should be analyzed in the light of potential security
impact.

##### Security Impact Analysis ZFM Software

ZFM code itself must be reviewed in this light before committing it to CM.

#### New NPM Packages used by ZFM

When a new package is used, it, and its dependencies should be checked for
security issues. This happens automatically when installing packages with NPM,
but it is wise to also review the site for the new package.

#### Newly Discovered Security Issues in Packages used by ZFM

At times a package that is already in use turns out to have a security issue.
These are identified and using "npm audit" and can often be fixed with
"npm audit fix", though sometimes it requires migration to a newer version of
the package which might involve code changes.

Also, notifications from dependabot on GitHub are indicators that a package
needs to be updated.

#### Security Impact Analysis for Production Server OS

Any updates to server packages or use of new server packages need to be:

1. checked for security issues
2. reviewed to understand secure deployment configurations
3. configured securely
4. documented in the system deployment guide


