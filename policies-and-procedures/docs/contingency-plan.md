# Zebrafish Facility Manager Contingency Plan

Version Draft 0.1

Issued TBD

Last Updated and Approved TBD

## Purpose

This plan deals with contingencies to allow customers to continue to operate in
the event of major outages.

## Special Note

The ZFM system is typically not mission critical. Significant outages can be
tolerated by the customer without affecting their work. This contingency plan
reflects that reality.

However, should a customer require a fault-tolerant system that includes running
over multiple datacenters, this can be accomplished as a custom deployment which
involves costs both for the setup of the deployment and ongoing costs for the
environment itself.

## Essential Functions

The system provides zebrafish researchers with the following essential
functions:

1. Tracking of which genetic markers (Mutations and Transgenes) are, or have
   been, in use in their facility at any point.
2. Tracking of which stocks are or have been in existence in their facility
3. Tracking of the lineage of the stocks
4. Tracking of which stocks carry which markers
5. Tracking of where stocks currently reside in their facility

Before the ZFM system was created, Zebrafish researchers have been tracking this
information with their own ad-hoc solutions ranging from FileMaker Pro
databases, to Excel workbooks to paper notebooks.

## Contingency Requirements

### During Minor Outage < 3 business days

No contingency is required for a brief outage. Customers are able to continue to
carry out their experiments in the absence of the system. After the outage, the
customer can add any changes made during the outage.

#### Implementation Note

Customers are encouraged to export their data in Excel on a regular basis. The
exported workbook will allow them to continue to work very easily during any
brief outage.

A feature is planned to notify admin users of contingency planning

1. when they become administrators
2. annually thereafter
3. if changes to their responsibilities occur

The note will include:

1. reminder to export their data to Excel regularly
2. contact information in the event of an outage
3. a link to this contingency plan

### During Prolonged Outage > 3 business days

If the customer has not regularly exported their data to Excel, they will begin
to experience some hardship after a few days.

Should the customer require it, an Excel version of their database will be
provided to the customer after three days of outage.

Using the workbook, the customer can track changes made during the outage.

After the outage, either the customer or ZFM personnel can add the changes made
during the outage to the live system.

#### Implementation Note

During a prolonged outage, a temporary system can be spun up either on a data
center host or in the development environment. The temporary system does not
need to be available to the customer. That system can be loaded with the latest
database backup from the affected system. The temporary system can be used to
export the required Excel workbook which can then be transferred to the
customer.

### Termination of Customer Contract

When a customer or the organization terminates a contract for using the ZFM
software, the customer must be able to have their data available to provide
continuity in their research.

The customer has several options available and may exercise any or all of them:

1. Export their data in the form of an Excel workbook, including the
   relationships between the objects in their system.
2. Request their data as a SQL dump from the MariaBD database.
3. Request for their system and data to be migrated to a customer owned and
   managed web hosting site.
4. Request a copy of the entire code base of the system with rights modify and
   deploy it for their own use.
5. Request a custom formatting of their data, within reasonable limits. E.g. no
   stone tablets.
6. Request consulting on how to modify and deploy the system for themselves.

#### Implementation Note

1. The customer is able to Export data in this way at any time from the user
   interface.
2. After shutting the system down, perform a database export and transfer the
   SQL file to the customer. There are no charges for this service.
3. The customer provides access to a web hosting service with an appropriate
   server configuration. We deploy the system as we would on a ZFM site and
   transfer their existing data to the customer's system. This includes any
   configuration, like DNS, Apache, MariaDB, SSL, etc. The new system is tested
   and handed over to the customer. This service is charged out at an hourly
   rate.
4. The customer is given access to the git repository that contains the system
   code and detailed deployment instructions. They can clone the repository and
   create a new one if they want to modify the system. This service is provided
   free of charge.
5. Together with the customer we determine the desirable format for the data and
   then create an export in that format. This service is charged out at an
   hourly rate.
6. This is a simple consulting service that may be used in conjunction with any
   of the above options. It is charged out at an hourly rate.

### Planned Wind-up of ZFM

In the event that ZFM is discontinued, customers can avail themselves of the
options available for the Termination of a Customer Contract.

## Backups

A full recovery of a system is possible with only a database backup of the
customer's data by simply spinning up a new server, configuring it and restoring
the backed up data. Thus, we only concern ourselves with backing up user data.

### Process

#### Hosted database service

In cases where the system uses a AWS or similar service to house the customer,
simply contract for the database service that has sufficient resiliency for the
customer's needs.

#### Database manually configured

In cases where the ZFM server also hosts a database (that is, we install MariaDB
and per customer databases), we also are required to create scripts to bac the
database up. The installation manual contains detailed instructions on how to
configure the backup process and ensure that it restarts should the system
restart.

TODO: define process transfer backups to a geographically separate server and
delete as appropriate.

## System Restoration

### Non-Catastrophic Server Failure

A non-catastrophic server failure is defined as a production server failure in
which the media containing the operating system, the ZFM software or the
customer database is not damaged. As an example, a power outage may cause a
non-catastrophic server failure.

In this case service restoration is automatic and will happen as soon as the
server is restarted at the datacenter.

In general, the choice of provider determines the recovery time based on the
provider's terms of service.

#### Implementation Note:

The critical components of the system (Apache Server, MariaBD database and the
ZFM server software) are configured to start automatically on system restart.

### Catastrophic Server Failure

In a catastrophic system failure is any failure that is not non-catastrophic. A
catastrophic failure can be caused by fire, sever weather events, and possibly
by malicious damage to the system by a hacker or even a disgruntled employee.

The recover time for a catastrophic failure should be limited to one week after
the failure has been identified. In the case of intentional data disruption, it
may take some time before the failure is even identified. In practice, recovery
time from the event can be significantly shorter, once the problem is
identified.

#### Implementation Notes

##### Data Recovery Only

If the failure is limited to data, but the system is sound, the recovery
requires the last clean database backup to be restored.

##### Full System Recovery

If the full system fails, the recovery process is straight-forward. A new host
is spun up at the hosting provider of choice, the system is configured and the
customer's most recent database backup is restored. The code repository contains
detailed deployment instructions, so they do not need to be repeated here.

## Roles and Responsibilities

The technical team is responsible for implementing all aspects of this plan.
Contact:

Ted Moens - Technical Lead, Sole Proprietor  
P: 778.706-7178  
E: ted.moens@gmail.com  
E: zebrafishfacilitymanager@gmail.com  



