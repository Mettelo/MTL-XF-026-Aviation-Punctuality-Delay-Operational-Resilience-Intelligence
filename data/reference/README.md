# MTL-XF-026 — Reference data and mappings

## Purpose

Maintain the code lists and crosswalks needed to implement this analytical grain:

Month × reporting airport × airline × supported route/destination × service/flight category and all other published dimensions. Preserve scheduled, actual, cancelled and matched-flight denominator distinctions.

Potential references are the publisher's geography/entity identifiers, category hierarchies, period definitions, units, status codes and revision markers. Include only references actually needed by the model. Register any separately downloaded official file as an additional source.

## Required mapping evidence

Each reference needs source/version, licence, valid-from/to dates, key uniqueness, allowed values, business meaning, owner and transformation use. For each crosswalk record source key, target key, relationship cardinality, rationale and treatment of unmapped or changed entities. Quantify 100% of unmatched keys; do not silently drop them or infer a mapping from similar names.

Avoid multiplying facts when a reference is many-to-many. Keep parent totals distinct from child categories. Non-official analyst-created groupings must be labelled as project assumptions and sensitivity-tested where they affect the investigation shortlist.

## Domain constraints

- Eight months cannot establish full annual seasonality or causal responsibility for delays.
- Average percentages must be weighted with the correct eligible flights; missing/cancelled flights need explicit treatment.
- Aviation performance signals require operational event, weather and schedule evidence before attributing cause.

The domain specialist approves category meaning and comparability. The Data Engineer supplies uniqueness, join-cardinality and coverage checks before the reference enters the curated model.
