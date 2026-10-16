# MTL-XF-026 — Required deliverables and metric contracts

**Decision:** Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?  
**Business acceptance:** Director of Airport Operations & Resilience  
**Core scope:** Eight agreed full-analysis CSVs, January–August 2026. Use one consistent report variant: combined arrival/departure Full Analysis unless a documented variant change is approved. Fix a shortlist of airport/airline segments after profiling; preserve supported route detail for diagnostics. Separate matched-flight delay denominators from all-flight band and cancellation denominators.

All artefact locations refer to the team repository. Deliver the core before optional extensions. [The source register](../data/SOURCE_REGISTER.md) documents evidence status; required field support is a G1 release condition.

## D1 — Discovery & requirements

**Due:** Week 1 · **Location:** `docs/01-discovery/` · **Owner:** Business Analyst

Map the monthly airport/airline performance review, stakeholder needs, current reporting failures and target decision. Eight prioritised requirements must cover the business questions, scope gates and usable outputs.

**Pass evidence:** Each requirement has an accountable user, artefact, test and acceptance owner.

## D2 — Sources, governance & cohort contract

**Due:** Week 2 · **Location:** `data/; docs/02-data-governance/` · **Owner:** Data Governance Analyst

Complete the source-to-deliverable support matrix and classify core, fallback and optional inputs. Eight agreed full-analysis CSVs, January–August 2026. Use one consistent report variant: combined arrival/departure Full Analysis unless a documented variant change is approved. Fix a shortlist of airport/airline segments after profiling; preserve supported route detail for diagnostics. Separate matched-flight delay denominators from all-flight band and cancellation denominators.

**Pass evidence:** Every used input has provenance, exact version/coverage, licence evidence and SHA-256; conditional scope cannot be signed off without supporting fields.

## D3 — Reproducible model & ingestion

**Due:** Week 3 · **Location:** `src/; sql/; docs/03-data-model/` · **Owner:** Data Engineer

Implement raw preservation, selection, schema checks, curated facts and dimensions. Month × reporting airport × airline × supported route/destination × service/flight category and all other published dimensions. Preserve scheduled, actual, cancelled and matched-flight denominator distinctions.

**Pass evidence:** Zero unexplained duplicate keys or join inflation; every input row accounted for as retained/excluded/quarantined.

## D4 — Quality, source reconciliation & exceptions

**Due:** Week 3 · **Location:** `tests/; docs/04-data-quality/` · **Owner:** Independent reviewer + domain specialist

Execute source, denominator, missingness, boundary and linkage checks against the risk 'Wrong weighting, incompatible denominators, report variants and duplicate airport observations can reverse punctuality comparisons.'

**Pass evidence:** Reconcile five source values from at least two periods or segments; retain source coordinates, precision and explanations for non-additive totals.

## D5 — Governed metric catalogue

**Due:** Week 4 · **Location:** `docs/05-kpi-catalogue/` · **Owner:** Domain specialist + Data Governance Analyst

Implement the 8 metric contracts below; distinguish unconditional core metrics from gated extensions.

**Pass evidence:** Each core metric has purpose, raw fields, formula, grain, denominator/unit, missing/zero handling, owner, refresh and test; conditional items have explicit eligibility or unavailable status.

## D6 — Domain assessment

**Due:** Week 5 · **Location:** `analysis/; docs/06-analysis/` · **Owner:** Domain analyst

Separate volume, punctuality, delay distribution and cancellation measures; retain route mix and matched-flight coverage. Show three-month persistence and eight-month coverage for each airport/airline segment.

**Pass evidence:** At least five supported findings answer the five questions or document a genuine evidence gap; each includes magnitude, scope, comparison and limitation.

## D7 — Investigation framework & scenarios

**Due:** Week 6 · **Location:** `docs/07-decision-framework/` · **Owner:** Director of Airport Operations & Resilience (business acceptance)

Baseline minimum = 100 eligible flights per airport/airline month; sensitivity = 250. Require at least three eligible months and display coverage out of eight. Compare a declared adverse-punctuality reference consistently across months and order by flight-weighted delay burden. Record excluded low-volume cases. Volume gates are simulated design choices and must not be described as CAA standards.

**Pass evidence:** Publish eligibility, component definitions, scenario differences and up to ten supported cases; every case names a service role, evidence request and review trigger.

## D8 — Decision-support BI

**Due:** Draft Week 6; final Week 7 · **Location:** `dashboard/` · **Owner:** BI Developer

Build overview, diagnostic and quality pages for the monthly airport/airline performance review. Show period, units, definitions, missingness and core/extension status.

**Pass evidence:** Five headline values reconcile; every visible filter and reset tested; accessible static export plus free review/build path.

## D9 — Assurance & simulated UAT

**Due:** Week 7 · **Location:** `docs/08-assurance-uat/` · **Owner:** Independent reviewer

Execute DT1–DT10 below, plus any tool-specific calculations and filter tests. Record expected/actual evidence, requirement links and defects.

**Pass evidence:** All ten mandatory domain cases evidenced; no critical/high issue remains; accepted lower-impact limitations have named review.

## D10 — Technical & operational handover

**Due:** Week 8 · **Location:** `docs/09-technical-handover/` · **Owner:** Data Engineer + a second-member reviewer

Provide environment, immutable manifest, end-to-end run, output checks, troubleshooting and refresh/change process.

**Pass evidence:** A second member regenerates equivalent core outputs without undocumented edits and records checks, environment, duration and result.

## D11 — Executive briefing & presentation

**Due:** Week 8 · **Location:** `deliverables/` · **Owner:** Business Analyst + specialist service roles

Deliver maximum two-page briefing and 15–20 minute presentation to Director of Airport Operations & Resilience: decision, five findings, scenario comparison, investigation actions, evidence gaps and next review.

**Pass evidence:** Every numeric claim links to tested evidence; explicitly show a case where action is not yet supported.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8 · **Location:** `CONTRIBUTIONS.md` · **Owner:** Delivery Lead

Link actual authored work, reviews, issues/PRs/commits and presentation/handover contributions for every member.

**Pass evidence:** All responsibilities have owners and evidence; commit count alone is insufficient.

## Metric contracts — authoritative definitions

| Metric | Definition / support condition |
| --- | --- |
| Eligible flight volume | Published matched/eligible flights under the source definition; identify flights excluded from punctuality calculation. |
| On-time band share | Use the exact CAA bands and documented denominator; label an early-to-15-minutes-late aggregate explicitly if reconstructed. Do not silently switch to matched-flight percentages. |
| Average delay minutes | Flight-weighted average = sum(mean delay × eligible flights) / sum(eligible flights) for compatible rows. |
| Severe-delay share | Aggregate the published bands for a declared threshold using their documented all-flight basis; preserve cancellation/unmatched context. |
| Cancellation share | Use the published cancellation percentage or 100 × cancelled / compatible total flights under CAA definitions; show the denominator explicitly. |
| Month-to-month change | Current on-time share minus previous comparable-month share, in percentage points. |
| Persistent-pressure flag | Adverse threshold exceeded in at least three observed months; report available months and volume gate. |
| Monthly coverage | Observed eligible months / eight required cohort months. |

For each metric add source ID and actual raw fields, business purpose, formula, grain, valid population, unit, numerator/denominator, hierarchy, suppression/zero/missing handling, owner, refresh and test evidence. Verify source rounding before setting a reconciliation tolerance. A conditional item is not silently promoted into core; a core requirement is not silently waived.

## Project-specific outcomes

1. Exactly eight unique monthly inputs are registered using the same report variant.
2. All-flight shares and matched-flight mean delay retain their respective denominators.
3. Every shortlisted segment shows eligible months, flight volume and sensitivity to 100/250-flight gates.

See [DT1–DT10 and investigation rules](ACCEPTANCE_CRITERIA.md) for worked pass/fail cases. Source schemas, specific period selections and reference versions must be signed at G1. Keep calculation definitions here; other guidance pages link to this contract rather than maintaining competing copies.
