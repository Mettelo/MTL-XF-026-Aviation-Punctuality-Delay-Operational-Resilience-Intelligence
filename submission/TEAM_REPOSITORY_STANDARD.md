# MTL-XF-026 — Mandatory team repository standard

## Ownership and setup

Create `MTL-XF-026-<team-name>` under the **Mettelo GitHub organisation**. Add every member using their own GitHub account. The team repository contains delivery evidence; this master remains the challenge specification. Record the master URL and reviewed specification commit in your README.

## Required structure

```text
README.md
CONTRIBUTIONS.md
data/SOURCE_REGISTER.md
data/raw/
data/reference/
data/metadata/
data/curated/
docs/01-discovery/
docs/02-data-governance/
docs/03-data-model/
docs/04-data-quality/
docs/05-kpi-catalogue/
docs/06-analysis/
docs/07-decision-framework/
docs/08-assurance-uat/
docs/09-technical-handover/
src/
sql/
notebooks/
analysis/
tests/
dashboard/
deliverables/
submission/FINAL_SUBMISSION.md
```

Use the implementation folders relevant to your chosen free toolchain; explain unused folders. SQL and notebooks are alternatives where appropriate, not a requirement to duplicate logic. Record dependencies and setup versions. Supply accessible BI exports if interactive access is unavailable.

## Project README requirements

State Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation? Include team/roles, frozen cohort, analytical grain, setup/run instructions, key outputs, five findings, shortlist/scenario links, limitations, quality/UAT status and submission version.

## Collaboration and roles

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Airport Operations & Aviation Strategy Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 026 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 026 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 026 dashboard measures and test every visible filter. |
| Aviation Performance Analyst | Own eligible-flight definitions, five source reconciliations and the eight-month comparability review. |
| Airport Operations Analyst | Translate up to ten persistent patterns into operational investigation questions without asserting delay causes. |
| Operational Assurance Analyst | Test flight weighting, cancellation denominators and sensitivity to at least two volume gates. |

Use issues for requirements/work packages, meaningful commits, branches, PRs and reviews where practical. A single bulk upload by one member is not sufficient collaboration evidence. `CONTRIBUTIONS.md` must link each member's artefacts, authored work, reviews, issues/PRs/commits and presentation/handover contribution. Commit totals alone do not establish contribution.

## Evidence rules

D1–D12 and AC1–AC12 need direct artefact/test links. Store outputs separately from raw inputs and preserve a manifest. Do not claim a freeze without actual checksums and source validation. Keep every manual adjustment in code or an auditable transformation record. Never commit credentials, prohibited personal data or confidential materials.

## Domain review requirements

- Eight months cannot establish full annual seasonality or causal responsibility for delays.
- Average percentages must be weighted with the correct eligible flights; missing/cancelled flights need explicit treatment.
- Aviation performance signals require operational event, weather and schedule evidence before attributing cause.

Include the four mandatory domain tests and at least six additional meaningful scenarios. A second member must verify the core rerun and five headline BI measures. Record any unavailable metric or approved scope change visibly.
