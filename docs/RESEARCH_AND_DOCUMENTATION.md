# APAAR-Verify AI — Research & Documentation Index

> A central index of the research, reference material, working documents, and implementation notes associated with **APAAR-Verify AI**.
>
> **Index prepared:** 2 November 2026  
> **Primary repository:** [Balaji-P-A/APAAR-Verify-AI](https://github.com/Balaji-P-A/APAAR-Verify-AI)

---

## 1. Project overview

**APAAR-Verify AI** is a prototype for student-data management and verification in AICTE-approved institutions. The project explores how institutions can submit student records, validate APAAR identifiers, detect inconsistencies and potential duplicate enrolments, monitor approved intake, and provide controlled verification of academic records.

The repository contains three implementation areas:

| Component | Directory | Main technologies |
|---|---|---|
| Web application | [`frontend/`](../frontend/) | React, Vite, Tailwind CSS |
| Backend API | [`edusync/`](../edusync/) | Python, FastAPI, MongoDB |
| Android application | [`Acadentrix/`](../Acadentrix/) | Kotlin, Jetpack Compose, Room |

The repository README and architecture document are the primary sources for the current implementation scope and status. See [Project README](../README.md) and [Backend architecture](../edusync/docs/architecture.md).

## 2. Research areas covered

| Research area | What was explored | Related implementation/documentation |
|---|---|---|
| APAAR and academic identity | APAAR as a student academic identity; its relationship to academic records, ABC and DigiLocker | [APAAR validator](../edusync/app/services/apaar_validator.py), Android validation module in `Acadentrix/core/` |
| Institutional student-data management | Student-level data intake, institution records, programme information and batch uploads | [CSV ingestion](../edusync/app/services/csv_ingestion.py), [Upload page](../frontend/src/pages/UploadPage.jsx) |
| Data validation and anomaly detection | Invalid or missing identifiers, duplicate records, intake inconsistencies, date and category checks, and reviewable anomaly findings | [Anomaly engine](../edusync/app/services/anomaly_engine.py), Android `AnomalyEngine.kt` |
| Academic-record correction impact | Previewing the downstream effects of a proposed correction before applying it; preserving linked records for review | [Corrections service](../edusync/app/services/corrections.py), [Impact page](../frontend/src/pages/ImpactPage.jsx) |
| Privacy, consent and access control | Role-based access, consent-aware verification, limiting the information exposed to verifiers | [Consent policy](../edusync/app/services/consent_policy.py), [Security and RBAC](../edusync/app/core/rbac.py) |
| Verifiable credentials and QR | Signed records, QR payloads, expiring/revocable verification tokens and controlled public responses | [QR service](../edusync/app/services/qr.py), [Token API](../edusync/app/api/tokens.py), [Seal service](../edusync/app/services/seal.py) |
| Auditability and integrity | Traceable record changes and tamper-evident audit history | [Audit-chain service](../edusync/app/services/audit_chain.py) |
| Platform delivery | Web, backend and Android implementation; local setup, tests and deployment | [Backend guide](../edusync/README.md), [Android guide](../Acadentrix/README.md), [`docker-compose.yml`](../docker-compose.yml) |

## 3. Working project documents

| Document | Description | Link |
|---|---|---|
| APAAR-Verify AI working project document | Project research and planning document shared during project preparation | [Open Google Doc](https://docs.google.com/document/d/1e0dfJ36B0Bq8fWRm3JGJowPpWP-x6fzxYYEph6pf-K4/) |
| Project source repository | Main source code, configuration, tests and project documentation | [Open GitHub repository](https://github.com/Balaji-P-A/APAAR-Verify-AI) |
| Main project README | Project summary, modules, setup, deployment and implementation notes | [README.md](../README.md) |
| Backend README | Backend setup, configuration and API-related guidance | [edusync/README.md](../edusync/README.md) |
| Backend architecture | Backend design and architecture notes | [architecture.md](../edusync/docs/architecture.md) |
| Android README | Android application setup and technical details | [Acadentrix/README.md](../Acadentrix/README.md) |
| Rebranding notes | Product naming and internal-identifier decisions | [REBRANDING_NOTES.md](../REBRANDING_NOTES.md) |
| Translation guide | Supported locales and translation contribution/check process | [TRANSLATIONS.md](./TRANSLATIONS.md) |
| Brand guide | Product visual identity and brand assets | [BRAND_GUIDE.md](./assets/brand/BRAND_GUIDE.md) |
| Project landing page | Local HTML landing page for the project | [index.html](./index.html) |

## 4. Official background and policy references

These sources provide background on APAAR and the wider academic-record ecosystem. They are references for research; they do **not** mean this prototype is connected to or officially endorsed by the Government of India, APAAR, AICTE, ABC or DigiLocker.

| Reference | Relevance | Source |
|---|---|---|
| APAAR official portal | Official overview of APAAR, its purpose and student academic identity | [apaar.education.gov.in](https://apaar.education.gov.in/) |
| APAAR official FAQs | Explanations of APAAR, the 12-digit identifier, academic records and related processes | [APAAR FAQs](https://apaar.education.gov.in/faqs) |
| APAAR resources | Official brochures, process-flow material, FAQs and consent-related resources | [APAAR Resources](https://apaar.education.gov.in/resource) |
| AICTE Approval Process Handbook 2024–2027 | AICTE approval-process reference material; check for later amendments or notices before relying on a particular provision | [Official AICTE PDF](https://www.aicte.gov.in/sites/default/files/APH%20Final.pdf) |

## 5. Competition and problem-statement research

### 5.1 Smart India Hackathon — SIH 2026, Problem Statement 26263

**Topic:** Development of an APAAR ID-Based Student Data Management and Verification Platform for AICTE-Approved Institutions.  
**Organisation shown in the problem-statement listing:** AICTE.  
**Theme shown in the listing:** Smart Automation.

This is the directly related problem-statement research for APAAR-Verify AI. The requirements described in the public listing include institution data submission, APAAR-based student identification, validation, duplicate and intake checks, dashboards, authorized verification, interoperability, privacy controls and reporting.

- [SIH 26263 — public problem-statement reference](https://zaidsayyed.in/tools/sih-problem-statements/sih26263) — **secondary listing**, not the official SIH portal. Confirm the final wording and status against the official SIH portal or the competition material supplied to the team before using it in a formal submission.
- [Smart India Hackathon official portal](https://sih.gov.in/) — use this for official competition notices and submission information.

### 5.2 Seva First Innovation Challenge 2026

The SEVA First material was reviewed as part of comparing competition fit and preparing application material. Keep the specific guideline/overview document supplied to the team with the submission records; a conversation-uploaded copy is not automatically included in this Git repository.

- [SEVA First Innovation Challenge — official portal](https://sevafirst.mic.gov.in/)
- [Challenge timeline](https://sevafirst.mic.gov.in/timeline)
- [Innovation tracks and evaluation criteria](https://sevafirst.mic.gov.in/tracks)

**Local working reference:** `Seva-First Innovatio Challenge (1).docx` (uploaded/shared during application preparation). To version it with this repository, place an approved copy under `docs/references/` and add its relative link here. Check the document's sharing and redistribution permissions before committing it.

### 5.3 Separate research item — SIH 2026, Problem Statement 26227

**Topic:** Semantic Retrieval and Multi-Temporal Change Analysis of Satellite Imagery (Ministry of Defence / Indian Army, as shown in the public listing).

This is a separate satellite-imagery research direction associated with the TerraLens AI concept. It is included here only as a cross-project reference because it was reviewed alongside APAAR-related competition options. It is **not** part of the APAAR-Verify AI product scope.

- [SIH 26227 — public problem-statement reference](https://sih2026.vuce.in/ps/SIH26227) — public listing; confirm official wording and requirements through the official SIH materials.

## 6. Current project scope and important limitations

Use the repository documentation and code as the source of truth for implementation status. In particular:

- APAAR-Verify AI is a **prototype**. Its verification flow checks records held by this prototype; it is not an official APAAR or AICTE verification service.
- The Android application is documented as offline-first and currently not synchronized with the web backend. Do not describe Android-to-server synchronization as implemented until that integration is completed and tested.
- Do not commit real student records, APAAR IDs, Aadhaar data, credentials, API keys, database connection strings, OAuth secrets or production `.env` files.
- Use synthetic/demo data in screenshots, sample files and public demonstrations.
- Treat policy thresholds, regulatory rules and competition requirements as versioned references. Verify the current official source before claiming that a rule is mandatory or up to date.

## 7. Suggested structure for adding future research files

Store approved research and submission documents in a clearly named folder, for example:

```text
docs/
├── RESEARCH_AND_DOCUMENTATION.md
├── research/
│   ├── APAAR-and-academic-identity.md
│   ├── AICTE-requirements.md
│   ├── privacy-and-consent.md
│   └── verification-and-audit-design.md
└── references/
    ├── README.md
    └── (approved source documents and competition material)
```

For each new item, record its title, author/issuing organisation, date, source URL or repository path, why it was reviewed, and whether it is an official source, a secondary source, or a team-created document.

## 8. Source and document register — add future items here

| Date | Document / research item | Type | Link or repository path | Notes |
|---|---|---|---|---|
|  | APAAR-Verify AI synopsis / proposal | Team document | Add link | Add the final submitted version, if shareable |
|  | SIH 26263 presentation / submission | Competition document | Add link | Add final submitted PPT/PDF, if shareable |
|  | Research papers / articles | Research | Add DOI or URL | Record author and publication year |
|  | Demo screenshots / evaluation evidence | Project evidence | Add repository path | Use synthetic data and remove secrets |

---

*This index is a navigation page, not a substitute for the original source documents. Public-source links should be rechecked before formal competition, policy, academic or regulatory use.*
