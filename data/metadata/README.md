# MTL-XF-026 — Metadata, lineage and freeze evidence

Metadata makes aviation punctuality, delay & operational resilience intelligence reproducible. This folder currently contains guidance; no acquisition manifest or source sign-off is claimed.

## Required records after acquisition

- Source manifest: source ID, exact/resolved URL, retrieval UTC, actual release, filename, bytes, SHA-256, archive members/sheets and coverage.
- Publisher methodology and licence/attribution evidence with provenance and retrieval date.
- Schema and field dictionary: name, type, meaning, units, key role, missing/suppression markers and valid values.
- Business glossary and critical data elements, with named steward and approved definitions.
- Grain, hierarchy and join-cardinality documentation.
- Field-level lineage from raw fields through transformations to each headline metric/dashboard measure.
- Quality profile, row-accounting reconciliation, exclusions, unresolved exceptions and their decision impact.
- Freeze approval, change log and later revision comparisons.

## Model contract

Month × reporting airport × airline × supported route/destination × service/flight category and all other published dimensions. Preserve scheduled, actual, cancelled and matched-flight denominator distinctions.

## Metric definition coverage

- Eligible flight volume: Published matched/eligible flights under the source definition; identify flights excluded from punctuality calculation.
- On-time share: Published on-time percentage under the exact CAA tolerance; recompute only with compatible numerator and denominator.
- Average delay minutes: Flight-weighted average = sum(mean delay × eligible flights) / sum(eligible flights) for compatible rows.
- Severe-delay share: Published or reconstructed delay-band share for a declared threshold; do not invent unreported bands.
- Cancellation share: 100 × cancelled flights / publisher-compatible scheduled flights, only if both are available.
- Month-to-month change: Current on-time share minus previous comparable-month share, in percentage points.
- Persistent-pressure flag: Adverse threshold exceeded in at least three observed months; report available months and volume gate.
- Monthly coverage: Observed eligible months / eight required cohort months.

Every listed metric needs source fields, transformation/formula, valid grain, unit, numerator/denominator, exclusions, zero/missing behaviour, refresh expectation, owner and test reference. Mark conditional metrics unavailable if the actual source cannot support them.

Store actual evidence only; never invent publisher schema, a completed licence review, a checksum or a stakeholder approval. See [source register](../SOURCE_REGISTER.md) and [acceptance criteria](../../project/ACCEPTANCE_CRITERIA.md).
