# Track Record Manifest

This directory holds dated, immutable snapshots of the model's predictions.
Files in this directory are append-only: once committed they will not be
modified or removed. Anyone can verify the SHA-256 below to confirm a
historical snapshot has not been altered.

| Snapshot date | File | Cards | SHA-256 |
|---|---|---|---|
| 2026-05-27 | `2026-05-27_predictions.csv` | 32691 | `c3df03af4c112bcbdfda44c61f8aa5c3076dec9eee2f013073099641ec44f944` |
| 2026-05-27 | `2026-05-27_predictions.json` | 32691 | `d90433e5c10b4db3e492e78702fd7a8714d024cc872ec273528e4a238f0f3252` |
| 2026-05-31 | `2026-05-31_predictions.csv` | 32691 | `b6039c6b2c51ac354565a2e29158d71cbfc143624507f6dcf10f4d8172536fed` |
| 2026-05-31 | `2026-05-31_predictions.json` | 32691 | `e93be155d392190fbc8ae456c81a685f195e8d404d2566329d1a3e55fc4e5183` |
| 2026-06-01 | `2026-06-01_predictions.csv` | 32691 | `ba259afb68625f263f6132d2f248896282c6652c128a9eb3894882a128ffbc3b` |
| 2026-06-01 | `2026-06-01_predictions.json` | 32691 | `65a88925f85dffe9167af8994946bbd3edbe326d088f4c01efcc0b69e6c68674` |
| 2026-06-02 | `2026-06-02_predictions.csv` | 32691 | `2d7ab5baee28d1fb9f44fbc199536c8aa9439adae546e26e478da3c494efec3a` |
| 2026-06-02 | `2026-06-02_predictions.json` | 32691 | `3076a124cb8dcd1242efe976595edcdc61e4bbec60173c6783b3aef777aa6b94` |
| 2026-06-03 | `2026-06-03_predictions.csv` | 32691 | `68c4111b31dcd638f672096015ec772eae862249ff3ebcda0d810bfa4eb4776d` |
| 2026-06-03 | `2026-06-03_predictions.json` | 32691 | `c66a83f91de36d94a770d43f4f9ae2c199eb299f9df5599bbfee66dbafffc926` |
| 2026-06-04 | `2026-06-04_predictions.csv` | 32691 | `57489d252177812557bcf044654eb6b4c3b82f5b849517aae080ef04dbdd7ed6` |
| 2026-06-04 | `2026-06-04_predictions.json` | 32691 | `ee6994be50e0ba1a39d1c9d852d17ac91787a46d359b739f565dea4a1d5edf3e` |
| 2026-06-05 | `2026-06-05_predictions.csv` | 32691 | `d497410bd6dd0c001464126571972fd18be7624c61d01d26ea44f846cbcf7e2f` |
| 2026-06-05 | `2026-06-05_predictions.json` | 32691 | `4c82bcb7d34f72d3661d7694cb01d4f8f93da3c7c038f4b85978093ce9e07f81` |
| 2026-06-07 | `2026-06-07_predictions.csv` | 32691 | `ca70550856a3549b15ac19b8745c74e01ea19de45d6ae8ae35c9d185cbdc6c53` |
| 2026-06-07 | `2026-06-07_predictions.json` | 32691 | `111cbb30db6916d1a9e3938267af5016501be7b5898ac6cbfa1c72557c9e06e9` |
| 2026-06-08 | `2026-06-08_predictions.csv` | 32691 | `228f69eada43dd21ac3ca71f165db87cdf5a7ab9c318da2fcb66bafc8501ea8e` |
| 2026-06-08 | `2026-06-08_predictions.json` | 32691 | `6f053757c7aee057b8bb0a32f8070bb1e1ab6b11cfe1b90e53f9220cf56aa7e3` |
| 2026-06-09 | `2026-06-09_predictions.csv` | 32691 | `721ebad439be56289003f1e5a8fd55cda210deaf806688527ad43bcbe850a905` |
| 2026-06-09 | `2026-06-09_predictions.json` | 32691 | `62654baab8383d6f16b008e1a0727f5dcdff8d4669756140dc14a28b01b2b2b2` |
| 2026-06-10 | `2026-06-10_predictions.csv` | 32691 | `c98654ca5d6250ab81c43916bb98a496cb728d716fb1cbf248ad8dcbe5d5bd7f` |
| 2026-06-10 | `2026-06-10_predictions.json` | 32691 | `a3fd7d0a153f211948a89950db82a13622ced857fcece33f3f8b6f9cc7afc749` |

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
