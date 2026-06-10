# Executive Summary
## Purpose Index Dashboard — Business Intelligence Platform
**Measure to Improve · Cátedra DPM / UIC Barcelona · 2026**

---

## About Measure to Improve

Measure to Improve was born after more than fifteen years of research on how to measure the experience of purpose within organizations. What began as an academic challenge is now a global movement that helps companies turn their purpose into action.

The movement emerged from a collaborative initiative led by the Chair in Management by Missions and Corporate Purpose, together with two pioneering foundations in purpose-driven organizational development: Corporate Excellence — Centre for Reputation Leadership and the DPMC Foundation.

The movement is backed by institutions including IESE Business School and Harvard T.H. Chan School of Public Health, and has grown to:

| Metric | Scale |
|---|---|
| Employees surveyed | +300,000 |
| Companies participating | +150 |
| Countries | +25 |
| Sectors | +15 |

---

## The Purpose Index — 3D Index

Companies give their employees a voice with three questions that form the Purpose Index, developed from over fifteen years of research on purpose measurement.

The three questions measure purpose from three distinct dimensions:

| Dimension | Question |
|---|---|
| Q1 — Coherence of Managers | Management's behavior is consistent with the PURPOSE / MISSION of the company |
| Q2 — Personal Connection | The PURPOSE / MISSION of my company is aligned with my personal values |
| Q3 — Coherence of Colleagues | My colleagues' behavior is consistent with the PURPOSE / MISSION of the company |

The terms "purpose/mission" may be replaced by any of the following: "purpose"; "purpose and mission"; "mission"; "mission and values"; "mission and vision"; "mission, vision, and values"; "purpose and values"; "purpose, mission, and values."

The measurement is flexible and can be applied to the entire organization or specific groups — area, department, hierarchical level, geographic region — always with a minimum of 30 people to ensure anonymous and reliable results.

---

## The Challenge

The Measure to Improve movement spans 150+ companies, 300,000+ employees across 25+ countries and 15+ sectors. As the movement scaled across new markets and sectors, the need for a more automated and flexible reporting infrastructure became clear — one capable of keeping pace with the growing volume of data while preserving the accuracy and rigor of the analysis.

The platform was architected to match the movement's scale and continue growing alongside it.

The need: an automated, scalable BI solution that could:

- Process large volumes of employee survey records simultaneously
- Generate contextual benchmarks for each company
- Deliver secure, personalized dashboards to each client
- Operate without manual intervention after initial setup

---

## The Solution

A fully automated end-to-end Business Intelligence platform built on Google Workspace — requiring zero infrastructure investment and integrating seamlessly into the organization's existing tools.

---

## How It Works

```
1. Company distributes 3-question survey to employees
        ↓
2. Raw data uploaded to the platform
        ↓
3. Single button click triggers automated pipeline
        ↓
4. Script cleans, normalizes and transforms all records
        ↓
5. KNN algorithm calculates contextual benchmark
        ↓
6. Secure personalized dashboard ready in < 5 minutes
        ↓
7. Each company accesses only their own data
```

---

## Technical Architecture

### Automated ETL Pipeline

- Ingests raw survey data and normalizes large volumes of employee records
- Auto-detects language per country — English / Spanish — with no manual configuration
- Applies ARRAYFORMULA, IFS, REGEXMATCH and IFERROR for field calculation and cleaning
- Generates calculated metrics: Purpose Index Gross, Net, Profiles, and demographic segmentation

### Custom KNN Benchmark Algorithm

The core innovation — a nearest-neighbor algorithm that identifies the most contextually similar companies for each organization and computes a weighted benchmark score. The algorithm applies a multi-tier matching logic to prioritize the most relevant peers, and the benchmark is automatically refreshed on every pipeline run.

Below is a simplified illustration of how a nearest-neighbor matching approach works conceptually:

```javascript
// Illustrative example — not the actual implementation
candidates = dataset.filter(c => matchesCriteria(c, target))
neighbors  = candidates.sortBy(c => distance(c.metrics, target.metrics))
benchmark  = weightedAverage(neighbors.slice(0, K))
```

*(The specific matching criteria, tier structure, distance function, weighting logic, and peer dataset used in this project are proprietary and confidential. The example above is illustrative only and does not reflect the actual algorithm.)*

This approach produces benchmarks more accurate than global industry averages — each company is compared against peers that truly reflect their context.

### Purpose Profile Classification

Each employee is classified into one of 6 profiles based on combined Q1/Q2/Q3 responses — using an algorithm that weights the personal alignment dimension as primary, combined with the coherence dimensions:

| Profile | Description |
|---|---|
| Profile 1 | Level 1 |
| Profile 2 | Level 2 |
| Profile 3 | Level 3 |
| Profile 4 | Level 4 |
| Profile 5 | Level 5 |
| Profile 6 | Level 6 |

Profile names, descriptions and the classification methodology is proprietary to Measure to Improve.

### Data Architecture

A purpose-built pivot layer (3 rows per employee × 3 questions) enables real-time segment filtering in Looker Studio — where each filter selection dynamically recalculates Q1/Q2/Q3 results for that specific segment.

---

## Platform Metrics

| Metric | Value |
|---|---|
| Employee records processed | ~30,000 *(anonymized — actual figure is confidential)* |
| Movement scale | 150+ companies · 300k+ employees · 25+ countries |
| Processing time (full pipeline) | < 5 minutes |
| Dashboard pages | 8 |
| Interactive charts | 50+ |
| Segmentation dimensions | 6 (Gender, Generation, Seniority, Area, Role, Age) |
| Languages | English + Spanish (auto-detected) |
| Security model | Row-level security |

---

## Business Impact

**Platform Impact:**
- Full pipeline execution in under 5 minutes
- Interactive dashboard with real-time segment filtering across 6 dimensions
- Contextual KNN benchmark automatically calculated for each company
- Secure multi-tenant access — each client sees exclusively their own data
- Zero manual intervention after data upload

---

## Security & Confidentiality

For this measurement to be effective and truly aimed at measuring for improvement, it must be developed in an environment of trust, confidentiality, and anonymity.

The platform implements row-level security — each company accesses only their own data, with zero risk of cross-company data exposure.

Company names, sectors and all identifying information have been fully anonymized to protect client confidentiality.

---

## Tech Stack

| Layer | Technology | Role |
|---|---|---|
| Data Storage | Google Sheets | Backend database |
| ETL Automation | Google Apps Script V8 | Data ingestion, cleaning, transformation |
| Formulas | ARRAYFORMULA, IFS, REGEXMATCH, IFERROR | Field calculation and normalization |
| Algorithm | Custom KNN — JavaScript | Contextual benchmark matching |
| Visualization | Google Looker Studio | Interactive multi-tenant dashboard |
| Design | Python + Pillow | Dashboard mockup generation |
| Security | Row-level access control | Data isolation per client |

---

## Live Dashboard

🔗 [View Live Dashboard](https://datastudio.google.com/s/kg_Gf8wFY98)

*Company names, sectors and all identifying information have been fully anonymized to protect client confidentiality. No real organizational data, client identifiers, or individual records are accessible through this link — all sensitive information has been replaced with anonymized equivalents prior to publication. Access to the original dataset is restricted and governed by a confidentiality agreement.*

---

## About the Author

**Ignacio Dehoy** · Data Analyst & Business Intelligence Specialist · Barcelona, Spain

Built for Measure to Improve — a global movement helping companies measure and improve the experience of purpose.

- 🌐 [measuretoimprove.org](https://measuretoimprove.org)
- 📧 [support@measuretoimprove.org](mailto:support@measuretoimprove.org)
- 💼 [Measure to Improve LinkedIn](https://www.linkedin.com/company/measuretoimprove)
- 👤 [Connect on LinkedIn](https://www.linkedin.com/in/ignacio-dehoy-munoz/)

---

*© 2026 Measure to Improve · All rights reserved*
