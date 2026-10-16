# MTL-XF-026 — Aviation Punctuality, Delay & Operational Resilience Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Airport Operations & Aviation Strategy Directorate  
**Accountable simulated executive:** Director of Airport Operations & Resilience  
**Sector:** Aviation / Transport / Operations  
**Team:** 6–8 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** monthly airport/airline performance review

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business setting

The simulated airport operations and aviation strategy directorate brings performance managers and operations leads together for a monthly resilience review. The immediate task is to choose which airport/airline operating patterns deserve a joint diagnostic discussion.

## Business problem

The Director of Airport Operations & Resilience needs to commission the right operational investigations rather than react to the worst percentage in the monthly pack. Current summaries can elevate small-volume routes, mix cancellation exposure with operated-flight delay, and hide a persistent airport/airline pattern behind changes in flight mix.

The resulting agenda can focus on a short-lived or low-volume outlier while a higher-volume recurring issue receives less attention. The commission is a flight-weighted performance review for January–August 2026 that shows persistence, coverage and sensitivity before identifying cases for joint operations discussion. Delay causes and operational remedies require evidence beyond the CAA tables.

## Commissioned decision

> Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

## Practical use

At the monthly review, the Airport Performance Manager opens a shortlisted airport/airline case and shows its eight-month coverage, eligible flights and monthly punctuality pattern. The Operations Planning Lead compares the case under the 100- and 250-flight gates and checks whether the concern remains after flight weighting and route-mix inspection.

The Director commissions a joint resilience diagnostic only when the evidence is sufficiently stable, assigning an Operations owner to request schedule, weather and disruption logs. A low-volume or incomplete case remains on a watchlist. The output frames a specific operational question; it does not assign fault or prescribe a staffing change from the public performance data.

**Management handover:** An airport/airline performance pack with a flight-weighted scorecard, separate cancellation and matched-flight delay measures, coverage diagnostics, threshold sensitivity and a joint-investigation brief for each selected case.

The full [business context](project/BUSINESS_CONTEXT.md) sets out stakeholders, decisions, evidence limits and proposed benefit measures.

## What must be delivered

1. Separate volume, punctuality, delay distribution and cancellation measures; retain route mix and matched-flight coverage.
2. Show three-month persistence and eight-month coverage for each airport/airline segment.
3. Produce up to ten resilience-investigation cases under at least two minimum-flight thresholds and compare weighted with unweighted summaries.

The complete D1–D12 pack includes discovery, source governance, ingestion/model, quality, metric catalogue, analysis, investigation scenarios, BI, assurance/UAT, independent handover, executive briefing and contribution evidence. A dashboard by itself does not satisfy the commission.

## Fixed core and optional work

**Core:** Eight agreed full-analysis CSVs, January–August 2026. Use one consistent report variant: combined arrival/departure Full Analysis unless a documented variant change is approved. Fix a shortlist of airport/airline segments after profiling; preserve supported route detail for diagnostics. Separate matched-flight delay denominators from all-flight band and cancellation denominators.

**Extensions:** Full-year seasonality, delay-cause attribution, passenger compensation and operational resource optimisation are outside core. Arrival/departure-specific reports or 2025 history require separately registered sources and compatible definitions.

Source support is checked at the Week 2 gate. A required output is blocked until its fields and cohort are verified; it cannot pass acceptance through a generic “data unavailable” disclaimer. An explicitly optional extension may remain unavailable with a reason. See [exact source URLs and verification evidence](data/SOURCE_REGISTER.md).

## Measurable project outcomes

1. Exactly eight unique monthly inputs are registered using the same report variant.
2. All-flight shares and matched-flight mean delay retain their respective denominators.
3. Every shortlisted segment shows eligible months, flight volume and sensitivity to 100/250-flight gates.

All headline metrics require field lineage; five source values and five BI measures must reconcile. DT1–DT10 must be executed, a second member must reproduce the core outputs, and no critical/high defect may remain. These assess delivery quality; real-world savings or service improvement are not claimed.

## Investigation rules

Baseline minimum = 100 eligible flights per airport/airline month; sensitivity = 250. Require at least three eligible months and display coverage out of eight. Compare a declared adverse-punctuality reference consistently across months and order by flight-weighted delay burden. Record excluded low-volume cases. Volume gates are simulated design choices and must not be described as CAA standards.

- Eight months cannot establish full annual seasonality or causal responsibility for delays.
- Average percentages must be weighted with the correct eligible flights; missing/cancelled flights need explicit treatment.
- Aviation performance signals require operational event, weather and schedule evidence before attributing cause.

## Team and stakeholder ownership

Director of Airport Operations & Resilience approves business scope and the investigation recommendation. The Business Analyst, Data Governance Analyst, Data Engineer and BI Developer work with the specialist roles in the [project brief](project/PROJECT_BRIEF.md). Assign individual owners at kickoff and record substantive work and independent reviews in `CONTRIBUTIONS.md`.

## Delivery plan

Weeks 1–2: decision requirements and verified cohort. Weeks 3–4: model, reconciliation and metric definitions. Weeks 5–6: analytical findings, alternative investigation scenarios and BI draft. Weeks 7–8: simulated UAT, independent rerun, executive briefing and handover.

## Start here

1. [Project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. [D1–D12 deliverables and metric contracts](project/DELIVERABLES.md).
3. [AC1–AC12 and DT1–DT10 acceptance tests](project/ACCEPTANCE_CRITERIA.md).
4. [Governance and sign-off](project/GOVERNANCE.md).
5. [Data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw](data/raw/README.md), [reference](data/reference/README.md) and [metadata](data/metadata/README.md) guidance.
6. [Team repository standard](submission/TEAM_REPOSITORY_STANDARD.md), [submission guide](submission/SUBMISSION_GUIDE.md) and [final template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master repository holds the Mettelo-controlled specification. Create `MTL-XF-026-<team-name>` under the **Mettelo GitHub organisation** and add every member's individual account. Delivery analysis, code, tests, BI and contribution evidence belong in that team repository. Use issues, branches, meaningful commits, PRs and reviews where practical.

The required master areas are `project/`, `data/` (including raw/reference/metadata guidance) and `submission/`; [the documentation index](project/README.md) explains their authority and current revision.

**Mettelo — Built for What’s Next**
