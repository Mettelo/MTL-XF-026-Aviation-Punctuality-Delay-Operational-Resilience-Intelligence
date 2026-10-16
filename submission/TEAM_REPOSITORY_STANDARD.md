# MTL-XF-026 — Team repository standard

## Ownership

Create `MTL-XF-026-<team-name>` under **Mettelo** and add every member through an individual GitHub account. Record this master URL, reviewed specification commit and final submission commit/tag. The master defines scope; the team repository contains delivery evidence.

## Required areas

```text
README.md
CONTRIBUTIONS.md
data/SOURCE_REGISTER.md
data/raw/
data/reference/
data/metadata/
data/curated/
docs/01-discovery/
docs/02-data-governance/
docs/03-data-model/
docs/04-data-quality/
docs/05-kpi-catalogue/
docs/06-analysis/
docs/07-decision-framework/
docs/08-assurance-uat/
docs/09-technical-handover/
src/
sql/
notebooks/
analysis/
tests/
dashboard/
deliverables/
submission/FINAL_SUBMISSION.md
```

Use implementation folders appropriate to the free toolchain; SQL/notebooks need not duplicate logic. Explain unused areas. Provide environment/dependency versions and a reviewable static dashboard export where interactive access is unavailable.

## Project README and evidence

State the decision, **Director of Airport Operations & Resilience** as the simulated decision owner, approved cohort, core/extension status, run steps, five findings, scenario/shortlist links, limitations, UAT and independent rerun results. Link each D/AC/DT item to its actual artefact, owner, reviewer and state.

Responsibilities are defined once in [the project brief](../project/PROJECT_BRIEF.md). Assign named team owners and review partners. Use issues, meaningful commits, branches, PRs and reviews where practical. One member's bulk upload is insufficient evidence of multidisciplinary contribution. `CONTRIBUTIONS.md` links authored work, reviews and presentation/handover contribution for every member; commit count alone is insufficient.

## Project-specific acceptance

1. Exactly eight unique monthly inputs are registered using the same report variant.
2. All-flight shares and matched-flight mean delay retain their respective denominators.
3. Every shortlisted segment shows eligible months, flight volume and sensitivity to 100/250-flight gates.

Keep actual source support and mandatory blockers visible. Preserve raw/curated separation, manifests and every manual adjustment in code or an auditable record. Never commit credentials, prohibited personal information or invented approvals. Retain the simulated-client declaration in public descriptions.

## Team organisation

The recommended team size is **3–5 people**. Delivery roles describe responsibilities, not separate positions: members can combine complementary business analysis, governance, engineering, analysis/modelling, BI and domain responsibilities. Assign a named owner to each deliverable and use a different team member to review critical calculations and perform the final clean rerun.
