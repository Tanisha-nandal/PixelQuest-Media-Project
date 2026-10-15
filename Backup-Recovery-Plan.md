# Backup and Disaster Recovery Plan

## 1. Objective
Protect source code and media assets from accidental deletion, corruption, ransomware, unauthorized changes, and service disruption.

## 2. Backup Schedule
- Source code: remote Git history and an independent repository backup.
- Critical media assets: daily backup of new or modified assets.
- Complete media library: weekly backup.
- Approved releases: retain release tags and corresponding approved assets.
- Restoration testing: quarterly and after major infrastructure changes.

## 3. Security Controls
- Encrypt data in transit and at rest.
- Restrict access to backup administrators.
- Enable object versioning where supported.
- Keep an independent backup in a separate account or security boundary.
- Protect backup credentials from ordinary developer access.
- Monitor backup jobs and alert on failures.

## 4. Recovery Procedure
1. Identify the incident and stop further unauthorized changes.
2. Revoke compromised credentials where necessary.
3. Identify the latest known-good commit and asset versions.
4. Restore the required files to a clean environment.
5. Verify file integrity, access permissions, and application functionality.
6. Document the recovery results and corrective actions.

## 5. Recovery Targets
Proposed Recovery Point Objective (RPO): 24 hours for routine media changes.
Proposed Recovery Time Objective (RTO): 8 hours for critical project services.

These are planning targets, not measured guarantees.

## 6. Testing
Record each restoration test's date, data restored, recovery duration, result, and required improvements.
