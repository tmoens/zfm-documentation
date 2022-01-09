## Access Control Policy

Version 1.0

Issued 2021-08-04

Last Updated and Approved 2021-08-04


##### Purpose
Define Logical Access Controls for ZFM.

##### Scope
ZFM System

##### Responsibilities
Development must ensure that the controls described here are implemented in the system.

##### Management Commitment
Management must ensure that the controls described here are implemented in the system.

### ZFM User Account Management

ZFM delegates user account management to the customer.
ZFM must provide tools for the customer to manage accounts.

#### User Account Creation

Only a administrative user can create new users.
A potential user cannot create their own account.

#### User Account Updates

Users are able to manage their own passwords.
User administrators can edit other aspects of the user's account.

#### User Account Deactivation

The administrator can activate or deactivate a user at any time.
Deactivation of an authenticated user will cause the
user's authentication credentials to be canceled.

#### User Account Deletion

Any user that is referenced by another object in the system can not be deleted.
Other users can be deleted by the system administrator.
Deleted users are not archived.

### Permitted Actions without Identification or Authentication
A user can attempt login before identification or authentication.
A user can reset their password before authentication.
This supports "forgotten password" cycle.
User identification and authentication is required for all other actions.

### Remote Access
All user interaction is to be treated as if it were remote.
Local users receive no special access privileges.

### Wireless Access
Wireless access must be treated with equal security as wired access.

### Access Control for Mobile Devices
Mobile access must be treated equally securely as fixed access.

### Use of External Information Systems
ZFM uses public information regarding zebrafish
genetics provided by ZFIN.org.

### Publicly Accessible Content
No information from a ZFM system shall be made public by the system.




