# MTL-XF-026 — Required deliverables

**Commissioned decision:** Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

All locations below refer to the team's delivery repository. The master repository defines the requirements and contains no completed analysis. Owners are assigned from [the project roles](PROJECT_BRIEF.md).

## D1 — Discovery & decision requirements

**Due:** Week 1  
**Team artefact location:** `docs/01-discovery/`

Decision statement; stakeholder map; as-is reporting to investigation-review process; at least eight prioritised requirements. Answer these questions: Which airport/airline combinations have persistent rather than one-month delays? How do flight volumes and route mix affect apparent performance? Which delay bands or cancellation measures contribute to deterioration? Does a minimum-volume rule alter the investigation shortlist? What operational cause evidence is needed before attributing delay to an organisation?

**Acceptance evidence:** All requirements have an owner, priority, deliverable and test ID; domain analyst approves scope.

## D2 — Governed sources & cohort

**Due:** Week 2  
**Team artefact location:** `docs/02-data-governance/; data/`

Freeze all eight agreed CAA monthly full-analysis CSVs for January–August 2026. The eight months are the core cohort; do not describe them as a full year or infer annual seasonality. Historical 2025 files are optional extensions with their own source records. Register exact files, metadata, licences, checksums, coverage and critical fields; record rejection of unavailable dimensions.

**Acceptance evidence:** 100% of inputs registered; no claimed freeze until acquisition evidence exists.

## D3 — Reproducible analytical model

**Due:** Week 3  
**Team artefact location:** `src/; sql/; docs/03-data-model/`

Month × reporting airport × airline × supported route/destination × service/flight category and all other published dimensions. Preserve scheduled, actual, cancelled and matched-flight denominator distinctions. Deliver load, type checks, hierarchy handling, lineage, exclusions and environment instructions.

**Acceptance evidence:** A second member regenerates equivalent curated outputs from identical inputs; no unexplained duplicate analytical keys.

## D4 — Quality & reconciliation

**Due:** Week 3  
**Team artefact location:** `docs/04-data-quality/; tests/`

Profile missingness, suppression, valid values, keys and join coverage. Confirm one source file for each of the eight months and fail on missing or repeated months. Reconcile five airport/airline figures against source cells. Demonstrate flight-weighted average delay differs correctly from an unweighted row mean. Test zero eligible flights, a low-volume route and cancellations excluded from the punctuality denominator.

**Acceptance evidence:** Every input row is accounted for as retained, excluded or quarantined; five published cells reconcile within declared rounding.

## D5 — KPI catalogue

**Due:** Week 4  
**Team artefact location:** `docs/05-kpi-catalogue/`

Define all 8 measures listed below with formula, grain, denominator, unit, source fields, exclusions, owner, refresh and limitations.

**Acceptance evidence:** 100% headline metrics trace to source fields and tested transformations; conditional unavailable measures are explicitly marked.

## D6 — Domain analytical assessment

**Due:** Week 5  
**Team artefact location:** `analysis/; docs/06-analysis/`

Separate volume, punctuality, delay distribution and cancellation measures; retain route mix and matched-flight coverage. Show three-month persistence and eight-month coverage for each airport/airline segment.

**Acceptance evidence:** At least five evidence-backed findings state period, population, comparison, magnitude, uncertainty and limitation; negative findings count.

## D7 — Investigation decision framework

**Due:** Week 6  
**Team artefact location:** `docs/07-decision-framework/`

Produce up to ten resilience-investigation cases under at least two minimum-flight thresholds and compare weighted with unweighted summaries. Record eligibility, thresholds, weights if used, reason codes and manual review triggers.

**Acceptance evidence:** Every shortlisted case has metrics, rationale, owner and evidence gaps; at least two scenarios compared; fewer than ten is valid where evidence is insufficient.

## D8 — BI decision-support product

**Due:** Draft Week 6; final Week 7  
**Team artefact location:** `dashboard/`

Executive overview answering 'Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?' plus diagnostic and data-quality views; visible periods, units, denominator notes, resettable filters and accessible labels.

**Acceptance evidence:** Five headline measures reconcile; every filter tested; export screenshots/PDF plus reproducible build or free access instructions.

## D9 — Independent assurance & UAT

**Due:** Week 7  
**Team artefact location:** `docs/08-assurance-uat/`

At least ten scenarios including the four project-specific tests below; requirement-to-test matrix, expected/actual evidence, defect log and simulated stakeholder feedback.

**Acceptance evidence:** No unresolved critical/high defect; accepted lower-severity limitations have a named reviewer and explicit impact.

## D10 — Technical & operational handover

**Due:** Week 8  
**Team artefact location:** `docs/09-technical-handover/`

Clean setup, architecture, frozen input manifest, run/refresh steps, output checks, troubleshooting and change-control process for Aviation Punctuality, Delay & Operational Resilience Intelligence.

**Acceptance evidence:** Another member reproduces the core outputs without undocumented edits and records environment, duration and discrepancies.

## D11 — Executive recommendation

**Due:** Week 8  
**Team artefact location:** `deliverables/`

Maximum two-page briefing and 15–20 minute presentation: commissioned decision, five findings, investigation shortlist, sensitivity, missing evidence, responsibilities and next review.

**Acceptance evidence:** Every quantitative claim links to an artefact/metric; no unsupported causal, policy or operational guarantee.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8  
**Team artefact location:** `CONTRIBUTIONS.md; delivery issues/PRs`

Record who delivered and reviewed each MTL-XF-026 work package, including domain, governance, engineering, BI and assurance contributions.

**Acceptance evidence:** Every member links to substantive artefacts and review/presentation evidence; commit count alone is insufficient.

## Required KPI definitions

| Metric | Required definition / calculation |
| --- | --- |
| Eligible flight volume | Published matched/eligible flights under the source definition; identify flights excluded from punctuality calculation. |
| On-time share | Published on-time percentage under the exact CAA tolerance; recompute only with compatible numerator and denominator. |
| Average delay minutes | Flight-weighted average = sum(mean delay × eligible flights) / sum(eligible flights) for compatible rows. |
| Severe-delay share | Published or reconstructed delay-band share for a declared threshold; do not invent unreported bands. |
| Cancellation share | 100 × cancelled flights / publisher-compatible scheduled flights, only if both are available. |
| Month-to-month change | Current on-time share minus previous comparable-month share, in percentage points. |
| Persistent-pressure flag | Adverse threshold exceeded in at least three observed months; report available months and volume gate. |
| Monthly coverage | Observed eligible months / eight required cohort months. |

For every metric record business purpose, formula, source fields, grain, unit, numerator/denominator, exclusions, suppression, zero-base behaviour, owner, refresh and test evidence. Do not populate conditional metrics from invented fields.

## Mandatory domain scenarios

1. Confirm one source file for each of the eight months and fail on missing or repeated months.
2. Reconcile five airport/airline figures against source cells.
3. Demonstrate flight-weighted average delay differs correctly from an unweighted row mean.
4. Test zero eligible flights, a low-volume route and cancellations excluded from the punctuality denominator.

## Review gates

Week 2: cohort and source approval. Week 4: model, DQ and metrics approval. Week 6: analytical and decision-framework review. Week 8: UAT, independent rerun and final panel review. Record reviewer, date, artefact version and decision at every gate.
