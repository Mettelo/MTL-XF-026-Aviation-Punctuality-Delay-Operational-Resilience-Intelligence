# MTL-XF-026 — Business context

## Organisation and decision owner

**Simulated client:** Confidential Airport Operations & Aviation Strategy Directorate. **Accountable executive:** Director of Airport Operations & Resilience. **Review cadence:** monthly airport/airline performance review.

This fictional directorate/board is an engagement scenario, not an assertion of a real client's circumstances. The source data remains official public/open data.

## Business problem

Operations leaders receive performance summaries that may mix route volumes, cancellation exposure and operated-flight delay. A small route can appear worse than a busy route on a simple row average, while combining airport records can count domestic movements twice. Leadership needs a defensible comparison before deciding which operating patterns deserve a joint resilience investigation.

## Why the current process is insufficient

The current scenario relies on separately prepared reports without a common source/metric contract. The material failure to prevent is specific: Wrong weighting, incompatible denominators, report variants and duplicate airport observations can reverse punctuality comparisons.

This creates uncertainty over which cases need investigation and which comparisons should be rejected. No quantified loss, backlog, budget deficit or service failure is invented as a client fact.

## Stakeholders and decisions

| Simulated stakeholder | Decision / review responsibility |
| --- | --- |
| Director of Airport Operations & Resilience | Accountable for scope, investigation priorities, accepted limitations and final business sign-off. |
| Airport Performance Manager | Own performance diagnostics and coverage checks. |
| Airline Relationship Manager | Take evidence-led questions to airline partners without attributing unverified blame. |
| Operations Planning Lead | Identify schedule, disruption and resource evidence needed for resilience investigation. |
| Aviation Data Steward | Approve report variant, denominators, route categories and airline consolidation. |

## Commissioned decision

Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

## Practical management use case

The monthly review opens an airport/airline segment that has missed the team's declared punctuality reference in at least three months. The Performance Manager compares flight-weighted results and shows whether the signal survives a higher volume gate. The Operations Lead then asks for disruption and schedule evidence; the dashboard alone does not assign responsibility to an airline or airport.

## Current-to-target workflow

1. **Before review:** analyst registers the approved files, coverage and definitions; steward checks the cohort and unresolved exceptions.
2. **At review:** Director of Airport Operations & Resilience opens the overview, then inspects diagnostics and the underlying eligible population before considering a case.
3. **Challenge:** the relevant stakeholder compares the alternative scenario and asks whether the signal survives missingness, comparability and denominator checks.
4. **Action:** each accepted case records investigation type, responsible service role, missing evidence, next review and what finding would reverse the recommendation.
5. **Follow-up:** the next monthly airport/airline performance review records evidence received and the decision, without claiming the analytical signal itself caused an improvement.

## Required analytical response

- Separate volume, punctuality, delay distribution and cancellation measures; retain route mix and matched-flight coverage.
- Show three-month persistence and eight-month coverage for each airport/airline segment.
- Produce up to ten resilience-investigation cases under at least two minimum-flight thresholds and compare weighted with unweighted summaries.

## Measurable project outcomes

1. Exactly eight unique monthly inputs are registered using the same report variant.
2. All-flight shares and matched-flight mean delay retain their respective denominators.
3. Every shortlisted segment shows eligible months, flight volume and sensitivity to 100/250-flight gates.

## Proposed benefit monitoring

At kickoff, record a baseline review process and propose measures for: time to regenerate the agreed evidence pack; proportion of agenda recommendations with a complete evidence chain; and proportion of accepted investigations with a role owner and next review. The target for recommendation traceability and ownership is 100%; regeneration time is measured during the independent rerun, with no fabricated pre-project baseline or claimed reduction. These are proposed management measures, not achieved service benefits.

## Scope and evidence limits

**Core:** Eight agreed full-analysis CSVs, January–August 2026. Use one consistent report variant: combined arrival/departure Full Analysis unless a documented variant change is approved. Fix a shortlist of airport/airline segments after profiling; preserve supported route detail for diagnostics. Separate matched-flight delay denominators from all-flight band and cancellation denominators.

**Extensions:** Full-year seasonality, delay-cause attribution, passenger compensation and operational resource optimisation are outside core. Arrival/departure-specific reports or 2025 history require separately registered sources and compatible definitions.

- Eight months cannot establish full annual seasonality or causal responsibility for delays.
- Average percentages must be weighted with the correct eligible flights; missing/cancelled flights need explicit treatment.
- Aviation performance signals require operational event, weather and schedule evidence before attributing cause.

## Risks, mitigations and escalation

- **Interpretation risk:** Wrong weighting, incompatible denominators, report variants and duplicate airport observations can reverse punctuality comparisons. The domain specialist reviews definitions and DT1–DT10 before sign-off.
- **Source risk:** Monthly directory, first agreed CSV link, method notes and stated reuse constraints verified; all eight payload schemas/checksums and period-specific notices pending. The steward records unresolved items at G1; mandatory gaps block dependent outputs.
- **Decision risk:** prioritisation assumptions may affect which cases appear. Show alternative scenarios, excluded cases and evidence that could change a recommendation.
- **Delivery risk:** limited time or skills can leave undocumented manual steps. Assign a second-member rerun and retain contribution/review evidence throughout the eight weeks.

## Evidence chain

Stakeholder requirement → registered source and valid cohort → governed field/metric → tested transformation → reconciled finding → scenario reason code → investigation owner/evidence request → simulated UAT and sign-off.

Every major recommendation must be traceable through this chain.
