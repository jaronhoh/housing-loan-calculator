# Property Investment & Mortgage Calculator - Project Status & Handoff

> Canonical project status. Last updated: 2026-10-25 (Asia/Kuala_Lumpur).

## Project identity
- Repository: https://github.com/jaronhoh/housing-loan-calculator
- Default branch: main
- Canonical status file: `docs/PROJECT_STATUS.md`
- Source workbook: `Property Calculation v2.xlsx` (user-supplied; **not committed**)
- Production Site: none verified.

## Current status
| Area | Status | Evidence | Updated |
|---|---|---|---|
| Overall scope | Confirmed | User DEC-001 | 2026-10 |
| Strict Excel compatibility | Confirmed | User DEC-002 | 2026-10 |
| ASCII UI wireframe requirement | Confirmed | User DEC-003 | 2026-10 |
| Formula inventory | Extracted (8,064 cells); parity not verified | `docs/analysis/Excel_Formula_Map_P1.md` | 2026-10-24 |
| PM module requirements and ASCII mockup | Draft for user review | `01-产品定义/08-需求模块清单.md`, `01-产品定义/09-ASCII-Mockup-评审版.md` | 2026-10-25 |
| PM final brief | Draft / not frozen | `01-产品定义/06-最终定型稿.md` | 2026-10-24 |
| PRD | Not started | - | 2026-10-24 |
| Development / tests / deployment | Not started | - | 2026-10-24 |

## Latest release
No development release, deployed site, or production verification.

## Open work and blockers
| Priority | Item | Next action | Evidence |
|---|---|---|---|
| P0 | Excel Formula Map | Classify 8,064 extracted formula cells by dependency and rule; compare calculated outputs | `docs/analysis/Excel_Formula_Map_P1.md` |
| P0 | Calculation parity cases | Compare workbook outputs, conditions and rounding | Not yet executed |
| P1 | UI wireframes | Review new ASCII mockup and Excel-driven module list | `01-产品定义/09-ASCII-Mockup-评审版.md` |
| P1 | Finalize PM brief | Resolve open questions and freeze | `05-开放问题.md` |
| P2 | PRD | Draft after validated requirements | Not started |

## Handoff notes
- Preserve nonstandard formulas exactly unless the user explicitly approves a change.
- Do not assume fee schedule or tax rules reflect current law.
- Do not claim parity tests have passed.
- Do not commit the user's spreadsheet to this public repository without authorization.
- Next: Formula Map and UI review, then finalize brief and PRD.

## Change log (append only)
| Date | Change | Result | Evidence |
|---|---|---|---|
| 2026-10-24 | Initialize requirements records from confirmed DEC-001/002/003 | Documentation prepared; calculation validation pending | User decisions |\n| 2026-10-24 | P1 formula extraction inventory | 8,064 formula cells extracted; numerical parity remains unverified | `docs/analysis/Excel_Formula_Map_P1.md` |

| 2026-10-25 | Add 15 Excel-based requirements modules and expanded ASCII mockup | Drafts committed for GitHub review; user approval and formula parity pending | `01-产品定义/08-需求模块清单.md`, `01-产品定义/09-ASCII-Mockup-评审版.md` |

## Next update
Trigger: Formula Map verified, UI design approved, PM brief frozen, PRD milestone, code/test/deployment change.
