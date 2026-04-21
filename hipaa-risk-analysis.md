# HIPAA Risk Analysis

![Organisation](https://img.shields.io/badge/Organisation-CareLink%20Health-blue)
![Regulation](https://img.shields.io/badge/Regulation-HIPAA%20Security%20Rule-green)
![Required](https://img.shields.io/badge/Document-Required%20by%20Law-red)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

**Organisation:** CareLink Health
**Document:** HIPAA Security Rule — Required Risk Analysis
**Reference:** 45 CFR 164.308(a)(1)(ii)(A)
**Version:** 1.0
**Prepared By:** Privacy and Security Officer
**Date:** 2025

---

## Purpose

The HIPAA Security Rule requires all covered entities and business
associates to conduct an accurate and thorough assessment of the
potential risks and vulnerabilities to the confidentiality, integrity,
and availability of all electronic Protected Health Information (ePHI)
that the organisation creates, receives, maintains, or transmits.

This is a mandatory, required implementation specification. It is
not optional.

---

## Scope

This risk analysis covers all ePHI created, received, maintained,
or transmitted by CareLink Health including:

- Patient consultation recordings (video and audio)
- Electronic health records and clinical notes
- Prescription records
- Remote monitoring data (heart rate, blood pressure, glucose levels)
- Appointment and scheduling data
- Billing and insurance records
- Staff and administrative data with PHI

**Systems in scope:**
- CareLink telehealth platform (AWS-hosted)
- EHR system (MedRecord Systems — business associate)
- Video consultation platform (integrated with main platform)
- Billing and insurance processing (BillPro Health — business associate)
- Staff email system (used to communicate some patient information)
- Staff mobile devices (used for on-call consultation)

---

## Risk Assessment Methodology

**Threat identification:** Identify potential threats to ePHI from
environmental, human, and technical sources.

**Vulnerability identification:** Identify weaknesses in systems,
processes, or policies that could be exploited by threats.

**Likelihood rating:**
- High: The threat is likely to occur without the vulnerability
  being addressed
- Moderate: The threat may occur
- Low: The threat is unlikely to occur

**Impact rating:**
- High: Significant harm to patients, significant HIPAA penalties,
  major operational disruption
- Moderate: Limited patient harm, moderate penalties, some disruption
- Low: Minimal patient impact, minor regulatory exposure

---

## Risk Analysis Results

### Threat 1 — Ransomware Attack
**Likelihood:** High
**Impact:** High
**Risk Level:** CRITICAL

CareLink's telehealth platform hosts consultation recordings and PHI
for 25,000 patients. A ransomware attack could encrypt all patient
data, prevent clinical staff from accessing records during
consultations, and result in a reportable breach affecting all 25,000
patients. Healthcare organisations are the most targeted sector for
ransomware globally.

**Vulnerabilities identified:**
- No immutable backup copies maintained separately from main storage
- Staff security awareness training is inconsistent

**Required actions:**
- Implement immutable backup copies in a separate cloud region
- Launch mandatory security awareness training including ransomware
  recognition
- Test incident response plan for ransomware scenario

---

### Threat 2 — Unauthorised Access to Consultation Recordings
**Likelihood:** High
**Impact:** High
**Risk Level:** CRITICAL

Consultation recordings contain highly sensitive PHI including
discussions of mental health, sexual health, HIV status, and other
sensitive conditions. A breach could cause severe harm to patients.

**Vulnerabilities identified:**
- MFA not enforced for all accounts with access to recordings
- Access reviews not conducted on a regular schedule

**Required actions:**
- Enable MFA for all accounts with access to PHI immediately
- Conduct quarterly access reviews
- Implement role-based access — only the treating clinician should
  access a patient's recordings

---

### Threat 3 — Accidental PHI Disclosure via Email
**Likelihood:** High
**Impact:** Moderate
**Risk Level:** HIGH

Staff use email to communicate about patient appointments and
occasionally share clinical information. Email is not encrypted
and messages can be sent to the wrong recipient or intercepted.

**Vulnerabilities identified:**
- No policy prohibiting unencrypted PHI in email
- No email encryption solution deployed

**Required actions:**
- Write and enforce a policy requiring encrypted email for any
  message containing PHI
- Deploy an email encryption solution
- Train all staff on the policy within 30 days

---

### Threat 4 — Lost or Stolen Staff Mobile Device
**Likelihood:** Moderate
**Impact:** High
**Risk Level:** HIGH

Clinical staff use personal and company mobile phones for on-call
consultations and occasionally to access patient records. A lost
or stolen unencrypted device containing PHI is a reportable breach.

**Vulnerabilities identified:**
- Not all staff devices are enrolled in Mobile Device Management (MDM)
- No policy requiring encryption and remote wipe capability

**Required actions:**
- Enrol all devices used for clinical work in MDM
- Require full device encryption and screen lock
- Enable remote wipe capability for all enrolled devices

---

### Threat 5 — Business Associate Data Breach
**Likelihood:** Moderate
**Impact:** High
**Risk Level:** HIGH

CareLink shares PHI with three business associates. A breach at any
of them would be a reportable breach by CareLink regardless of which
party was responsible.

**Vulnerabilities identified:**
- BAAs are in place but vendor security assessments not conducted
- No annual review of business associate security posture

**Required actions:**
- Conduct annual security assessment of all business associates
- Include right-to-audit clause in all future BAAs
- Request SOC 2 reports from all business associates

---

## Risk Register Summary

| Risk | Level | Owner | Target Date |
|------|-------|-------|-------------|
| Ransomware attack | CRITICAL | Security Officer | 30 days |
| Unauthorised access to recordings | CRITICAL | Security Officer + IT | 30 days |
| Accidental email disclosure | HIGH | Security Officer | 60 days |
| Lost or stolen device | HIGH | IT Manager | 60 days |
| Business associate breach | HIGH | Privacy Officer | 90 days |
| Unencrypted PHI on personal devices | MODERATE | IT Manager | 60 days |
| Inadequate audit log review | MODERATE | IT Manager | 90 days |
| Insufficient breach notification procedures | MODERATE | Privacy Officer | 60 days |

---

## Required Review

This risk analysis must be reviewed and updated:
- At least annually
- When environmental or operational changes occur that may affect ePHI
- Following a security incident
- When new technology is implemented

**Next scheduled review:** 2026

---

*This document is part of a GRC portfolio project. All names,
data, and scenarios are fictional and used for learning and
career development purposes only.*

