<div align="center">

# 🛡️ Mediroza General Hospital
### Authorized Security Assessment · Networkwalks Week 4

**Black-Box Web Application Security | PDF Security Review | Evidence-Based Reporting**

<br/>

![Status](https://img.shields.io/badge/Report-Synthetic%20Training%20Example-7c3aed?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Tools](https://img.shields.io/badge/Tools-OWASP%20ZAP%20%7C%20ExifTool%20%7C%20qpdf-2563eb?style=for-the-badge)
![Scope](https://img.shields.io/badge/Scope-Authorization%20Required-0f766e?style=for-the-badge)

**Prepared by:** `ORES MWIJAGE OSCAR`  

</div>

---


## 🧭 1. Executive Summary

This project documents a structured security-assessment workflow based on the Networkwalks Week 4 exercise for Mediroza General Hospital. The assignment covers black-box web application review, passive security observations, PDF metadata and encryption inspection, assessment of potential sensitive-document exposure, and preparation of a professional report.

The assessment should be conducted only against the explicitly authorized target and approved exercise materials. The final report must distinguish confirmed findings from scanner alerts that have not been validated, observations with no demonstrated security impact, and tests that were not performed.

### Report status

| Item | Status |
|---|---|
| Report type | Synthetic training template |
| Live target independently verified | No |
| Confirmed vulnerabilities documented here | None |
| Actual ZAP evidence attached | No |
| Actual PDF exercise evidence attached | No |
| Confidential data accessed or reproduced | No claim made |

> **Interpretation:** This document demonstrates professional report structure. It is not evidence that a live penetration test has been completed or that the target has any particular security weakness.

## 🎯 2. Assessment Objectives

The objectives of the exercise are to:

1. Review public-facing application components within the authorized scope.
2. Observe permitted HTTP requests and responses.
3. Review OWASP ZAP alerts and validate them against supporting evidence.
4. Inspect metadata and encryption properties of designated PDF exercise files.
5. Assess potential exposure using only approved test materials.
6. Document findings, potential impact, and remediation recommendations.
7. Maintain a traceable evidence register and record testing limitations.
8. Produce a clear, reproducible, professional security report.

## 🗺️ 3. Scope and Rules of Engagement

### 3.1 Target information

| Field | Value |
|---|---|
| Organization named in the assignment | Mediroza General Hospital |
| Target supplied by the assignment | `https://medirozahospital.com` |
| Assessment approach | Black-box |
| Assessment focus | Web application and approved PDF exercise files |
| Authorization | Must be confirmed from the written rules of engagement |



### 3.2 In-scope activities

Only when explicitly permitted by the written authorization:

- Reviewing publicly accessible pages on the approved domain.
- Passively observing browser-visible HTTP requests and responses.
- Reviewing security-related HTTP headers.
- Reviewing scanner alerts and their supporting evidence.
- Inspecting designated PDF exercise files using document-analysis tools.
- Documenting verified observations and recommended fixes.

### 3.3 Exclusions and safety constraints

- No social engineering.
- No denial-of-service, stress, or load testing.
- No testing of unrelated domains or third-party systems.
- No unauthorized access to restricted resources.
- No retrieval or publication of real patient records.
- No collection or disclosure of real employee salary or shareholder information.
- No password recovery or access-control bypass against confidential real-world documents without explicit authorization for that exact activity.
- No publication of credentials, session tokens, personal information, or confidential evidence.

## 🧰 4. Assessment Environment and Tools

| Tool | Purpose | Evidence to retain |
|---|---|---|
| **Kali Linux** | Controlled assessment workstation | Environment notes |
| **OWASP ZAP** | Passive web observation and alert triage | Alert details and relevant request/response records |
| **Firefox Developer Tools** | Inspect browser-visible requests, responses, and headers | Redacted screenshots or notes |
| **ExifTool** | Inspect PDF metadata | Text output for approved sample files |
| **pdfinfo** | Inspect PDF document properties | Command output |
| **qpdf** | Inspect PDF encryption settings | Command output |
| **Git / GitHub** | Version control and report publication | Commit history; no confidential artifacts |

> Installation or execution of a tool is not proof of a completed security test. Each reported result must be supported by recorded output or other appropriate evidence.

## 🔬 5. Methodology

### Phase 1 — Preparation

1. Read the rules of engagement and confirm the approved target.
2. Identify prohibited actions and permitted test materials.
3. Create a dedicated workspace for notes, logs, screenshots, and reports.
4. Verify the required tools are installed.
5. Establish a consistent naming scheme for evidence.

### Phase 2 — Passive web assessment

1. Browse permitted public pages.
2. Observe requests and responses in OWASP ZAP.
3. Review each relevant alert's name, risk, confidence, URL, description, and solution.
4. Inspect the request/response evidence supporting the alert.
5. Record whether the issue was validated, remains unconfirmed, or was not tested.
6. Do not expand into intrusive testing unless specifically authorized.

### Phase 3 — PDF properties and encryption

1. Use designated, authorized exercise PDFs.
2. Inspect document properties and metadata.
3. Check encryption status and available encryption details.
4. Save command output as evidence.
5. Distinguish results from sample documents from any conclusions about actual hospital records.

### Phase 4 — Data exposure assessment

1. Review only approved exercise resources.
2. Determine whether evidence demonstrates unintended exposure.
3. Record the resource and access condition without copying unnecessary sensitive content.
4. Redact personal information from evidence.
5. If required materials are unavailable, record the test as **Not tested** rather than inventing a result.

### Phase 5 — Reporting and quality review

1. Consolidate the evidence register.
2. Validate each proposed finding.
3. Assess likelihood and impact using the supplied risk matrix where available.
4. Recommend practical remediation.
5. Record limitations and outstanding work.
6. Review the report and repository for confidential information before sharing.

## 🌐 6. M1 — Initial Access and Web Assessment

### Objective

Review permitted web entry points and identify potential security weaknesses through passive observation and evidence review.

### Activities

- Review public pages within scope.
- Observe permitted requests and responses in OWASP ZAP.
- Review the Sites, History, and Alerts panels.
- Record alert names, risk levels, confidence levels, and affected URLs.
- Inspect relevant response headers and supporting evidence.
- Capture appropriately redacted screenshots or records.



## 🔐 7. M2 — PDF Encryption Analysis

### Objective

Inspect the properties and encryption configuration of approved PDF exercise files.

### Tools

- `pdfinfo`
- ExifTool
- `qpdf`

### inspection commands

```bash
pdfinfo pformat.pdf
exiftool pformat.pdf
qpdf --is-encrypted pformart.pdf
qpdf --show-encryption pformat.pdf
```


### How to interpret the output

| Command | Purpose |
|---|---|
| `pdfinfo` | Displays document properties where available |
| `exiftool` | Displays available metadata fields |
| `qpdf --is-encrypted` | Checks whether a PDF is encrypted |
| `qpdf --show-encryption` | Displays available encryption details |

For `qpdf --is-encrypted`, exit status `0` indicates an encrypted PDF and exit status `2` indicates a PDF that is not encrypted. Other errors should be investigated and must not be automatically treated as either result.

Encryption status alone does not establish whether a document is secure. The sensitivity of its contents, encryption configuration, key handling, and access controls are also relevant.


## 🗂️ 8. M3 — Further Data Exposure Assessment

### Objective

Examine authorized exercise materials for unintended information exposure, including the categories identified in the assignment.

### Metadata fields to review

| Field | Possible significance |
|---|---|
| `Author` | May reveal an author's name |
| `Creator` | May identify the software used to create the document |
| `Producer` | May identify the software that generated the PDF |
| `CreateDate` | May reveal document creation time |
| `ModifyDate` | May reveal document modification time |
| `Title` / `Subject` | May disclose document purpose or subject |

The presence of metadata does not automatically establish a vulnerability. Risk depends on whether the information is sensitive, whether it was intended to be public, and what impact disclosure could have.

### Sensitive-document review

The assignment identifies employee salary information and shareholder details as areas to assess. This template does **not** claim that these data were discovered.

Record the outcome accurately:

- **Confirmed:** Authorized evidence demonstrates unintended exposure.
- **Not found:** The permitted test was completed, but no exposure was identified in the resources examined.
- **Not tested:** Required authorized files, access, or evidence were unavailable.


### Recommended controls

- Enforce authentication and server-side authorization for sensitive documents.
- Keep confidential documents outside public web directories where practical.
- Verify authorization on every request to a protected resource.
- Remove unnecessary sensitive metadata before publication.
- Review documents for hidden or unintended content before release.
- Review relevant access logs where authorized.
- Use least-privilege permissions and appropriate retention controls.

## 📝 9. M4 — Reporting and Deliverables

### Objective

Produce a professional report that clearly records the scope, methodology, findings, evidence, risk ratings, remediation recommendations, and limitations.

Each finding should include:

1. Finding ID and title.
2. Severity and validation status.
3. Affected asset.
4. Description of the observed condition.
5. Evidence reference.
6. Potential impact.
7. Conditions required for the issue to matter.
8. Recommended remediation.
9. Retest result, where applicable.



**Description:** In a hypothetical scenario, an HTTP response omits a security header that may be appropriate for the application.

**Potential impact:** The significance depends on the specific header, application behavior, and other controls. A missing header alone does not prove that exploitation is possible.

**Recommendation:** Review the application's requirements, configure applicable headers, and verify the response after remediation.

### F-02 — Passive Scanner Alert Requiring Validation


**Description:** A scanner alert requires manual review. The actual alert name and technical condition must be copied from the real tool output rather than invented.

**Validation steps:**

- Record the exact alert name, risk, confidence, and URL.
- Review the supporting request and response.
- Determine whether the reported condition is reproducible within scope.
- Consider whether the alert is a false positive.

**Recommendation:** Apply the remediation that corresponds to the actual validated issue and retest it after the fix.

### F-03 — PDF Metadata Review


**Description:** Review metadata such as Author, Creator, Producer, and dates. These fields may reveal document workflow information, but their presence is not automatically a security vulnerability.

**Recommendation:** Remove unnecessary sensitive metadata before publishing the document and inspect it for unintended content.

### F-04 — Sensitive Document Exposure Assessment


**Description:** Assess whether an approved exercise resource exposes information it should protect. Do not claim that patient, employee, or shareholder data was accessed unless authorized evidence establishes that fact.

**Recommendation:** Enforce server-side access control, restrict document access, remove unintended public copies where authorized, and review relevant logs.

## ⚖️ 11. Risk Rating Method

Use the risk matrix specified by the assignment or organization where one is provided. Otherwise, consider likelihood, required access, exposure, data sensitivity, and plausible impact.

| Rating | General interpretation |
|---|---|
| **Critical** | Verified issue with potentially severe consequences |
| **High** | Verified issue with substantial potential impact |
| **Medium** | Verified issue with meaningful but more limited impact |
| **Low** | Verified issue with limited impact |
| **Informational** | Observation without demonstrated security impact |
| **Pending validation** | Evidence is insufficient to assign a confirmed rating |



## 🛠️ 12. Remediation Roadmap

| Priority | Recommended action | Verification |
|---|---|---|
| 1 | Validate each scanner alert | Record evidence and validation outcome |
| 2 | Enforce server-side authorization for sensitive files | Test with authorized accounts and approved resources |
| 3 | Review published PDF metadata | Inspect sanitized copies |
| 4 | Apply relevant security-header/configuration fixes | Compare actual responses before and after |
| 5 | Protect evidence and report artifacts | Review for credentials and personal data |
| 6 | Retest confirmed findings | Record the retest date and outcome |


<div align="center">

**Mediroza General Hospital — Networkwalks Week 4**

*Document carefully. Validate findings. Protect sensitive information.*

**Report status:** Synthetic training template until verified evidence is added.

</div>
