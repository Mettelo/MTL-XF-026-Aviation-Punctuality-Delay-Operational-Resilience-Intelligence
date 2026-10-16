# MTL-XF-026 — Acceptance criteria and domain tests

**Business decision owner:** Director of Airport Operations & Resilience. **Decision:** Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

## Delivery sign-off

| ID | Deliverables | Required pass evidence | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight user requirements cover the commissioned questions, named stakeholder actions and core/extension boundary. | Business Analyst / Director of Airport Operations & Resilience |
| AC2 | D2 | 100% of used source files have approved provenance, version/coverage, licence, retrieval UTC and SHA-256. Required fields and reference versions are checked. | Data Governance Analyst |
| AC3 | D3 | Every input row is accounted for; keys and all many-to-many/hierarchy effects have explicit checks and no unexplained duplication. | Data Engineer / independent reviewer |
| AC4 | D4 | Five source cells reconcile within a declared rounding tolerance; all material differences and non-additive totals are explained. | Domain specialist |
| AC5 | D5 | All 8 metric contracts are classified core/conditional and have tested definitions; no unsupported fields or fabricated unavailable values. | Data Governance Analyst / BI Developer |
| AC6 | D6 | Five findings cover all business questions or evidence gaps; period, eligible population, magnitude, comparison and limitation are visible. | Domain analyst |
| AC7 | D7 | The project-specific baseline and alternative below are implemented; eligibility, scenario changes, reason codes and evidence requests are visible. | Director of Airport Operations & Resilience |
| AC8 | D8 | Five BI measures reconcile to curated outputs; all filters/reset/export retain the scope, units and limitations. | BI Developer / operational UAT user |
| AC9 | D9 | DT1–DT10 have actual execution evidence and expected/actual outcomes; no unresolved critical/high defect. | Independent reviewer |
| AC10 | D10 | A distinct member's clean rerun reproduces equivalent core outputs with documented environment and checks. | Independent rerun reviewer |
| AC11 | D11 | Two-page maximum briefing and 15–20 minute presentation answer the decision and assign investigation owners without unsupported outcomes. | Director of Airport Operations & Resilience / Mettelo panel |
| AC12 | D12 | Every member links substantive authored and reviewed work, including handover or presentation contribution. | Delivery Lead |

## Project-specific business success

1. Exactly eight unique monthly inputs are registered using the same report variant.
2. All-flight shares and matched-flight mean delay retain their respective denominators.
3. Every shortlisted segment shows eligible months, flight volume and sensitivity to 100/250-flight gates.

## Required prioritisation and sensitivity

Baseline minimum = 100 eligible flights per airport/airline month; sensitivity = 250. Require at least three eligible months and display coverage out of eight. Compare a declared adverse-punctuality reference consistently across months and order by flight-weighted delay burden. Record excluded low-volume cases. Volume gates are simulated design choices and must not be described as CAA standards.

Record each case's entity/segment, valid period, supporting measures, reason code, scenario position, missing evidence, responsible operational role, next review and manual-review trigger. Fewer than ten cases is valid; padding unsupported cases fails acceptance.

## DT1–DT10 — minimum executed domain tests

| Test | Input / action | Expected pass evidence |
| --- | --- | --- |
| DT1 | Confirm one source file for each of the eight months and fail on missing or repeated months. | Five selected published values reproduce within declared source precision, with explicit source coordinates and scope. |
| DT2 | Reconcile five airport/airline figures against source cells. | The invalid comparison, join or denominator is rejected or flagged according to the documented rule; no silent fallback. |
| DT3 | Demonstrate flight-weighted average delay differs correctly from an unweighted row mean. | The edge case produces an explicit unavailable/exclusion result or a supported calculation, with affected rows quantified. |
| DT4 | Verify zero/low-volume handling and the separate all-flight share versus matched-flight delay denominators. | The domain boundary remains visible in the analytical output and BI product; no unsupported inference. |
| DT5 | 10 flights averaging 10 minutes and 90 averaging 20 | Weighted delay = 19 minutes, not 15. |
| DT6 | All-flight delay-band shares include cancellation/unmatched components | Use the documented all-flight basis; do not renormalise to operated flights without a new label. |
| DT7 | Early-to-15-minutes-late is rebuilt from published sub-bands | Include all appropriate early bands and 0–15 late; publish the exact definition. |
| DT8 | One domestic movement appears at both reporting airports | Airport observations are not labelled unique UK flights. |
| DT9 | A segment has 150 eligible flights in a month | Passes 100-flight gate, fails 250-flight sensitivity; exclusion is visible. |
| DT10 | A full-analysis total differs from a summary report | Investigate coverage/consent and report variant; do not force equality. |

Worked values are **synthetic test fixtures**, not claims about the public data or simulated client. For each test retain requirement ID, source/input or fixture, expected result, actual result, evidence link, tester, independent reviewer and date. DT1–DT4 additionally require the documented project-specific rule; their general evidence descriptions do not waive the named domain condition. Add dashboard/filter tests as needed beyond these ten.

## Scope gate and unresolved issues

**Mandatory core:** Eight agreed full-analysis CSVs, January–August 2026. Use one consistent report variant: combined arrival/departure Full Analysis unless a documented variant change is approved. Fix a shortlist of airport/airline segments after profiling; preserve supported route detail for diagnostics. Separate matched-flight delay denominators from all-flight band and cancellation denominators.

**Optional extensions:** Full-year seasonality, delay-cause attribution, passenger compensation and operational resource optimisation are outside core. Arrival/departure-specific reports or 2025 history require separately registered sources and compatible definitions.

A mandatory source/field gap blocks the affected deliverable and must be resolved by a registered official replacement or approved, versioned scope change. An explicitly optional result may be unavailable with a reason and a useful evidence request. Neither missing raw data nor unexecuted tests may be marked passed.

A critical/high defect materially changes a headline value, cohort, recommendation, provenance or reproducibility and blocks release. Lower-impact issues require a named acceptance owner and disclosed impact. All panel feedback and approvals must be recorded honestly as simulated where applicable.
