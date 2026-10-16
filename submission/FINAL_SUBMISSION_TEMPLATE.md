# MTL-XF-026 — Final submission: Aviation Punctuality, Delay & Operational Resilience Intelligence

Complete this template in your team repository as `submission/FINAL_SUBMISSION.md`. Replace prompts with evidence; leave unavailable items explicitly unavailable with reasons. This template itself is not completed delivery evidence.

## Team and version

- Team repository URL:
- Team name and individual GitHub accounts:
- Final commit/tag and submission date:
- Master specification URL and reviewed commit:
- Delivery dates:
- Named role owners and independent reviewers:
- Engagement declaration: simulated confidential-client engagement using official public/open data; no real-client employment, endorsement or privileged access claimed.

## Commissioned decision

Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

State the answer, confidence, principal limitation and proposed investigation action.

## Actual cohort and provenance

Agreed boundary: Freeze all eight agreed CAA monthly full-analysis CSVs for January–August 2026. The eight months are the core cohort; do not describe them as a full year or infer annual seasonality. Historical 2025 files are optional extensions with their own source records.

Record actual frozen files/versions, manifest/checksums, source-register link, licence evidence, retrieval timestamp, schema/coverage validation, inclusions/exclusions and approved deviations. Do not mark acquisition complete without evidence.

## Evidence index

| Deliverable | Artefact link | Owner / reviewer | Status / limitation |
| --- | --- | --- | --- |
| D1 — Discovery & decision requirements | To complete | To complete | To complete |
| D2 — Governed sources & cohort | To complete | To complete | To complete |
| D3 — Reproducible analytical model | To complete | To complete | To complete |
| D4 — Quality & reconciliation | To complete | To complete | To complete |
| D5 — KPI catalogue | To complete | To complete | To complete |
| D6 — Domain analytical assessment | To complete | To complete | To complete |
| D7 — Investigation decision framework | To complete | To complete | To complete |
| D8 — BI decision-support product | To complete | To complete | To complete |
| D9 — Independent assurance & UAT | To complete | To complete | To complete |
| D10 — Technical & operational handover | To complete | To complete | To complete |
| D11 — Executive recommendation | To complete | To complete | To complete |
| D12 — Contribution & delivery record | To complete | To complete | To complete |

## Governed measures

| Required measure | Definition/source/test link | Result / unavailable reason |
| --- | --- | --- |
| Eligible flight volume | To complete | To complete |
| On-time share | To complete | To complete |
| Average delay minutes | To complete | To complete |
| Severe-delay share | To complete | To complete |
| Cancellation share | To complete | To complete |
| Month-to-month change | To complete | To complete |
| Persistent-pressure flag | To complete | To complete |
| Monthly coverage | To complete | To complete |

## Business questions and five findings

1. Which airport/airline combinations have persistent rather than one-month delays?
2. How do flight volumes and route mix affect apparent performance?
3. Which delay bands or cancellation measures contribute to deterioration?
4. Does a minimum-volume rule alter the investigation shortlist?
5. What operational cause evidence is needed before attributing delay to an organisation?

For each question record the finding, quantitative evidence, period/grain, comparison, uncertainty, limitation and artefact link. Record an evidenced gap where the data cannot answer it.

## Investigation shortlist and sensitivity

Provide up to ten supported cases. For each: entity/segment, signal and magnitude, eligibility, reason code, scenario membership, proposed investigation, responsible role, missing evidence and review trigger. Compare at least two scenarios and explain membership/rank changes. Include a case where evidence is insufficient for action.

## Acceptance and assurance

| Criterion | Pass/fail / evidence / reviewer |
| --- | --- |
| AC1 (D1) | To complete |
| AC2 (D2) | To complete |
| AC3 (D3) | To complete |
| AC4 (D4) | To complete |
| AC5 (D4–D5) | To complete |
| AC6 (D5) | To complete |
| AC7 (D6) | To complete |
| AC8 (D7) | To complete |
| AC9 (D8) | To complete |
| AC10 (D9) | To complete |
| AC11 (D10–D11) | To complete |
| AC12 (D12) | To complete |

Record at least ten executed UAT scenarios, expected/actual results, defect severity/disposition and five reconciled BI measures. Mandatory cases:

1. Confirm one source file for each of the eight months and fail on missing or repeated months.
2. Reconcile five airport/airline figures against source cells.
3. Demonstrate flight-weighted average delay differs correctly from an unweighted row mean.
4. Test zero eligible flights, a low-volume route and cancellations excluded from the punctuality denominator.

## Reproducible handover

- Environment/tool versions and dependencies:
- Input snapshot location and checksum verification:
- Clean run instructions and output locations:
- Independent rerun reviewer/date/duration/results:
- Reconciliation evidence and permitted rounding:
- Refresh/change process and known failure modes:

## Executive delivery

- Two-page briefing link:
- Presentation link and 15–20 minute duration:
- Dashboard/free access instructions and static export:
- Recommendations, missing evidence, responsible roles and next review:

## Contributions

For every member link authored artefacts, review work, issues/PRs/commits and presentation/handover contribution. Link `CONTRIBUTIONS.md`; commit count alone is insufficient.

## Limitations and review decision

- Eight months cannot establish full annual seasonality or causal responsibility for delays.
- Average percentages must be weighted with the correct eligible flights; missing/cancelled flights need explicit treatment.
- Aviation performance signals require operational event, weather and schedule evidence before attributing cause.

Add actual limitations, optional extensions, unresolved accepted issues and their impacts. Record simulated panel review date, reviewers and decision only after review occurs. Do not claim real operational savings or outcome improvements.
