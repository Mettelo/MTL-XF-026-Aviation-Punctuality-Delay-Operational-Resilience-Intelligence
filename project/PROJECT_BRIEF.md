# MTL-XF-026 — Project brief

## Engagement

This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

**Simulated sponsor:** Confidential Airport Operations & Aviation Strategy Directorate. **Duration:** 8 weeks. **Team:** 6–8 members. **Track:** Cross-Functional. **Sector:** Aviation / Transport / Operations.

## Commission

Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

**Aviation Punctuality, Delay & Operational Resilience Intelligence.** An airport/aviation operations team needs to identify persistent delay patterns by airport/airline rather than overreacting to a single bad month. The output should support resilience planning and operational-performance review.

## Outcomes and boundaries

- Separate volume, punctuality, delay distribution and cancellation measures; retain route mix and matched-flight coverage.
- Show three-month persistence and eight-month coverage for each airport/airline segment.
- Produce up to ten resilience-investigation cases under at least two minimum-flight thresholds and compare weighted with unweighted summaries.

Deliver evidence for a management investigation decision, with an auditable shortlist of up to ten cases and at least two alternative prioritisation scenarios. Do not manufacture a full shortlist where the data supports fewer cases. Findings may conclude that evidence is insufficient.

**Data boundary:** Freeze all eight agreed CAA monthly full-analysis CSVs for January–August 2026. The eight months are the core cohort; do not describe them as a full year or infer annual seasonality. Historical 2025 files are optional extensions with their own source records.

**Model boundary:** Month × reporting airport × airline × supported route/destination × service/flight category and all other published dimensions. Preserve scheduled, actual, cancelled and matched-flight denominator distinctions.

**Out of scope:** real operational deployment, confidential case-level data, guaranteed savings/outcome improvements, paid-source dependencies and automatic allocation of services or funding. Optional modelling or enriched sources must not delay or replace the core D1–D12 pack.

## Users and acceptance owners

- Simulated sponsor/review panel: approves commissioned question, changes and final investigation recommendation.
- Domain service/planning user: checks whether diagnostic evidence supports the proposed review action.
- Data steward: verifies source/version, licence, definitions, quality and retention evidence.
- BI user: tests overview, drill-down, filters and limitations.
- Independent reviewer: verifies calculations, rerun and requirement-to-test traceability.

These are simulated stakeholder roles, not claims of access to a real organisation.

## Work allocation

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Airport Operations & Aviation Strategy Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 026 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 026 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 026 dashboard measures and test every visible filter. |
| Aviation Performance Analyst | Own eligible-flight definitions, five source reconciliations and the eight-month comparability review. |
| Airport Operations Analyst | Translate up to ten persistent patterns into operational investigation questions without asserting delay causes. |
| Operational Assurance Analyst | Test flight weighting, cancellation denominators and sensitivity to at least two volume gates. |

At kickoff, replace role ownership with named team members and record review partners in `CONTRIBUTIONS.md`. Multiple roles per member are permitted, but critical calculations need a reviewer distinct from their author.

## Working stages

1. Week 1: agree at least eight requirements and define expected decisions.
2. Week 2: inspect actual file schemas, establish available coverage and approve cohort freeze.
3. Week 3: implement and reconcile analytical facts, keys and exclusions.
4. Week 4: approve the 8-measure KPI catalogue and denominator rules.
5. Week 5: complete five supported findings and domain comparisons.
6. Week 6: compare two decision scenarios, produce the investigation shortlist and BI draft.
7. Week 7: execute ten or more assurance/UAT scenarios, including project-specific edge cases.
8. Week 8: independent rerun, executive briefing, presentation and final handover.

## Sign-off

Follow [D1–D12](DELIVERABLES.md) and [AC1–AC12](ACCEPTANCE_CRITERIA.md). Approve only with reproducible evidence, no unresolved critical/high defects and transparent conditional-data limitations. A change in source availability must be logged; do not silently substitute a newer release.
