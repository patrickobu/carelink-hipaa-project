# HIPAA Security Rule Gap Assessment

**Organisation:** CareLink Health
**Document:** Full gap assessment — all 75 Security Rule requirements
**Version:** 1.0
**Date:** 2025

## Assessment Summary

| Category | Requirements | Implemented | Partial | Gap |
|----------|-------------|------------|---------|-----|
| Administrative (45) | 45 | 18 (40%) | 14 (31%) | 13 (29%) |
| Physical (18) | 18 | 12 (67%) | 3 (17%) | 3 (17%) |
| Technical (12) | 12 | 6 (50%) | 4 (33%) | 2 (17%) |
| **Total (75)** | **75** | **36 (48%)** | **21 (28%)** | **18 (24%)** |

## Administrative Safeguards — Detail

| Requirement | Type | Status | Notes |
|-------------|------|--------|-------|
| Risk analysis | Required | GAP | Never formally conducted |
| Risk management | Required | Partial | Informal only |
| Sanction policy | Required | Implemented | HR policy in place |
| Information system activity review | Required | Partial | Logs exist but not reviewed |
| Assigned security responsibility | Required | Implemented | Privacy Officer appointed |
| Authorization and supervision | Addressable | Partial | No formal process |
| Workforce clearance procedure | Addressable | Partial | Inconsistent background checks |
| Termination procedures | Addressable | Implemented | IT off-boarding checklist exists |
| Access authorisation | Addressable | Partial | No formal approval process |
| Access establishment | Addressable | Partial | Role-based but not documented |
| Access modification | Addressable | Partial | Not consistently applied |
| Security reminders | Addressable | GAP | No formal programme |
| Protection from malicious software | Addressable | Implemented | Antivirus deployed |
| Log-in monitoring | Addressable | Partial | Logging exists, not monitored |
| Password management | Addressable | Partial | Policy exists but not enforced |
| Response and reporting | Required | Partial | Process exists but not tested |
| Testing | Addressable | GAP | No testing programme |
| BAA requirements | Required | Implemented | Three BAAs in place |

## Physical Safeguards — Detail

| Requirement | Type | Status | Notes |
|-------------|------|--------|-------|
| Facility access controls | Addressable | Implemented | Key fob access control |
| Contingency operations | Addressable | GAP | No formal BCP |
| Facility security plan | Addressable | Implemented | CCTV and access logs |
| Access control and validation | Addressable | Implemented | Visitor sign-in process |
| Maintenance records | Addressable | Implemented | IT maintenance log kept |
| Workstation use | Required | GAP | No formal policy written |
| Workstation security | Required | Partial | Some unlocked workstations observed |
| Device and media controls | Required | GAP | No disposal procedure |
| Disposal | Required | GAP | No documented secure disposal process |
| Media re-use | Addressable | Implemented | Devices wiped before re-issue |
| Accountability | Addressable | Implemented | Device register maintained |
| Data backup and storage | Addressable | Implemented | Cloud backup automatic |
| Movement of hardware | Addressable | Partial | No formal tracking process |

## Technical Safeguards — Detail

| Requirement | Type | Status | Notes |
|-------------|------|--------|-------|
| Unique user identification | Required | Implemented | Individual accounts for all staff |
| Emergency access | Required | Implemented | Break-glass procedure documented |
| Automatic logoff | Addressable | Partial | Not configured on all systems |
| Encryption and decryption | Addressable | Implemented | PHI encrypted at rest |
| Audit controls | Required | Partial | Logging enabled, not reviewed |
| Integrity controls | Addressable | Implemented | Data integrity checks in place |
| Authentication | Required | GAP | MFA not enabled for all accounts |
| Transmission security | Required | Implemented | TLS 1.2+ enforced |

## Priority Remediation Actions

### Immediate (High risk — within 30 days)
1. Enable MFA for all accounts accessing PHI
2. Document and conduct the required HIPAA risk analysis
3. Configure automatic session logoff on all PHI-access systems

### Short-term (within 90 days)
4. Write workstation use policy
5. Establish monthly audit log review
6. Write device disposal procedure
7. Launch security awareness training programme

### Medium-term (within 6 months)
8. Write and test Business Continuity Plan
9. Conduct annual tabletop exercise for breach scenario
10. Implement formal access review process
11. Write and test contingency plan
