## Maintenance Policy

Version 1.1

Issued 2021-08-07

Last Updated and Approved 2022-08-07


##### Purpose
Maintenance policy for ZFM.

##### Scope
ZFM System

##### Responsibilities
Technical support must ensure that the policies described here are carried out.

##### Management Commitment
Management must ensure that the policies described here are implemented in the system.

### Physical Maintenance

ZFM is not perform physical hardware maintenance for client or server side software.

Maintenance of client side information systems equipment (computers, tablets, printers, phones)
is delegated to the customer.

Maintenance of Server side equipment is inherited by AWS hosting service.

### ZFM software maintenance (client and server)

All modules of ZFM code must be monitored for security vulnerabilities.

#### Process

GitHub dependabot provides security notifications for vulnerable packages.
If warranted, dependabot security notifications should be addressed with the
next release of the software.
If the notification is urgent, change should be implemented in a special
security release.

Each release of the software should include a check of outdated npm packages
and updates if warranted.
It is not necessary to update every outdated package particularly if they
involve breaking changes.

### ZFM client side operating system maintenance

The ZFM client runs in a modern browser on the customer's device (phone, computer or tablet).
The maintenance of the client system's operating system and browser software
is the responsibility of the customer.

### ZFM Server side operating system maintenance

The operating system software must be updated regularly.
On Linux systems this is done with apt.


