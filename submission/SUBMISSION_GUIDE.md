# MTL-XF-026 — Submission guide

## What to submit

Submit the Mettelo organisation team repository URL, final commit/tag, completed `submission/FINAL_SUBMISSION.md`, and links to D1–D12. Use the provided [template](FINAL_SUBMISSION_TEMPLATE.md). The final version must remain reproducible after review; record changes made after submission.

## Before submitting

1. Confirm the repository README states the simulated engagement and commissioned decision: Which airport, airline and supported route combinations show persistent punctuality deterioration across January–August 2026 and warrant operational-resilience investigation?
2. Complete the source manifest and cohort sign-off. Freeze all eight agreed CAA monthly full-analysis CSVs for January–August 2026. The eight months are the core cohort; do not describe them as a full year or infer annual seasonality. Historical 2025 files are optional extensions with their own source records.
3. Link the requirements matrix, model, field lineage, quality/reconciliation evidence and all 8 metric definitions.
4. Link at least five findings and the up-to-ten-case investigation shortlist, including owners, evidence gaps and two compared scenarios.
5. Reconcile at least five headline dashboard measures and test all visible filters; provide a free review path and static export.
6. Execute ten or more UAT scenarios, including all domain cases below. Resolve critical/high defects and disclose any accepted remaining limitations.
7. Have another member reproduce the core outputs using documented steps; retain the run environment, checks and results.
8. Complete contribution evidence for each member and prepare the two-page briefing and 15–20 minute presentation.

## Required domain checks

1. Confirm one source file for each of the eight months and fail on missing or repeated months.
2. Reconcile five airport/airline figures against source cells.
3. Demonstrate flight-weighted average delay differs correctly from an unweighted row mean.
4. Test zero eligible flights, a low-volume route and cancellations excluded from the punctuality denominator.

## Panel presentation

Explain the decision, actual cohort and limitations; demonstrate one source-to-KPI-to-dashboard chain; present five findings; compare two prioritisation scenarios; justify the investigation cases; show one case where action is not supported; describe next evidence-gathering steps and named role ownership.

Expect challenges on definitions, denominators, exclusions, comparability, threshold choices, sensitivity, reproducibility and contribution. Label feedback and approvals as simulated where appropriate. Do not invent contact with real stakeholders.

## Acceptance and changes

Use [AC1–AC12](../project/ACCEPTANCE_CRITERIA.md) to record pass/fail, evidence and reviewer. An unavailable conditional analysis needs a supported explanation and alternative; it cannot be disguised as a result. Source changes require registration, impact review and rerun. Final acceptance is recorded by the simulated Mettelo review panel, not self-certified as a real-client outcome.
