# Smart India Hackathon (SIH) — Research & Documentation Index

> **Purpose:** A central index of the SIH problem statements, research directions, reference portals, and working documents reviewed for the team's hackathon preparation.
>
> **Last reviewed:** 02 November 2026  
> **Competition cycle:** Smart India Hackathon 2026

---

## 1. SIH 2026 official resources

| Resource | Link | Use |
|---|---|---|
| SIH official website | [sih.gov.in](https://sih.gov.in/) | Official notices, announcements and event information |
| SIH 2026 problem statements | [Official problem-statement portal](https://sih.gov.in/sih2026PS) | Confirm the official problem statement ID, title, sponsoring organisation and latest details |
| SIH 2026 idea-presentation format | [Official PPT template](https://sih.gov.in/letters/2026/SIH2026-IDEA-Presentation-Format.pptx) | Required presentation structure; check the current portal for any revised template |
| SIH 2026 problem statement archive | [SIH 2026 statement browser](https://sih2026.vuce.in/) | Convenient search and reference across problem statements; community-maintained, not an official SIH site |

**Source note:** Use the SIH portal and official notices as the authority for submission rules, deadlines and final problem-statement wording. Community-maintained statement browsers are secondary references and should be cross-checked against the official portal.

---

## 2. Problem statements researched

### 2.1 SIH26227 — Semantic Retrieval and Multi-Temporal Change Analysis of Satellite Imagery

| Field | Details |
|---|---|
| Problem statement ID | `SIH26227` |
| Organisation | Ministry of Defence (MoD) |
| Department | Indian Army (DGIS) |
| Category / theme | Software / Space Technology |
| SIH 2026 deadline shown in the statement archive | 30 September 2026 |
| Research / project direction | **TerraLens AI** — semantic satellite-imagery retrieval and multi-temporal land/change analysis |
| Statement reference | [Open SIH26227 statement](https://sih2026.vuce.in/ps/SIH26227) |

**Problem areas to address**

- **Semantic and multimodal retrieval:** Search satellite-image tiles using natural-language descriptions and image-to-image similarity, with spatial, date and sensor filters.
- **Multi-temporal change analysis:** Identify appearance, disappearance, expansion or contraction of features and classify supported changes such as construction, clearance, water-extent variation and road development.
- **False-alarm suppression:** Account for seasonality, illumination, viewing geometry, cloud, haze, snow, shadows, radiometric differences and image-registration errors.
- **Discovery and clustering:** Group visually or semantically similar locations so analysts can discover comparable sites.
- **Analyst review and provenance:** Present ranked candidates with before/after evidence, location, acquisition time, sensor/source, confidence and processing history; retain analyst decisions.
- **Incremental ingestion and on-premises operation:** Add new imagery without rebuilding the entire index and support operation without cloud services or external APIs during evaluation.

**Important constraints and expected evidence**

- Stage approved models, libraries, datasets and model weights before the network-disabled demonstration.
- Preserve georeferencing and acquisition metadata; support organiser-defined formats such as GeoTIFF and Cloud Optimized GeoTIFF (COG).
- Use publicly available or organiser-provided imagery only. Do not use classified, operational or service-generated imagery.
- Prepare source code, an architecture note, index-build and incremental-ingestion instructions, model/dataset provenance, and a reproducible evaluation report.
- The evaluation report should record the indexed area, number of scenes/tiles, index build time, storage footprint, query latency and hardware used.

**Research themes / implementation notes**

| Area | Questions to investigate |
|---|---|
| Data ingestion | How will Sentinel/Landsat or other approved public scenes be downloaded, tiled, georeferenced, quality-filtered and incrementally indexed? |
| Embeddings | Which vision-language or remote-sensing embedding model supports the target imagery and can be packaged for offline inference? |
| Search | Which vector index and metadata filters provide useful ranked retrieval with measurable latency? |
| Change detection | Which methods distinguish real changes from seasonal, atmospheric, illumination and registration artefacts? |
| Provenance | How will every result retain scene ID, sensor, acquisition date, tile coordinates, preprocessing version and model version? |
| Offline deployment | Can the complete pipeline run locally after all required assets have been staged? |
| Evaluation | What held-out text queries, relevance judgements and labelled change/no-change samples will be used? |

**Public Earth-observation reference portals**

- [Copernicus Data Space Ecosystem](https://dataspace.copernicus.eu/) — access point for Copernicus Earth-observation data.
- [ESA Sentinel-1](https://www.esa.int/Applications/Observing_the_Earth/Copernicus/Sentinel-1) — radar Earth-observation mission reference.
- [ESA Sentinel-2](https://www.esa.int/Applications/Observing_the_Earth/Copernicus/Sentinel-2) — optical multispectral Earth-observation mission reference.
- [USGS Landsat Missions](https://www.usgs.gov/landsat-missions) — Landsat programme and data reference.
- [ISRO Bhuvan](https://bhuvan.nrsc.gov.in/) — Indian geospatial visualisation and data portal.

Check each provider's current access conditions, attribution requirements and dataset licence before using imagery in a submission or public demonstration.

---

### 2.2 SIH26068 — WeatherGPT: Conversational AI for Weather Forecasting, Alerts, and Climate Information

| Field | Details |
|---|---|
| Problem statement ID | `SIH26068` |
| Organisation | Ministry of Earth Sciences (MoES) |
| Department | India Meteorological Department (IMD) |
| Category / theme | Software / Disaster Management |
| SIH 2026 deadline shown in the statement archive | 20 September 2026 |
| Research direction | Conversational, multilingual weather intelligence and decision support |
| Statement reference | [Open SIH26068 statement](https://sih2026.ankus.dev/en/ps/SIH26068) |

**Problem areas to address**

- Real-time weather information retrieval and natural-language forecast queries.
- Integration with numerical weather prediction (NWP) models and meteorological data sources.
- Extreme-weather alerts and early-warning dissemination.
- Location-based forecasts and advisory generation.
- Multilingual interaction, including voice-enabled access for rural users.
- Historical weather analysis and climate trends.

**Research themes / implementation notes**

| Area | Questions to investigate |
|---|---|
| Data sources | Which official meteorological feeds, bulletins, forecast products and APIs are permitted and available? |
| Forecast grounding | How will responses identify issue time, forecast period, location and source rather than inventing weather values? |
| Conversational AI | How will user questions be converted into structured location/time/weather queries? |
| Alerts | How will severity, geographic relevance, issue time and expiry be represented? |
| Language and voice | Which Indian languages and speech interfaces can be supported reliably? |
| Evaluation | How will factual accuracy, relevance, latency, multilingual quality and alert delivery be measured? |

**Useful starting reference**

- [India Meteorological Department](https://mausam.imd.gov.in/) — official weather information, forecasts and warnings. Confirm the terms and access method for any data used by the implementation.

---

## 3. Working project and competition-document register

Use this table to keep the actual working files together with the repository. Add a relative path when a document is committed under `docs/`, `presentations/`, or another project folder.

| Work item | Related SIH reference | Document / artifact | Repository path or link | Status / notes |
|---|---|---|---|---|
| TerraLens AI research and solution direction | SIH26227 | Problem-statement analysis, architecture, data-source study, offline workflow and evaluation plan | Add files under `docs/sih/terralens-ai/` | Research direction associated with satellite imagery retrieval and change analysis |
| WeatherGPT research direction | SIH26068 | Problem analysis, conversational workflow, data-source study and evaluation plan | Add files under `docs/sih/weathergpt/` | Research reference; keep separate from TerraLens AI |
| SIH idea presentation | Selected SIH problem statement | Official-format idea presentation (PPT/PDF) | Add the final submitted copy and supporting assets here | Use the latest official SIH template |
| SIH prototype evidence | Selected SIH problem statement | Screenshots, demo video, test results and prototype notes | Add files under `docs/sih/evidence/` | Include only evidence that was actually produced and tested |
| SIH submission record | Selected SIH problem statement | Submitted title, abstract, team details, submission date and acknowledgement | Add a redacted copy or a record of the submission | Do not commit passwords, OTPs, private IDs or personal contact details |

### Existing project repository

- [APAAR-Verify-AI — GitHub repository](https://github.com/Balaji-P-A/APAAR-Verify-AI)

> **Competition mapping note:** APAAR-Verify AI and its AICTE/SEVA-related work are maintained separately from the two SIH problem statements indexed above. Do not label APAAR-Verify AI as SIH26068 or SIH26227 unless an official SIH submission record confirms that mapping.

---

## 4. Suggested folder structure for SIH materials

```text
APAAR-Verify-AI/
└── docs/
    ├── SIH_RESEARCH_AND_DOCUMENTATION.md
    └── sih/
        ├── terralens-ai/
        │   ├── problem-statement-analysis.md
        │   ├── research-notes.md
        │   ├── architecture.md
        │   ├── datasets-and-models.md
        │   └── evaluation-plan.md
        ├── weathergpt/
        │   ├── problem-statement-analysis.md
        │   ├── research-notes.md
        │   ├── architecture.md
        │   └── evaluation-plan.md
        ├── presentations/
        ├── evidence/
        └── submission/
```

Only create or list a file as completed after it exists. Keep large datasets, model weights, generated imagery and build outputs outside Git unless their licences and repository size make committing them appropriate. Prefer linking to the source and documenting download/version details.

---

## 5. Submission and research checklist

- [ ] Verify the selected PS ID and exact wording on the official SIH portal.
- [ ] Save the official SIH guidelines and current presentation template used by the team.
- [ ] Record the problem statement, sponsoring organisation, department and theme.
- [ ] Keep research claims traceable to source links, papers or dataset documentation.
- [ ] Record dataset names, versions, licences, acquisition dates and preprocessing steps.
- [ ] Record model names, versions, licences, weight locations and offline setup steps.
- [ ] Keep architecture diagrams, implementation notes and evaluation methodology in the repository.
- [ ] Keep a copy of the final submitted presentation and a submission acknowledgement, with personal information redacted where necessary.
- [ ] Do not publish private team data, credentials, API keys, restricted data or non-public organiser material.

---

## 6. Source and accuracy notes

1. The problem-statement detail pages linked above are community-maintained SIH 2026 archives. They are useful for research navigation, but are **not official SIH websites**.
2. The SIH official portal is the authority for final wording, deadlines, rules, eligibility and submission status. Recheck it before relying on any archived value.
3. The dates shown for SIH26068 and SIH26227 are the deadlines displayed in the linked SIH 2026 archive pages. They are historical dates, not upcoming deadlines.
4. Research ideas, implementation notes and suggested folder structures in this file are working notes. They should not be represented as official SIH requirements unless the official problem statement or guidelines explicitly say so.

---

*Maintained as the SIH research and documentation index for the project workspace.*
