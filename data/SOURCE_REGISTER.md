# MTL-XF-026 — Source register and verification record

**Project:** Aviation Punctuality, Delay & Operational Resilience Intelligence  
**Documentation review:** 16 October 2026  
**State:** official documentation checked; acquired-file validation and freeze approval pending.  
**Steward:** Data Governance Analyst, with the project domain specialist.

## Source/cohort decision

Eight agreed full-analysis CSVs, January–August 2026. Use one consistent report variant: combined arrival/departure Full Analysis unless a documented variant change is approved. Fix a shortlist of airport/airline segments after profiling; preserve supported route detail for diagnostics. Separate matched-flight delay denominators from all-flight band and cancellation denominators.

**Outside core:** Full-year seasonality, delay-cause attribution, passenger compensation and operational resource optimisation are outside core. Arrival/departure-specific reports or 2025 history require separately registered sources and compatible definitions.

## Official publication and methodology references

| Official reference | URL |
| --- | --- |
| CAA 2026 monthly file directory | https://www.caa.co.uk/data-and-analysis/uk-aviation-market/flight-punctuality/uk-flight-punctuality-statistics/2026/ |
| CAA calculation and coverage notes | https://www.caa.co.uk/data-and-analysis/uk-aviation-market/flight-punctuality/uk-flight-punctuality-statistics-notes/ |

References above were inspected for this revision. They establish only the evidence described below; they are not a completed file acquisition, licence clearance or signed freeze.

## Verification findings

The CAA directory lists all eight full-analysis months. Its notes distinguish the combined report from the arrival/departure variant, define gate-time-based delay, and describe all-flight bands including cancellations/unmatched flights. Full-analysis and summary coverage can differ; domestic movements can occur at both reporting airports. The directory requires attribution and states that statistics may not be sold on.

**Field/reference mapping and acquisition instructions:** Before aggregation map actual field names for report month, reporting airport, airline, destination, eligible/matched flights, total flights, cancelled flights, time-band percentages and average delay. Cite the CAA definitions beside the field mapping. Do not assume every percentage shares the matched-flight denominator.

**Remaining status:** Monthly directory, first agreed CSV link, method notes and stated reuse constraints verified; all eight payload schemas/checksums and period-specific notices pending.

## Exact copyable file URLs

Original agreed URLs are retained. Entries labelled required supplement/reference or fallback are explicit changes from the initial pack. Do not silently replace an input with a newer release.

### S1 — January 2026 Full Analysis

```text
https://www.caa.co.uk/Documents/Download/26825/de96ee2c-f138-4043-b7d5-08a1edf7a5c8/1718
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S2 — February 2026 Full Analysis

```text
https://www.caa.co.uk/Documents/Download/26825/de96ee2c-f138-4043-b7d5-08a1edf7a5c8/1723
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S3 — March 2026 Full Analysis

```text
https://www.caa.co.uk/Documents/Download/26825/de96ee2c-f138-4043-b7d5-08a1edf7a5c8/1727
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S4 — April 2026 Full Analysis

```text
https://www.caa.co.uk/Documents/Download/26825/de96ee2c-f138-4043-b7d5-08a1edf7a5c8/1733
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S5 — May 2026 Full Analysis

```text
https://www.caa.co.uk/Documents/Download/26825/de96ee2c-f138-4043-b7d5-08a1edf7a5c8/1738
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S6 — June 2026 Full Analysis

```text
https://www.caa.co.uk/Documents/Download/26825/de96ee2c-f138-4043-b7d5-08a1edf7a5c8/1745
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S7 — July 2026 Full Analysis

```text
https://www.caa.co.uk/Documents/Download/26825/de96ee2c-f138-4043-b7d5-08a1edf7a5c8/1749
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S8 — August 2026 Full Analysis

```text
https://www.caa.co.uk/Documents/Download/26825/de96ee2c-f138-4043-b7d5-08a1edf7a5c8/1753
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

## File validation and licence record

For every actually used input record:

`source_id, role_core_reference_fallback_extension, original_url, resolved_url, retrieved_utc, actual_release, filename, bytes, sha256, format, sheets_or_members, rows, geography, period_start, period_end, grain, schema_version, methodology_evidence, licence_notice, attribution, redistribution_conditions, approved_by, approval_date`

Retain the relevant publication/file notices, including exceptions and third-party conditions. Do not assume all publishers use the same licence. A stated publication licence does not remove the need to check file-specific terms. Keep unverified values pending; never invent a hash or approval.

## Support and freeze decision

Complete the [source-to-deliverable matrix](README.md). The domain specialist verifies actual grain, units, period comparability and supported metrics; the steward verifies identity and reuse terms. Required missing fields block dependent core outputs. Every activated extension is separately registered. Where a fallback is used, record why, which original it replaces, overlap handling and impact on outputs.

If an agreed URL fails, seek the same official archived release and record evidence. A browser format limitation does not prove a file is unavailable, and a successful page fetch does not prove payload integrity. Preserve the frozen version and metadata in the approved location so future website changes do not silently alter the cohort.
