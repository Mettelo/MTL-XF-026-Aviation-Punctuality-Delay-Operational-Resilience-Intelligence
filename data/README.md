# MTL-XF-026 — Data workspace

## Required sources and cohort

CAA monthly full-analysis CSVs. Historical punctuality data is retained back many years; 2026 files are small, generally under 1 MB each.

Freeze all eight agreed CAA monthly full-analysis CSVs for January–August 2026. The eight months are the core cohort; do not describe them as a full year or infer annual seasonality. Historical 2025 files are optional extensions with their own source records.

[Source register and exact URLs](SOURCE_REGISTER.md)

**Current state:** specification only. No raw datasets have been downloaded or uploaded in this build. Expected size, row count and history statements from the earlier agreement require verification against the actual files. Do not mark the cohort frozen until the manifest and metadata are complete.

## Controlled acquisition and preparation

1. Read [SOURCE_REGISTER.md](SOURCE_REGISTER.md); use the exact agreed URLs and official publisher documentation.
2. Validate that the response is the expected CSV/ODS/XLSX/ZIP rather than an error page. Inspect archive contents and sheet names where relevant.
3. Record resolved URL, UTC retrieval, release, coverage, filename, bytes, SHA-256 and licence evidence. Log discrepancies before changing sources.
4. Preserve original bytes in an approved immutable snapshot; later upload only where instructed and redistribution is permitted.
5. Record source fields, types, valid values, suppression, units and publisher methodology in [metadata](metadata/README.md).
6. Implement the analytical grain below, verify keys/cardinality and account for excluded/quarantined records.
7. Reconcile at least five published measures and create curated outputs reproducibly in the team repository.

## Analytical grain

Month × reporting airport × airline × supported route/destination × service/flight category and all other published dimensions. Preserve scheduled, actual, cancelled and matched-flight denominator distinctions.

## Required metric contract

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

## Mandatory quality risks

- Eight months cannot establish full annual seasonality or causal responsibility for delays.
- Average percentages must be weighted with the correct eligible flights; missing/cancelled flights need explicit treatment.
- Aviation performance signals require operational event, weather and schedule evidence before attributing cause.

1. Confirm one source file for each of the eight months and fail on missing or repeated months.
2. Reconcile five airport/airline figures against source cells.
3. Demonstrate flight-weighted average delay differs correctly from an unweighted row mean.
4. Test zero eligible flights, a low-volume route and cancellations excluded from the punctuality denominator.

## Folder ownership

- [raw](raw/README.md): unmodified approved source snapshots; guidance only at present.
- [reference](reference/README.md): governed code lists, hierarchies and crosswalks.
- [metadata](metadata/README.md): source notices, schema, glossary, lineage and manifest evidence.

Curated data, processing code, logs and test results belong in the team delivery repository. Preserve a reproducible boundary between source inputs and generated products. Do not add personal, confidential or paid-source data.
