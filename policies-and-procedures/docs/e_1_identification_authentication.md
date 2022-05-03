## Identification and Authentication Policy

Version TBD

Issued TBD

Last Updated and Approved TBD


##### Purpose
Define Identification and Authentication policy for ZFM.

##### Scope
ZFM System

##### Responsibilities
Development must ensure that the controls described here are implemented
in the system.

##### Management Commitment
Management must ensure that the controls described here are implemented in the system.


###External User Identifier
Users have an identifier with which they identify themselves to the system.
External identifiers are:

- unique
  
- mutable

The system does not store references to the external identifier because it can change.

### Internal User Identifier
Users will be identified by internal identifier.
Internal identifiers are:

- unique
  
- immutable
  
- not of use to end users

The system uses the internal identifier to store references to user objects.

### User Email Address

The system requires an email address for every user.
Email addresses are effectively identifying attributes of a user and therefore they must be unique.
Email addresses are used to communicate messages to the users such as status updates,
welcome messages and password reset coordination.

### User Passwords

Users must sign in to the system using a password inorder to access functionality.

The system assigns a password automatically when a user is created.

A user can change their password at any time when logged in.

A user can have their password reset without knowing their current password (forgotten password).

Any passwords issued by the system are randomly generated, include special character and are
at least 8 characters long. Such passwords are valid for signing into the system only once.

The system must be configurable for any deployment to impose password constraints.
Specifically configurable constraints are:

- minimum password length

- requirement of uppercase characters

- requirement of numeric digits

- requirement of special characters

- requirement of password strength. Each character used scores 5 points, but only up to 5 occurrences of any specific character.
  Each different type of character (lowercase, uppercase, numeric and special) scores additional 10 points. 
  80 points is a strong password.

Strong memorable pass phrases must be allowable.
  
### System treatment of passwords

No users of the system will have access to any password that any other user sets for themselves.

Passwords will always be encrypted when transmitted between the client and the server.

Passwords will always be encrypted when stored.

The system must not be able to decrypt a stored password.

### Use of Tokens for Authentication

When a user initially logs in, they are required to authenticate with their password.
When password authentication is successful, the user is granted a JWT which is used 
to authenticate further actions by that user until the JWT expires.

The system must allow customer facility to specify the duration of validity for JWTs.

The system must disallow users from having two valid web tokens at any one time.

The if a user is deactivated and they have a valid token, that token must be
redacted immediately.









