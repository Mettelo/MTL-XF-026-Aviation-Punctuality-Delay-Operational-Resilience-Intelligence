# MTL-XF-026 — Aviation Punctuality, Delay & Operational Resilience Intelligence

**Mettelo Project Studio** · Cross-Functional · Master specification  
**Client:** Confidential Airport Operations & Aviation Strategy Directorate  
**Sector:** Aviation / Transport / Operations  
**Status:** Pre-launch; documentation ready, data acquisition/freeze pending  
**Recommended team:** 6–8 people · **Delivery window:** 8 weeks  
**Master repository:** `Mettelo/MTL-XF-026-Aviation-Punctuality-Delay-Operational-Resilience-Intelligence`

> This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

## Business challenge

**Aviation Punctuality, Delay & Operational Resilience Intelligence.** An airport/aviation operations team needs to identify persistent delay patterns by airport/airline rather than overreacting to a single bad month. The output should support resilience planning and operational-performance review.

Current reporting fragments the evidence needed for a repeatable management review. The team must explain which signals are reliable, which comparisons are valid and where further investigation is needed. No budget, operational failure or improvement outcome is asserted as an observed client fact.

## Commissioned decision

> Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?

The product supports a simulated stakeholder review. A dashboard alone is insufficient: the recommendation must be traceable to governed definitions, a reproducible model, reconciled analysis and a transparent investigation framework.

## Business questions

- Which airport/airline combinations have persistent rather than one-month delays?
- How do flight volumes and route mix affect apparent performance?
- Which delay bands or cancellation measures contribute to deterioration?
- Does a minimum-volume rule alter the investigation shortlist?
- What operational cause evidence is needed before attributing delay to an organisation?

## Approved data and cohort

CAA monthly full-analysis CSVs. Historical punctuality data is retained back many years; 2026 files are small, generally under 1 MB each.

Freeze all eight agreed CAA monthly full-analysis CSVs for January–August 2026. The eight months are the core cohort; do not describe them as a full year or infer annual seasonality. Historical 2025 files are optional extensions with their own source records.

Exact copyable URLs and acquisition gates are in [SOURCE_REGISTER.md](data/SOURCE_REGISTER.md). No raw data is uploaded by this build. Source coverage and size statements inherited from the agreement are expected values until controlled acquisition verifies them; current URLs are not a substitute for a frozen file manifest.

## What the team must build

1. Separate volume, punctuality, delay distribution and cancellation measures; retain route mix and matched-flight coverage.
2. Show three-month persistence and eight-month coverage for each airport/airline segment.
3. Produce up to ten resilience-investigation cases under at least two minimum-flight thresholds and compare weighted with unweighted summaries.

Produce the full D1–D12 delivery pack: discovery, governance, ingestion/model, quality, KPI catalogue, analysis, decision framework, BI, assurance/UAT, handover, executive briefing and contribution record. [Deliverables](project/DELIVERABLES.md) defines locations, dates and evidence for each.

## Core measures

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

## Cross-functional ownership

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Airport Operations & Aviation Strategy Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 026 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 026 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 026 dashboard measures and test every visible filter. |
| Aviation Performance Analyst | Own eligible-flight definitions, five source reconciliations and the eight-month comparability review. |
| Airport Operations Analyst | Translate up to ten persistent patterns into operational investigation questions without asserting delay causes. |
| Operational Assurance Analyst | Test flight weighting, cancellation denominators and sensitivity to at least two volume gates. |

Roles may be combined by a smaller team, but each responsibility needs a named owner. A different member reviews critical calculations and final evidence wherever practical.

## Interpretation rules

- Eight months cannot establish full annual seasonality or causal responsibility for delays.
- Average percentages must be weighted with the correct eligible flights; missing/cancelled flights need explicit treatment.
- Aviation performance signals require operational event, weather and schedule evidence before attributing cause.

## Measurable success

- All source files and transformations have provenance and licence evidence; approved inputs have SHA-256 manifests.
- All headline metrics have tested definitions and source-field lineage.
- At least five published values and five dashboard measures reconcile with declared source rounding.
- At least five findings address the business questions and quantify materiality.
- Up to ten investigation cases have evidence, reason codes, owners and limitations; at least two priority scenarios are compared.
- At least ten UAT scenarios pass or have explicitly accepted low-impact limitations; no critical/high defect remains.
- A second member reproduces the core outputs from the same frozen inputs.

These are delivery acceptance thresholds, not promises of real-world service improvement. See [acceptance criteria](project/ACCEPTANCE_CRITERIA.md).

## Delivery sequence

Weeks 1–2: decision requirements, source inspection and freeze approval. Weeks 3–4: model, reconciliation and KPI definitions. Weeks 5–6: analysis, investigation framework and BI draft. Weeks 7–8: UAT, independent rerun, briefing and handover.

## Start here

1. Read the [project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. Review [deliverables](project/DELIVERABLES.md), [acceptance criteria](project/ACCEPTANCE_CRITERIA.md) and [governance](project/GOVERNANCE.md).
3. Inspect the [data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw guidance](data/raw/README.md), [reference guidance](data/reference/README.md) and [metadata guidance](data/metadata/README.md).
4. Create `MTL-XF-026-<team-name>` under the **Mettelo GitHub organisation**, add each member's individual account and follow the [team repository standard](submission/TEAM_REPOSITORY_STANDARD.md).
5. Use the [submission guide](submission/SUBMISSION_GUIDE.md) and [final submission template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master holds the challenge specification. Teams deliver their analysis and artefacts in their own Mettelo organisation repository. Do not submit team work by replacing this master specification. Use issues, branches, meaningful commits, PRs and reviews to demonstrate actual collaboration.

## Specification map

```text
README.md
project/README.md
project/PROJECT_BRIEF.md
project/BUSINESS_CONTEXT.md
project/DELIVERABLES.md
project/ACCEPTANCE_CRITERIA.md
project/GOVERNANCE.md
data/README.md
data/SOURCE_REGISTER.md
data/raw/README.md
data/reference/README.md
data/metadata/README.md
submission/README.md
submission/TEAM_REPOSITORY_STANDARD.md
submission/SUBMISSION_GUIDE.md
submission/FINAL_SUBMISSION_TEMPLATE.md
```

**Mettelo — Built for What’s Next**
