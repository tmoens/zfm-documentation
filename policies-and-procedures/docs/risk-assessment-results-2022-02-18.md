# Risk Assessment Results

Version 1.0

Issued: TBD

Last Updated and Approved 2022-02-18

## Purpose

Capture results of Risk Assessment

## Information Vulnerability

Overall comment: The ZFM system does not maintain any confidential or secret data.
It is limited to

- the zebrafish stocks belonging to a particular facility
- the transgenes those stocks carry
- the mutation those stocks carry
- the lineage of those stocks
- the tanks in the zebrafish facility
- a record of which stocks are in which tanks
- a record of the lineage of the stocks (stock 23 and stock 98 begat stocks 132 and 124)
- the users of the system with names and publicly known email addresses

The users of the system are not in fact concerned with the disclosure of this data
as it would not impact their work or reveal secrets about their research.

### Unauthorized access of ZFM system and data through the zfm-client
#### Likelihood of occurrence
Low.  The most likely way this could happen is by end users sharing their access
or using guessable passwords they have used elsewhere.
It could also happen if a third party gained access to an authorized user's computer
before the user's session expired.
#### Impact
None. Disclosure of ZFM data is not deemed a risk, nor likely to have any adverse impact.
#### Actions required
None.
#### Possible Mitigation
None planned.

### Unauthorized use or disclosure of ZFM system and data through the zfm-client
#### Likelihood of occurrence
Very Low. as it would first require access, which is very low.
#### Impact
None. Disclosure of AFM data is not deemed a risk, nor likely to have any adverse impact.
Work processes will not be affected at all.
#### Actions required
None.
#### Possible Mitigation
None planned.

### Unauthorized modification or destruction of ZFM system data through the zfm-client
#### Likelihood of occurrence
Very Low.  It would require access to the system which is very low.
It would also require access with an admin role to delete any data.
#### Impact
Medium: The impact could be significant if unauthorized access is malicious.
It may be difficult to detect and correct the changes although the system has
tools for auditing data and finding discrepancies.
#### Mitigation in place
- Assuming the malicious user gained access through the zfm-client at a user's
  workstation, the user will be forced to log in again at some point meaning that
  they cannot do a huge amount of damage.
- When malicious access is detected, the time of the login of the user can be
  found in the logs and the database can be restored to a checkpoint before the
  user's login.
- The system's Audit tool can help restore part of the data effectively.
#### Actions required
None.
#### Possible Mitigation
None considered or planned.

### Unauthorized modification or destruction of ZFM system data through zf-server host access
#### Likelihood of occurrence
Extremely low.  Logging in to the host is only possible via SSH with only the
ZFM developer (and an emergency backup) having the correct credentials.
Password based login is disabled on the host, so password guessing and poor
password selection will not introduce vulnerabilities.
#### Impact
Potentially Extreme. Even if a malicious user got access, destroyed the database,
and reformatted the disk, the system could quickly be reinstalled on another host
and restarted with a restored database from offsite storage.
However, the access from the host to the offsite storage could also be used by
the malicious users to erase the off-site storage.
#### Mitigation in place
- users are advised to download a copy of their data on a regular basis.
The system can be restored using that data.
#### Actions required
None.
#### Possible Mitigation
None considered or planned.

### Unauthorized access of ZFM system data through the server's API
The API is protected by the same controls that the zfm-client is.
Specifically a password is required to log in and every API call thereafter
requires authentication using a JWT Token.

## System Failure

Various system failure eventualities are covered in the Contingency plan.
