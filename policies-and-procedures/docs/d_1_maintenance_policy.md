## Maintenance Policy

Version Draft 0.1

Issued: TBD

Last Updated and Approved TBD

### Purpose

Develop, implement, and maintain a plan for maintaining production
hardware and software for ZFM.

### Scope

ZFM System

### Responsibilities

Management team and technical team must develop the maintenance plan.

Same must review and update the plan on an annual basis.

The technical team is responsible for testing and implementing the plan.

#### Management Commitment

Management must ensure that the plan is developed, maintained, reviewed,
understood and implemented by appropriate staff.

### Physical Maintenance

The web hosting service is responsible for the physical maintenance of servers.

Maintenance of client side information systems equipment (computers, tablets,
printers, phones) is the responsibility the customer.

### ZFM software maintenance (client and server)

All modules of ZFM code must be monitored for security vulnerabilities.
Vulnerabilities must be dealt with in a timely fashion.

#### Process

GitHub dependabot provides security notifications for vulnerable packages. If
warranted, dependabot security notifications should be addressed with the next
release of the software. If the notification is urgent, change should be
implemented in a special security release.

Each release of the software should include a check of outdated npm packages and
updated if warranted. It is not necessary to update an outdated package if it
poses no security threat, particularly if the new version of the package
includes breaking changes.

### ZFM client side operating system maintenance

The ZFM client runs in a modern browser on the customer's device (phone,
computer or tablet). The maintenance of the client system's operating system and
browser software is the responsibility of the customer.

### ZFM production server operating system maintenance

The operating system software must be updated regularly. On Linux systems this
is done with apt.


