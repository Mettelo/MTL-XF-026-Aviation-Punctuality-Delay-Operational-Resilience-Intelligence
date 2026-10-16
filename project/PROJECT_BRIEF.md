# MTL-XF-026 — Project brief

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

**Client:** Confidential Airport Operations & Aviation Strategy Directorate. **Decision owner:** Director of Airport Operations & Resilience. **Team:** 6–8. **Duration:** 8 weeks. **Review:** monthly airport/airline performance review.

## Business problem and commission

Operations leaders receive performance summaries that may mix route volumes, cancellation exposure and operated-flight delay. A small route can appear worse than a busy route on a simple row average, while combining airport records can count domestic movements twice. Leadership needs a defensible comparison before deciding which operating patterns deserve a joint resilience investigation.

> Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

## Core deliverable boundary

Eight agreed full-analysis CSVs, January–August 2026. Use one consistent report variant: combined arrival/departure Full Analysis unless a documented variant change is approved. Fix a shortlist of airport/airline segments after profiling; preserve supported route detail for diagnostics. Separate matched-flight delay denominators from all-flight band and cancellation denominators.

**Optional / out of core:** Full-year seasonality, delay-cause attribution, passenger compensation and operational resource optimisation are outside core. Arrival/departure-specific reports or 2025 history require separately registered sources and compatible definitions.

File availability does not prove dimensional support. Before analytical build, the team completes the source→field→metric→deliverable matrix in [data guidance](../data/README.md). Missing mandatory support blocks the gate and requires an approved official replacement or scope decision.

## Analytical model

Month × reporting airport × airline × supported route/destination × service/flight category and all other published dimensions. Preserve scheduled, actual, cancelled and matched-flight denominator distinctions.

The source contract above controls where a general grain description is conditional. Do not create dimensions absent from the approved input.

## Objectives

1. Exactly eight unique monthly inputs are registered using the same report variant.
2. All-flight shares and matched-flight mean delay retain their respective denominators.
3. Every shortlisted segment shows eligible months, flight volume and sensitivity to 100/250-flight gates.

## Business questions

1. Which airport/airline combinations have persistent rather than one-month delays?
2. How do flight volumes and route mix affect apparent performance?
3. Which delay bands or cancellation measures contribute to deterioration?
4. Does a minimum-volume rule alter the investigation shortlist?
5. What operational cause evidence is needed before attributing delay to an organisation?

## Cross-functional delivery model

| Delivery role | Required project contribution |
| --- | --- |
| Business Analyst / Delivery Lead | Map the monthly airport/airline performance review, document eight prioritised user requirements and maintain requirement→deliverable→test links; Director of Airport Operations & Resilience owns business approval. |
| Data Governance Analyst | Own the MTL-XF-026 source/metadata register, cohort decision, licence evidence and 100% headline-measure lineage; resolve the specific risk: Wrong weighting, incompatible denominators, report variants and duplicate airport observations can reverse punctuality comparisons. |
| Data Engineer | Implement the declared facts, keys, hierarchy and join controls; account for every source row and deliver a second-member reproducible run at the chosen MTL-XF-026 scope. |
| BI Developer | Implement the monthly airport/airline performance review overview, diagnostic and quality pages; reconcile five measures and ensure cohort/extension warnings survive filters and export. |
| Aviation Performance Analyst | Own eligible-flight definitions, five source reconciliations and the eight-month comparability review. |
| Airport Operations Analyst | Translate up to ten persistent patterns into operational investigation questions without asserting delay causes. |
| Operational Assurance Analyst | Test flight weighting, cancellation denominators and sensitivity to at least two volume gates. |

Assign named team members and review partners at kickoff; roles may be combined, but a distinct member must review critical calculations and perform the final clean rerun. The executive and operational stakeholder roles are specified in [business context](BUSINESS_CONTEXT.md).

## Required investigation approach

Baseline minimum = 100 eligible flights per airport/airline month; sensitivity = 250. Require at least three eligible months and display coverage out of eight. Compare a declared adverse-punctuality reference consistently across months and order by flight-weighted delay burden. Record excluded low-volume cases. Volume gates are simulated design choices and must not be described as CAA standards.

## Milestones and acceptance

| Gate | Reviewers | Evidence / decision |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Monthly directory, first agreed CSV link, method notes and stated reuse constraints verified; all eight payload schemas/checksums and period-specific notices pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Airport Operations & Resilience + operational stakeholders | Baseline minimum = 100 eligible flights per airport/airline month; sensitivity = 250. Require at least three eligible months and display coverage out of eight. Compare a declared adverse-punctuality reference consistently across months and order by flight-weighted delay burden. Record excluded low-volume cases. Volume gates are simulated design choices and must not be described as CAA standards. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

D1–D12 are defined in [deliverables](DELIVERABLES.md). AC1–AC12 and DT1–DT10 are defined in [acceptance criteria](ACCEPTANCE_CRITERIA.md). No real production deployment, automatic funding/service allocation, private-client data or paid-source dependency is required.
