# MTL-XF-026 — Acceptance criteria

**Decision to support:** Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

These criteria assess delivery quality; they do not certify real operational outcomes. Complete a requirement → deliverable → test → evidence → reviewer matrix in the team repository.

| ID | Deliverables | Pass condition | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight or more prioritised requirements map to a named user, deliverable, acceptance test and reviewer. | Business Analyst / simulated sponsor |
| AC2 | D2 | 100% of core and extension inputs have exact source URL, actual version/coverage, retrieval timestamp, licence evidence, byte size and SHA-256; mutable endpoints have one approved snapshot. | Data Governance Analyst |
| AC3 | D3 | A distinct reviewer reruns the same frozen inputs in the documented environment and obtains equivalent curated rows and values; explain any nondeterministic ordering. | Data Engineer / independent reviewer |
| AC4 | D4 | Every input row is accounted for in retained/excluded/quarantined counts; zero unexplained key duplicates; all join multiplication is quantified. | Data Engineer / domain analyst |
| AC5 | D4–D5 | At least five source cells across two periods or segments reconcile exactly for counts and within source precision for rounded measures. Each tolerance is declared before testing. | Domain analyst / assurance reviewer |
| AC6 | D5 | All 8 listed measures have definitions, source lineage and edge-case behaviour; conditional unavailable metrics show an explicit reason, no fabricated value. | Data Governance Analyst / BI Developer |
| AC7 | D6 | At least five findings state scope, magnitude, comparison and limitation; all five business questions are answered or have an evidenced data gap. | Domain analyst |
| AC8 | D7 | Up to ten investigation cases have reason codes, supporting metrics, an owner and missing-evidence request; at least two priority scenarios show membership/rank changes and rationale. | Specialist policy/operations role |
| AC9 | D8 | At least five headline BI values reconcile to curated output; all visible filters, reset behaviour, period labels, units and quality warnings are tested. | BI Developer / UAT reviewer |
| AC10 | D9 | At least ten scenarios include the four mandatory domain cases, calculation, filtering, missingness and reproducibility; expected/actual results and evidence recorded; zero unresolved critical/high defects. | Assurance reviewer |
| AC11 | D10–D11 | Independent clean rerun evidence, maximum two-page briefing and 15–20 minute presentation exist; every numerical recommendation links to a tested metric/artefact. | Delivery Lead / review panel |
| AC12 | D12 | Each member has evidence-linked authored and reviewed work, role ownership and presentation/handover contribution; master/team repository distinction maintained. | Delivery Lead |

## Required domain acceptance cases

1. Confirm one source file for each of the eight months and fail on missing or repeated months.
2. Reconcile five airport/airline figures against source cells.
3. Demonstrate flight-weighted average delay differs correctly from an unweighted row mean.
4. Test zero eligible flights, a low-volume route and cancellations excluded from the punctuality denominator.

Each case needs test input/reference, expected result, actual result, pass/fail, evidence path, tester, reviewer and execution date. Add cases until there are at least ten; do not count a written assertion as an executed test.

## Specific analytical sign-off

- Separate volume, punctuality, delay distribution and cancellation measures; retain route mix and matched-flight coverage.
- Show three-month persistence and eight-month coverage for each airport/airline segment.
- Produce up to ten resilience-investigation cases under at least two minimum-flight thresholds and compare weighted with unweighted summaries.

Reviewers must verify the declared cohort and grain:

Freeze all eight agreed CAA monthly full-analysis CSVs for January–August 2026. The eight months are the core cohort; do not describe them as a full year or infer annual seasonality. Historical 2025 files are optional extensions with their own source records.

Month × reporting airport × airline × supported route/destination × service/flight category and all other published dimensions. Preserve scheduled, actual, cancelled and matched-flight denominator distinctions.

## Failed or unavailable evidence

A conditional metric may be marked unavailable when the source lacks its dimensions, with a documented alternative or evidence request. This does not waive the core model, dashboard or assurance. A change to a mandatory requirement needs a change log entry with impact and simulated-panel approval. Missing sources mean the data freeze remains pending; do not mark a source gate passed.

Critical/high means a defect materially changes a headline value, cohort, recommendation, provenance or reproducibility. Such defects block final acceptance. Lower-severity limitations need named acceptance and disclosed effect. No stakeholder approval may be invented; record simulated UAT as simulated.
