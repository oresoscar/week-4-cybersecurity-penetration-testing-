<div align="center">

# 🛡️ Mediroza General Hospital
### Authorized Security Assessment · Networkwalks Week 4

**Black-Box Web Application Security | PDF Security Review | Evidence-Based Reporting**

<br/>

![Status](https://img.shields.io/badge/Report-Synthetic%20Training%20Example-7c3aed?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Tools](https://img.shields.io/badge/Tools-OWASP%20ZAP%20%7C%20ExifTool%20%7C%20qpdf-2563eb?style=for-the-badge)
![Scope](https://img.shields.io/badge/Scope-Authorization%20Required-0f766e?style=for-the-badge)

**Prepared by:** `[Your Name]`  
**Assessment window:** `[Insert actual dates]`  
**Version:** `1.0`

</div>

---

> [!IMPORTANT]
> **Training example — not verified findings.** This README is a professionally formatted report template. Any sample findings, evidence IDs, dates, and ratings are illustrative only. They do **not** assert that vulnerabilities exist on the live target. Replace placeholders only with evidence gathered within the written authorization. Do not include real patient records, credentials, employee salary details, or confidential shareholder information in this public repository.

## 📑 Contents

- [1. Executive Summary](#-1-executive-summary)
- [2. Assessment Objectives](#-2-assessment-objectives)
- [3. Scope and Rules of Engagement](#-3-scope-and-rules-of-engagement)
- [4. Assessment Environment and Tools](#-4-assessment-environment-and-tools)
- [5. Methodology](#-5-methodology)
- [6. M1 — Initial Access and Web Assessment](#-6-m1--initial-access-and-web-assessment)
- [7. M2 — PDF Encryption Analysis](#-7-m2--pdf-encryption-analysis)
- [8. M3 — Further Data Exposure Assessment](#-8-m3--further-data-exposure-assessment)
- [9. M4 — Reporting and Deliverables](#-9-m4--reporting-and-deliverables)
- [10. Findings Register](#-10-findings-register)
- [11. Risk Rating Method](#-11-risk-rating-method)
- [12. Remediation Roadmap](#-12-remediation-roadmap)
- [13. Evidence Handling](#-13-evidence-handling)
- [14. Limitations](#-14-limitations)
- [15. Conclusion](#-15-conclusion)
- [16. Repository Layout](#-16-repository-layout)
- [17. Reproducing the PDF Checks](#-17-reproducing-the-pdf-checks)
- [18. Responsible Testing](#-18-responsible-testing)
- [19. Final Submission Checklist](#-19-final-submission-checklist)

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
| Assessment dates | `[Insert actual dates]` |

The target URL is reproduced from the assignment. This README does not independently verify the domain's ownership, current availability, or authorization to test it.

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

### Results

**Actual result:** `[Insert observations supported by your ZAP evidence]`

No specific live-site vulnerability is asserted by this template. A scanner alert is an indication requiring interpretation; it is not automatically a confirmed vulnerability.

### Evidence checklist

- [ ] ZAP alert details recorded.
- [ ] Affected URL confirmed to be in scope.
- [ ] Supporting request/response reviewed.
- [ ] Alert validation status recorded.
- [ ] Screenshots redacted and stored safely.

## 🔐 7. M2 — PDF Encryption Analysis

### Objective

Inspect the properties and encryption configuration of approved PDF exercise files.

### Tools

- `pdfinfo`
- ExifTool
- `qpdf`

### Example inspection commands

```bash
pdfinfo sample.pdf
exiftool sample.pdf
qpdf --is-encrypted sample.pdf
qpdf --show-encryption sample.pdf
```

Replace `sample.pdf` with the actual filename of an approved exercise file.

### How to interpret the output

| Command | Purpose |
|---|---|
| `pdfinfo` | Displays document properties where available |
| `exiftool` | Displays available metadata fields |
| `qpdf --is-encrypted` | Checks whether a PDF is encrypted |
| `qpdf --show-encryption` | Displays available encryption details |

For `qpdf --is-encrypted`, exit status `0` indicates an encrypted PDF and exit status `2` indicates a PDF that is not encrypted. Other errors should be investigated and must not be automatically treated as either result.

Encryption status alone does not establish whether a document is secure. The sensitivity of its contents, encryption configuration, key handling, and access controls are also relevant.

### Results register

| File | Encryption status | Evidence reference | Conclusion |
|---|---|---|---|
| `[Approved PDF 1]` | `[Observed result]` | `[Evidence ID]` | `[Evidence-based conclusion]` |
| `[Approved PDF 2]` | `[Observed result]` | `[Evidence ID]` | `[Evidence-based conclusion]` |
| `[Approved PDF 3]` | `[Observed result]` | `[Evidence ID]` | `[Evidence-based conclusion]` |

These are placeholders. Enter actual filenames and observed results; do not assume all PDFs use the same encryption method.

### Evidence checklist

- [ ] PDF properties captured.
- [ ] Metadata output saved.
- [ ] Encryption output saved.
- [ ] File source and authorization recorded.
- [ ] Passwords and confidential document contents excluded from public evidence.

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

If a controlled exercise confirms exposure, record the file or resource identifier, access-control condition, potential impact, and a redacted evidence reference. Avoid reproducing real personal or financial details.

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

Do not label an unverified alert as a confirmed vulnerability. Mark tests that were not performed as **Not tested**.

## 📋 10. Findings Register

> [!NOTE]
> The entries below are **reporting examples only**, not actual findings about the target. Replace or remove them according to verified evidence.

### F-01 — Security Header Configuration Review

| Field | Value |
|---|---|
| Severity | Pending validation |
| Asset | `[Verified in-scope URL]` |
| Evidence ID | `[Evidence ID]` |
| Status | Illustrative example; not verified |

**Description:** In a hypothetical scenario, an HTTP response omits a security header that may be appropriate for the application.

**Potential impact:** The significance depends on the specific header, application behavior, and other controls. A missing header alone does not prove that exploitation is possible.

**Recommendation:** Review the application's requirements, configure applicable headers, and verify the response after remediation.

### F-02 — Passive Scanner Alert Requiring Validation

| Field | Value |
|---|---|
| Severity | Pending validation |
| Asset | `[Verified in-scope URL]` |
| Evidence ID | `[Evidence ID]` |
| Status | Unverified until supporting evidence is reviewed |

**Description:** A scanner alert requires manual review. The actual alert name and technical condition must be copied from the real tool output rather than invented.

**Validation steps:**

- Record the exact alert name, risk, confidence, and URL.
- Review the supporting request and response.
- Determine whether the reported condition is reproducible within scope.
- Consider whether the alert is a false positive.

**Recommendation:** Apply the remediation that corresponds to the actual validated issue and retest it after the fix.

### F-03 — PDF Metadata Review

| Field | Value |
|---|---|
| Severity | Informational unless impact is demonstrated |
| Asset | `[Approved exercise PDF]` |
| Evidence ID | `[Evidence ID]` |
| Status | Pending actual metadata review |

**Description:** Review metadata such as Author, Creator, Producer, and dates. These fields may reveal document workflow information, but their presence is not automatically a security vulnerability.

**Recommendation:** Remove unnecessary sensitive metadata before publishing the document and inspect it for unintended content.

### F-04 — Sensitive Document Exposure Assessment

| Field | Value |
|---|---|
| Severity | Not assigned without evidence |
| Asset | `[Authorized exercise resource]` |
| Evidence ID | `[Redacted evidence reference]` |
| Status | `[Confirmed / Not found / Not tested]` |

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

Ratings must be justified by the evidence. Scanner severity should be reviewed, not accepted automatically.

## 🛠️ 12. Remediation Roadmap

| Priority | Recommended action | Verification |
|---|---|---|
| 1 | Validate each scanner alert | Record evidence and validation outcome |
| 2 | Enforce server-side authorization for sensitive files | Test with authorized accounts and approved resources |
| 3 | Review published PDF metadata | Inspect sanitized copies |
| 4 | Apply relevant security-header/configuration fixes | Compare actual responses before and after |
| 5 | Protect evidence and report artifacts | Review for credentials and personal data |
| 6 | Retest confirmed findings | Record the retest date and outcome |

This is a suggested remediation workflow. Final priorities should reflect actual verified findings and the applicable risk matrix.

## 🧾 13. Evidence Handling

### Suggested evidence naming convention

```text
E-01-zap-alert-details.png
E-02-response-headers.txt
E-03-pdf-metadata.txt
E-04-pdf-encryption.txt
```

Use identifiers that correspond to the findings register. Store evidence securely and redact personal information before sharing.

### Example commands for approved PDF files

```bash
mkdir -p ~/mediroza-pentest/logs/m3

exiftool sample.pdf \
  > ~/mediroza-pentest/logs/m3/sample-metadata.txt

pdfinfo sample.pdf \
  > ~/mediroza-pentest/logs/m3/sample-properties.txt

qpdf --show-encryption sample.pdf \
  > ~/mediroza-pentest/logs/m3/sample-encryption.txt 2>&1
```

Replace `sample.pdf` with the actual approved exercise filename.

Do not commit confidential documents, passwords, tokens, patient data, private employee details, or confidential shareholder information to a public GitHub repository.

## ⚠️ 14. Limitations

- This README is a synthetic training template, not a verified report of live testing.
- No actual ZAP export or validated web vulnerability evidence is included here.
- No claim is made that confidential patient, employee, or shareholder information was retrieved.
- Results from sample PDFs do not establish the security status of real hospital documents.
- Passive inspection cannot prove the absence of all vulnerabilities.
- Findings must be updated to reflect tests actually completed within the written authorization.
- Any unperformed test must be recorded as **Not tested**, not as a successful or failed test.

## ✅ 15. Conclusion

This project presents a structured approach to authorized web application review, PDF metadata and encryption inspection, sensitive-document exposure assessment, and professional reporting.

A final assessment report should be reproducible, evidence-led, and clear about uncertainty. Confirmed findings must be supported by evidence; unverified observations must remain pending validation; and unperformed tests must be documented honestly.

## 📁 16. Repository Layout

```text
mediroza-pentest/
├── README.md
├── screenshots/
│   └── .gitkeep
├── logs/
│   ├── m2/
│   ├── m3/
│   └── .gitkeep
├── lab-pdfs/
│   └── .gitkeep
├── notes/
│   └── .gitkeep
└── report/
    └── final-report.md
```

This is a suggested layout. Only approved, non-confidential evidence should be committed.

## 🧪 17. Reproducing the PDF Checks

### Install tools on Kali Linux

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

Review the output, preserve the relevant evidence, and record only conclusions supported by the results.

## 🤝 18. Responsible Testing

This repository is intended for authorized educational security testing.

- Obtain and follow written authorization.
- Stay within the approved target and testing methods.
- Do not access confidential records without explicit authorization.
- Do not perform denial-of-service or out-of-scope testing.
- Protect evidence and redact sensitive content.
- Report verified vulnerabilities through the authorized reporting channel.
- Do not publish personal or confidential data in GitHub issues, commits, screenshots, or repository files.

## 🧩 19. Final Submission Checklist

- [ ] Replace `[Your Name]` and illustrative dates.
- [ ] Confirm the actual scope and written authorization.
- [ ] Add evidence from tests actually performed.
- [ ] Replace placeholders with observed results.
- [ ] Remove or clearly label synthetic findings.
- [ ] Record unperformed tests as **Not tested**.
- [ ] Ensure every confirmed finding has an evidence reference.
- [ ] Check all screenshots and logs for sensitive information.
- [ ] Confirm no confidential documents or credentials are committed.
- [ ] Update the report status to reflect the actual assessment.

---

<div align="center">

**Mediroza General Hospital — Networkwalks Week 4**

*Document carefully. Validate findings. Protect sensitive information.*

**Report status:** Synthetic training template until verified evidence is added.

</div>
