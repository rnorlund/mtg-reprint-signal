# Track Record Manifest

This directory holds dated, immutable snapshots of the model's predictions.
Files in this directory are append-only: once committed they will not be
modified or removed. Anyone can verify the SHA-256 below to confirm a
historical snapshot has not been altered.

| Snapshot date | File | Cards | SHA-256 |
|---|---|---|---|
| 2026-05-27 | `2026-05-27_predictions.csv` | 32691 | `c3df03af4c112bcbdfda44c61f8aa5c3076dec9eee2f013073099641ec44f944` |
| 2026-05-27 | `2026-05-27_predictions.json` | 32691 | `d90433e5c10b4db3e492e78702fd7a8714d024cc872ec273528e4a238f0f3252` |

## How to verify

```
shasum -a 256 track_record/2026-05-27_predictions.csv
# should equal:
# c3df03af4c112bcbdfda44c61f8aa5c3076dec9eee2f013073099641ec44f944
```

## How to audit

For any snapshot date X, you can compare its `p_reprint_12mo` field against
which cards Wizards of the Coast actually reprinted between X and X+12 months.
Cards in the top decile of `p_reprint_12mo` should be reprinted at much
higher rates than the population base rate of about 15%.

Held-out verification of this exact methodology on the June 2024 snapshot
hit 95/100 top-100 picks reprinted within 12 months; see
`outputs/validation/2024-06-01/`.
