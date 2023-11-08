# Zebrafish Facility Manger Release History

Please note the history given here aligns with the features and functions 
committed to the ZFM code repository.
However, the release numbering given here prior to release 7.0 does not 
coincide with the release history in the code repository.

# Release 7.0

### Cross maker feature
Allows the user to create a new stock by selecting two stocks using the 
stock filter area.

### Stock Editor Re-write
Stock editor and creator now allows the user to do stock data, parentage, 
transgenes, mutations and swimmers all on one screen rather than as three 
separate operations.

### Multiple Marker Filtering
The user can now filter stocks for a conjunction of mutations and transgenes 
(formerly limited to one of each).

Update to Angular 16 and NestJS 10.

# Release 6.0 - skipped

## Release 5.1 April 2023

Major improvements to facility Audit tool.
Stock Walker fixes.
Optional feature to treat new stocks as alive whether they are in tanks or not.
Configuration switch added to ignore all tank related features.

# Release 5.0 March 2023

Upgrade to use NestJS 9.
Major changes for support of Angular 15.
Major changes for Typescript evolution and code cleanup.

## Release 4.2 Oct 2022

Support vertical label orientation.
Improve export audit report.
Update to Angular 14

## Release 4.1 Sept 2022

Overhaul label printing to make it easier to customize the label layout per 
facility.  Also, make it easy to modify label content before printing.

# Release 4.0 May 2022

Changes to keep up with newer versions of Angular and NestJS - the main 
underlying technologies.
Separation of all documentation to a different repository.

## Release 3.2 Feb 2022

Multiple minor user experience improvements.

## Release 3.1 Nov 2021

Add tool for generating tank records from a tank schema.  Speeds up onboarding.

# Release 3.0 Sept 2021

Outbound e-mail uses a more robust mail service.

## Release 2.6 - Sept 2021

Import from Excel to bring new facilities on board.
Ability to configure required password complexity for each facility.

## Release 2.5 - June 2021

## Stockbook Exporter

Allow users to export an entire stockbook to Excel.

## Documentation Upgrades

Add a description of the features and benefits of the system.

## Releases 2.1 - 2.4 April 2021

### Audit Tool

Using a phone only, make sure that the data in your system is in sync with
your fish facility.
Very fast and efficient update of the stocks and 
fish counts in tanks as you go from tank to tank.

### ZFIN Integration

When adding a mutation or transgene to the system, any alleles that are "known to
ZFIN" are recognized and user can import ZFIN information with a single click.

### Nursery census

The system now supports fish counts for a stock entering and leaving the nursery.
This will support nursery mortality reports and other animal
husbandry reports in the future.

### Data Importer

An importer feature was added to simplify the process of migrating existing
stockbooks to the Zebrafish Facility Manager system.

# Release 2.0. February 2021

### Stock Researchers and Primary Investigators Improved

Previously these were simple strings in the database.
They are now references to user object which means:

1. End users can no longer create multiple different strings for the same researcher
1. Researcher filters will produce much more reliable results
1. Stock editing will be simpler

### User Administration Improved

In order to support the stocks referring to users as PIs or researchers, users
can now be designated as either or both.  Only "active" users will show up on
the menu of researchers that can be assigned to a stock.

More advanced filtering has been implemented for user administration.

### Label Printing Improved

Label printing has been greatly improved. The user is now able to preview and edit the
label contents before printing. In particular:

1. Edit data for the label, removing redundant information and adding notes
1. Hide or show fields
1. Make minor adjustments to the font and font size

### Cross Label Feature

The system supports creating a label for a particular cross.
The cross label builder will automatically provide data from the researcher,
date and the parental stocks - but the user can override this data if desired.

### Mutation "researcher" field becomes "source"

This is in keeping with the general usage of the field to track from where the mutation
was acquired.

# Release 1.0 September 2020

This was the original release includes:

1. Stock Management
1. Mutation Management
1. Transgene Management
1. User Administration
1. Tank Label Printing
1. Excel reports
1. Tank Walker


