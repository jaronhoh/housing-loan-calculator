# Excel Formula Map — P1 Inventory

Status: **Extracted; numerical parity NOT VERIFIED**.

Source: user-provided `Property Calculation v2.xlsx` (not stored in this public repository).

## Extracted formula counts

| Sheet | Formula cells |
|---|---:|
| Export Summary | 0 |
| Profolio - Profile | 912 |
| Schedule - Schedule | 7,152 |
| **Total** | **8,064** |

Extraction scanned A:M, rows 1–200 for Profile, and A:S, rows 1–450 for Schedule. The source workbook has an Apple Numbers export notice warning that formula results may differ in Excel. The formula inventory is therefore **not** proof of numerical equivalence.

## Initial verified examples

| Cell | Original formula | Cached value |
|---|---|---:|
| `Profolio - Profile!D25` | `=D17*$C$25` | 12000 |
| `Profolio - Profile!E25` | `=E17*$C$25` | 6000 |
| `Schedule - Schedule!P2` | `="Sell @ MV "&P3` | Sell @ MV 90% |
| `Schedule - Schedule!R2` | `="Sell @ MV "&R3` | Sell @ MV 60% |
| `Schedule - Schedule!K3` | `='Profolio - Profile'!B109` | -6543 |
| `Schedule - Schedule!M3` | `='Profolio - Profile'!B55` | 471768.2 |
| `Schedule - Schedule!N3` | `='Profolio - Profile'!B49` | 480000 |

## Next validation
1. Identify editable input cells, calculated cells, and named/cross-sheet references.
2. Group formulas into unique formula patterns; distinguish repeated schedule rows from unique rules.
3. Compare source cached outputs with independent implementations for representative scenarios.
4. Test empty/zero/negative cases, fee brackets, mortgage tenure, rounding and selling scenarios.
5. Ask user to resolve anomalies before changing the original rules.

**Note:** A full cell-level extraction has been generated separately as `Excel_Formula_Map_P1.md` for review. This repository contains the concise inventory; the complete source-derived extraction has not yet been committed.
