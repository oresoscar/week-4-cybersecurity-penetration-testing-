
# Mediroza General Hospital — Penetration Testing Report

> **Project:** Networkwalks Week 4 Penetration Testing Exercise  
> **Assessment Type:** Black-Box Web Application Security Assessment  
> **Target:** `https://medirozahospital.com`  
> **Report Status:** Training Report — Synthetic Example  
> **Prepared by:** [Your Name]  
> **Assessment Period:** 28 September – 2 October 2026 *(illustrative dates)*

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Scope and Rules of Engagement](#3-scope-and-rules-of-engagement)
4. [Tools and Technologies](#4-tools-and-technologies)
5. [Methodology](#5-methodology)
6. [Milestone 1 — Initial Access and Web Assessment](#6-milestone-1--initial-access-and-web-assessment)
7. [Milestone 2 — PDF Encryption Analysis](#7-milestone-2--pdf-encryption-analysis)
8. [Milestone 3 — Further Data Exposure Assessment](#8-milestone-3--further-data-exposure-assessment)
9. [Milestone 4 — Professional Reporting](#9-milestone-4--professional-reporting)
10. [Illustrative Findings](#10-illustrative-findings)
11. [Risk Rating Methodology](#11-risk-rating-methodology)
12. [Remediation Recommendations](#12-remediation-recommendations)
13. [Evidence Management](#13-evidence-management)
14. [Limitations](#14-limitations)
15. [Conclusion](#15-conclusion)
16. [Repository Structure](#16-repository-structure)
17. [How to Reproduce the PDF Checks](#17-how-to-reproduce-the-pdf-checks)
18. [Ethical and Legal Considerations](#18-ethical-and-legal-considerations)

---

## 1. Project Overview

This repository documents a structured penetration-testing training exercise based on the Networkwalks Week 4 assignment for Mediroza General Hospital.

The exercise covers black-box web application assessment, passive security observation, PDF document metadata inspection, PDF encryption analysis, sensitive-document exposure assessment, and professional report preparation.

The objective is to demonstrate a repeatable, evidence-based security assessment workflow while respecting the approved scope and protecting confidential information.

> **Important:** This README is a synthetic training example. No claim is made that the listed illustrative findings exist on the live target. Replace examples with verified observations before presenting this as a completed assessment.

## 2. Objectives

The objectives of the exercise are to:

- Review publicly accessible web application components within the authorized scope.
- Identify and document potential web security weaknesses.
- Inspect HTTP requests, responses, and relevant security headers.
- Review security scanner alerts and validate them against evidence.
- Examine metadata and encryption properties of approved PDF exercise files.
- Assess whether authorized test materials expose sensitive information.
- Assign evidence-based risk ratings.
- Recommend practical remediation measures.
- Produce a professional penetration-testing report.

## 3. Scope and Rules of Engagement

### 3.1 Target

| Item | Description |
|---|---|
| Organization named in assignment | Mediroza General Hospital |
| Target domain | `https://medirozahospital.com` |
| Assessment approach | Black-box |
| Assessment type | Web application security assessment |
| Authorization | Must be verified against the written rules of engagement |

The domain above is taken from the assignment. This README does not independently verify ownership, current availability, or authorization to test the live website.

### 3.2 In Scope

Subject to the written authorization:

- Publicly accessible pages on the approved domain.
- Passive inspection of browser-visible HTTP requests and responses.
- Review of security-related HTTP headers.
- Review of OWASP ZAP alerts.
- Metadata and encryption checks on designated PDF exercise files.
- Documentation of verified findings and limitations.

### 3.3 Out of Scope

The exercise must not exceed its written authorization. The following restrictions apply:

- Social engineering.
- Denial-of-service or load testing.
- Testing unrelated domains or third-party infrastructure.
- Unauthorized access to restricted resources.
- Retrieval, publication, or unnecessary handling of real patient records.
- Collection or disclosure of real employee salary or shareholder information.
- Password recovery or access-control bypass against real confidential documents without explicit authorization for that exact activity.

## 4. Tools and Technologies

| Tool | Purpose |
|---|---|
| OWASP ZAP | Passive web application inspection and security alert review |
| Firefox Developer Tools | Review browser requests, responses, and headers |
| ExifTool | PDF metadata inspection |
| `pdfinfo` | PDF document properties |
| `qpdf` | PDF encryption inspection |
| Kali Linux | Assessment environment |
| Markdown | Report documentation |
| Git and GitHub | Version control and report publication |

Tool installation does not, by itself, prove that a test was completed successfully. Record the actual tool output and status in the evidence log.

## 5. Methodology

The assessment follows a structured workflow.

### Phase 1: Preparation

1. Review the written authorization.
2. Confirm the target domain and exclusions.
3. Create a dedicated workspace.
4. Prepare an evidence log and screenshot directory.
5. Verify that required tools are installed.

### Phase 2: Passive Web Assessment

1. Open the authorized public website.
2. Observe permitted browsing activity through OWASP ZAP.
3. Review alerts, risk levels, confidence levels, and affected URLs.
4. Inspect supporting request and response evidence.
5. Record unverified alerts as pending validation.
6. Avoid intrusive tests that are not explicitly authorized.

### Phase 3: PDF Inspection

1. Use approved exercise PDF files.
2. Inspect document properties.
3. Extract available metadata.
4. Check whether the files are encrypted.
5. Record results without exposing confidential document contents.
6. Distinguish sample-file results from findings about the live target.

### Phase 4: Data Exposure Assessment

1. Review only approved exercise resources.
2. Determine whether evidence demonstrates unintended exposure.
3. Record the affected resource and access condition.
4. Redact personal or confidential information from evidence.
5. Do not claim successful discovery when the relevant files or evidence were not provided.

### Phase 5: Reporting

1. Consolidate evidence.
2. Validate findings.
3. Assess potential impact and likelihood.
4. Assign risk ratings.
5. Recommend remediation.
6. Record limitations and tests not performed.

## 6. Milestone 1 — Initial Access and Web Assessment

### Objective

Review permitted web application entry points and identify potential security weaknesses using passive inspection and evidence review.

### Tool

OWASP ZAP.

### Activities

- Browse permitted public pages.
- Review the ZAP Sites and History panels.
- Inspect alerts and their descriptions.
- Record affected URLs and risk/confidence values.
- Review relevant HTTP response headers.
- Capture screenshots or export evidence where permitted.

### Results

**Actual result:** To be completed from the real assessment evidence.

Do not invent alert names, affected URLs, server responses, or successful access. A scanner alert should not be classified as a confirmed vulnerability until the underlying condition is validated.

### Evidence to attach

- ZAP alert screenshots.
- Relevant request and response records.
- Security-header observations.
- Notes explaining validation and limitations.

## 7. Milestone 2 — PDF Encryption Analysis

### Objective

Inspect the encryption properties of authorized PDF exercise files and document the results.

### Tools

- `pdfinfo`
- ExifTool
- `qpdf`

### Example Commands

```bash
pdfinfo sample.pdf
exiftool sample.pdf
qpdf --is-encrypted sample.pdf
qpdf --show-encryption sample.pdf
```

Replace `sample.pdf` with the name of an approved exercise file.

### Interpretation

- `pdfinfo` displays document properties where available.
- ExifTool displays metadata fields embedded in the document.
- `qpdf --is-encrypted` checks whether a PDF is encrypted.
- `qpdf --show-encryption` displays available encryption details.

For `qpdf --is-encrypted`, an exit status of `0` indicates that the PDF is encrypted, while `2` indicates that it is not encrypted. Other errors should be investigated rather than automatically interpreted as either result.

Encryption alone does not prove that a document is secure or insecure. Security also depends on the sensitivity of its contents, access controls, and the encryption configuration.

### Results

| File | Encryption Status | Evidence | Conclusion |
|---|---|---|---|
| `lab-report-1.pdf` | Pending actual output | To be attached | Not yet established |
| `lab-report-2.pdf` | Pending actual output | To be attached | Not yet established |
| `lab-report-3.pdf` | Pending actual output | To be attached | Not yet established |

These filenames are placeholders. Replace them with the actual approved exercise filenames and observed results.

### Evidence to attach

- PDF properties output.
- Metadata output.
- Encryption inspection output.
- Notes describing any limitations.

## 8. Milestone 3 — Further Data Exposure Assessment

### Objective

Examine authorized exercise materials for unintended exposure of sensitive document information, including the categories specified in the assignment.

### Areas of Review

- Document metadata.
- Document properties.
- Unnecessary author or workflow information.
- Access controls around sensitive documents.
- Evidence of unintended exposure in approved test resources.

### Metadata Fields

| Field | Potential significance |
|---|---|
| `Author` | May disclose a document author's name |
| `Creator` | May identify software used to create a document |
| `Producer` | May identify software used to generate a PDF |
| `CreateDate` | May reveal when a document was created |
| `ModifyDate` | May reveal when a document was modified |
| `Title` | May disclose document subject or purpose |

Metadata is not automatically a vulnerability. Its risk depends on whether the information is sensitive and whether disclosure creates a meaningful security or privacy impact.

### Sensitive Information Assessment

The assignment refers to employee salary information and shareholder details. This README does not claim that either category was discovered.

Record the actual outcome as one of the following:

- **Confirmed:** Authorized evidence establishes unintended exposure.
- **Not found:** The permitted test was performed, but no exposure was identified in the resources examined.
- **Not tested:** Required authorized materials or access were unavailable.

### Recommended Controls

- Apply server-side authorization to sensitive documents.
- Keep confidential documents outside public web directories where practical.
- Require authentication and verify authorization on every sensitive-document request.
- Remove unnecessary sensitive metadata before publishing files.
- Review document contents for hidden or unintended information.
- Review access logs where authorized.
- Avoid including personal data in screenshots or reports.

## 9. Milestone 4 — Professional Reporting

### Objective

Produce a report that documents scope, methodology, findings, evidence, risk ratings, remediation, and limitations.

Each finding should contain:

1. Finding identifier.
2. Title.
3. Severity.
4. Affected asset.
5. Description.
6. Evidence.
7. Potential impact.
8. Validation status.
9. Remediation recommendation.
10. Retest result, if applicable.

A finding must be traceable to evidence. Unverified alerts and unperformed tests must be clearly identified.

## 10. Illustrative Findings

> **All examples in this section are fictional. They are included to demonstrate report formatting and must not be presented as actual findings about Mediroza General Hospital.**

### F-01 — Security Header Configuration Review

| Field | Illustrative value |
|---|---|
| Severity | Low — provisional |
| Asset | Placeholder public page |
| Evidence ID | SYNTHETIC-E01 |
| Status | Not verified on the live target |

**Description:** In a hypothetical scenario, a response is found to omit a recommended security header.

**Potential impact:** The impact depends on the specific header, application behavior, and surrounding security controls. An omitted header alone does not establish that exploitation is possible.

**Recommendation:** Review applicable security headers, configure them according to the application's security requirements, and verify the response after remediation.

### F-02 — Scanner Alert Requiring Validation

| Field | Illustrative value |
|---|---|
| Severity | Pending validation |
| Asset | Placeholder |
| Evidence ID | SYNTHETIC-E02 |
| Status | Unverified example |

**Description:** A hypothetical scanner alert requires manual review. No actual alert output has been supplied for this report.

**Validation requirements:**

- Record the exact alert name and risk level.
- Review the supporting request and response.
- Determine whether the condition is reproducible.
- Check whether the alert is a false positive.

**Recommendation:** Apply the remediation appropriate to the actual validated issue. Do not assign a confirmed vulnerability rating based solely on an unverified alert.

### F-03 — PDF Metadata Review

| Field | Illustrative value |
|---|---|
| Severity | Informational |
| Asset | Placeholder exercise PDF |
| Evidence ID | SYNTHETIC-E03 |
| Status | Example only |

**Description:** A hypothetical document contains standard metadata such as Author, Creator, Producer, or dates.

**Potential impact:** Metadata may disclose unnecessary document workflow information. The presence of metadata does not automatically represent a vulnerability.

**Recommendation:** Remove metadata that is unnecessary or sensitive before publishing the document, and review the file for unintended content.

### F-04 — Sensitive Document Exposure

| Field | Value |
|---|---|
| Severity | Not assigned |
| Asset | To be determined from authorized evidence |
| Evidence ID | Not available |
| Status | Not established |

**Description:** The assignment requires an assessment of whether designated materials expose sensitive employee or shareholder information. No successful discovery is claimed in this synthetic report.

**Recommendation:** Verify access controls on approved test resources, restrict access to confidential documents, and record only the minimum evidence required to demonstrate an authorized finding.

## 11. Risk Rating Methodology

Use the organization's approved risk matrix when available. Otherwise, consider likelihood, required access, exposure, data sensitivity, and potential impact.

| Rating | General meaning |
|---|---|
| Critical | Verified issue with potentially severe consequences |
| High | Verified issue with substantial impact |
| Medium | Verified issue with meaningful but more limited impact |
| Low | Verified issue with limited impact |
| Informational | Observation without demonstrated security impact |
| Pending validation | Evidence is insufficient to assign a confirmed rating |

Risk ratings should reflect the evidence and realistic impact. Scanner severity should be reviewed rather than accepted automatically.

## 12. Remediation Recommendations

### Application Security

- Validate scanner alerts before assigning final severity.
- Review security headers and server configuration.
- Follow secure development and deployment practices.
- Retest confirmed findings after remediation.

### Document Security

- Enforce authentication and server-side authorization.
- Avoid exposing confidential files through public URLs.
- Remove unnecessary sensitive metadata.
- Apply appropriate encryption to confidential documents.
- Protect backups and document storage.
- Use least-privilege access controls.

### Evidence and Reporting

- Maintain a record of commands, dates, and observed results.
- Protect screenshots and logs.
- Redact personal or confidential information.
- Distinguish verified findings from assumptions.
- Document tests that were not performed.

## 13. Evidence Management

Suggested evidence directory structure:

```text
mediroza-pentest/
├── README.md
├── screenshots/
├── logs/
│   └── m3/
├── lab-pdfs/
├── notes/
└── report/
    └── final-report.md
```

Example commands for saving local PDF inspection output:

```bash
mkdir -p ~/mediroza-pentest/logs/m3

exiftool sample.pdf \
  > ~/mediroza-pentest/logs/m3/sample-metadata.txt

pdfinfo sample.pdf \
  > ~/mediroza-pentest/logs/m3/sample-properties.txt

qpdf --show-encryption sample.pdf \
  > ~/mediroza-pentest/logs/m3/sample-encryption.txt 2>&1
```

Use these commands only with files you are authorized to inspect. Replace the sample filename with the actual exercise filename.

Do not upload real patient records, passwords, authentication tokens, private employee information, or confidential shareholder documents to a public repository.

## 14. Limitations

- This repository README is a synthetic training example, not a record of verified live testing.
- No actual ZAP alert export or validated web vulnerability evidence is included.
- No claim is made that confidential patient, employee, or shareholder information was retrieved.
- Sample PDF results cannot establish the security status of actual hospital documents.
- Passive inspection cannot prove the absence of all vulnerabilities.
- Findings must be updated to reflect the tests actually performed within the authorized scope.

## 15. Conclusion

This project demonstrates a structured approach to web security assessment, PDF metadata and encryption inspection, sensitive-document exposure review, and professional reporting.

The final report should contain only findings supported by evidence collected during the authorized exercise. Unverified observations must remain pending validation, and unperformed tests must be recorded as not tested.

## 16. Repository Structure

```text
mediroza-pentest/
├── README.md
├── screenshots/
│   └── .gitkeep
├── logs/
│   └── .gitkeep
├── lab-pdfs/
│   └── .gitkeep
├── notes/
│   └── .gitkeep
└── report/
    └── final-report.md
```

This is a suggested structure. Store only approved, non-confidential evidence in the repository.

## 17. How to Reproduce the PDF Checks

### Install the tools on Kali Linux

```bash
sudo apt update
sudo apt install qpdf poppler-utils exiftool
```

### Verify installation

```bash
qpdf --version
pdfinfo -v
exiftool -ver
```

### Inspect an authorized exercise PDF

```bash
pdfinfo sample.pdf
exiftool sample.pdf
qpdf --is-encrypted sample.pdf
qpdf --show-encryption sample.pdf
```

Review the output, record the actual result, and include only evidence that is appropriate to share.

## 18. Ethical and Legal Considerations

This project is intended for authorized educational security testing.

- Obtain and follow written authorization.
- Stay within the approved target and testing methods.
- Do not attempt to access real confidential records without explicit authorization.
- Do not disrupt services or perform denial-of-service testing.
- Protect all collected evidence.
- Redact confidential information before sharing reports.
- Report vulnerabilities responsibly to the authorized contact.

---

## Report Status

**Current status:** Synthetic training example; actual findings are not established.

**Before submission:**
- [ ] Replace the student name and illustrative dates.
- [ ] Confirm the actual scope and authorization.
- [ ] Add verified evidence from the assessment.
- [ ] Replace placeholder results with observed results.
- [ ] Remove or clearly label all synthetic findings.
- [ ] Check the repository for confidential data.
- [ ] Update the report status accurately.

**End of README**
