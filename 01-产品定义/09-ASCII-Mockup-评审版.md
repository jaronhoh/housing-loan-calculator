# 09 - ASCII UI Mockup v0.2 (GitHub Review)

**Review draft, not implementation.** 2026-10-25. Designed from workbook module groups, not yet numerically verified. Text-only ASCII: no graphical assets. Labels in English for width stability; actual language is open. Legend: `[input]` editable, `<result>` calculated, `{choice}` decision pending, `[action]` button.

## A. Desktop overview (M01-M15)

```text
+----------------------------------------------------------------------------------------+
| PROPERTY INVESTMENT CALCULATOR                                 Scenario: [Property A] |
| [Overview] [Property] [Purchase] [Mortgage] [Renovation] [Rental] [Cash Flow] [Schedule] |
+----------------------------------------------------------------------------------------+
| [Property Name________________] [Location_______________] [Built-up sqft_____]        |
+---------------------+---------------------+----------------------+-------------------+
| TOTAL LOAN          | MONTHLY PAYMENT     | INITIAL CASH OUT     | MONTHLY CASH FLOW |
| <RM 471,768.20>     | <RM ...>            | <RM -6,543.00>       | <RM ...>          |
+---------------------+---------------------+----------------------+-------------------+
| Whole Unit Net Rent <RM ...>     Room Net Rent <RM ...>     Selected MAX <RM ...>      |
| Rental Yield <...%>              ROI <...%>               Coverage <Cover / Not>     |
+----------------------------------------------------------------------------------------+
| Investment Trend (proposed visual)               | Acquisition Breakdown             |
| [Monthly Schedule ->]                            | [Fees] [Renovation] [Cash Out]     |
+----------------------------------------------------------------------------------------+
| [View Formula Sources]   [Compare Scenarios? TBD]   [Export? TBD]                    |
+----------------------------------------------------------------------------------------+
```

## B. Property + Purchase + Mortgage (M01-M03)

```text
+----------------------------------------------------------------------------------------+
| PROPERTY & PURCHASE                                                                   |
+--------------------------------------------+-------------------------------------------+
| PROPERTY INPUT                             | FINANCING                                 |
| Property Name [____________________]        | Net Price [RM____________]                |
| Location      [____________________]        | Bank Value / SPA [RM_________]            |
| Tenure        [____________________]        | Loan % [____]   Years [____]              |
| Developer     [____________________]        | Annual Rate % [____]                      |
| Built-up sqft [________]                    | MRTA / CRTA [RM_________]                 |
| Bedrooms [__]  Partitions [__]              | Loan Legal Fee [RM_________]              |
|                                            | Valuation Fee [RM_________]               |
+--------------------------------------------+-------------------------------------------+
| CALCULATED: Loan Amount <RM...>   Total Loan <RM...>   Monthly PMT <RM...>              |
| Net Price Loan <RM...>       Cash Out Loan <RM...>      Initial Interest <RM...>        |
+----------------------------------------------------------------------------------------+
| FEES: Deposit <RM...> | SPA Legal <RM...> | MOT <RM...> | Stamp <RM...>               |
| SPA Paid? {Paid/Free} | MOT {Once/Twice} | Partner 1/2 <RM...> | Total <RM...>     |
| [Fee Bracket Detail]                          [Next: Renovation]                       |
+----------------------------------------------------------------------------------------+
```

## C. Renovation (M04)

```text
+----------------------------------------------------------------------------------------+
| RENOVATION                                  Need Renovation? {Yes/No}                   |
+----------------------------------------------------------------------------------------+
| ITEM                  QTY         UNIT COST (RM)           AMOUNT (RM)                  |
| Bedroom               [  ]        [             ]         <            >               |
| Partition             [  ]        [             ]         <            >               |
| Living Room           [  ]        [             ]         <            >               |
| Air Conditioning      [  ]        [             ]         <            >               |
| Smart Meter           [  ]        [             ]         <            >               |
| Room Lock             [  ]        [             ]         <            >               |
| Other items           [  ]        [             ]         <            >               |
+----------------------------------------------------------------------------------------+
| Other (special rule) [RM____________]       TOTAL RENOVATION <RM____________>           |
| [Show All Source Rows]                       [Next: Rental]                            |
+----------------------------------------------------------------------------------------+
```

## D. Rental analysis (M06-M08)

```text
+----------------------------------------------------------------------------------------+
| RENTAL ANALYSIS                                                                        |
+--------------------------------------------+-------------------------------------------+
| WHOLE UNIT                                 | ROOM BY ROOM                              |
| Monthly Rent      [RM__________]           | Bed 1 [RM____] Bed 2 [RM____]             |
| Agent Commission  [RM__________]           | Bed 3 [RM____] Bed 4 [RM____]             |
| Operating Rate    [____%]                  | Partition 1 [RM____] 2 [RM____]           |
| TA Stamping       <RM__________>           | Agent / TA / Operating / Internet         |
| Internet          [RM__________]           | [Rate___] <Cost____> [Internet____]       |
| NET RENT          <RM__________>           | NET RENT <RM__________>                   |
| YIELD             <______%>                | YIELD <______%>                           |
+--------------------------------------------+-------------------------------------------+
| EXCEL RULE: MAX(Whole Unit Net, Room Net) = <RM__________>                              |
| Other Investment [RM__________] Return [RM__________]                                  |
| TOTAL RENTAL INCOME <RM____________>             [Next: Cash Flow]                      |
+----------------------------------------------------------------------------------------+
```

## E. Cash flow + expenses (M05/M09/M10)

```text
+----------------------------------------------------------------------------------------+
| INVESTMENT CASH FLOW                                                                   |
+--------------------------------------------+-------------------------------------------+
| MONTHLY INCOME                             | MONTHLY EXPENSE                           |
| Selected Net Rental <RM________>           | Mortgage <RM________>                     |
| Other Return        <RM________>           | Maintenance <RM________>                  |
| TOTAL INCOME       <RM________>            | MLTA <RM________>                         |
|                                            | Quit Rent <RM________>                    |
|                                            | Assessment <RM________>                   |
|                                            | Other <RM________>                        |
+--------------------------------------------+-------------------------------------------+
| MONTHLY CASH FLOW <RM________> | COVERAGE <Cover / Didn't Cover>                       |
| NET CASH OUT <RM________>      | MONTHS ALIVE <___> | YEARS ALIVE <___>                |
| ROI (Excel definition) <____%>  [View Source Formula]                                  |
+----------------------------------------------------------------------------------------+
```

## F. Market comparison + interest coverage (M11/M12)

```text
+----------------------------------------------------------------------------------------+
| MARKET CHECK                                                                           |
| Median Price [RM________]     Median Price/sqft [RM________]                           |
| Financed Price/sqft <RM____>  Current Loan Amount <RM____>                              |
| Market Rank <Below / Above Market Value>                                               |
| Monthly Interest <RM____>     Rental/Interest Coverage <...>                            |
+----------------------------------------------------------------------------------------+
```

## G. Monthly schedule + sale (M13/M14)

```text
+----------------------------------------------------------------------------------------+
| MONTHLY SCHEDULE                Appreciation Rate [3.00%]   Sell 90% / 60%              |
+----------------------------------------------------------------------------------------+
| Month | Interest | Billed | Rental | Expense | Net CF | Principal | Outstanding         |
|-------+----------+--------+--------+---------+--------+-----------+---------------------|
| 1     | <...>    | <...>  | <...>  | <...>   | <...>  | <...>     | <...>               |
| 2     | <...>    | <...>  | <...>  | <...>   | <...>  | <...>     | <...>               |
| 13    | <...>    | <...>  | <...>  | <...>   | <...>  | <...>     | <...>               |
| ...   | ...      | ...    | ...    | ...     | ...    | ...       | ...                 |
+----------------------------------------------------------------------------------------+
| SELECT MONTH [___]  MARKET VALUE <RM________>  ACCUMULATED CASH <RM________>            |
| RPGT (source model) <...%>                                                              |
| SELL AT 90% MV <RM______> PROFIT <RM______>                                              |
| SELL AT 60% MV <RM______> PROFIT <RM______>                                              |
| [Show All Schedule Columns] [Export? TBD]                                               |
+----------------------------------------------------------------------------------------+
```

## H. Export & scenarios (M15)

```text
+----------------------------------------------------------------------------------------+
| INVESTMENT SUMMARY / EXPORT                                                            |
+----------------------------------------------------------------------------------------+
| Property       | Total Loan | Cash Out | Net Rental | Cash Flow | ROI | Sale Profit     |
|----------------+------------+----------+------------+-----------+-----+-----------------|
| Property A     | <...>      | <...>    | <...>      | <...>     | ... | <...>           |
| Property B?    | <...>      | <...>    | <...>      | <...>     | ... | <...>           |
+----------------------------------------------------------------------------------------+
| [Print? TBD]  [Export format? TBD]  [Save scenario? TBD]                                |
+----------------------------------------------------------------------------------------+
```

## I. Mobile adaptation (proposed, not approved)

```text
+------------------------------------+
| Property Calculator                |
| [Overview v] [Property A v]        |
+------------------------------------+
| Total Loan       <RM...>           |
| Monthly Payment  <RM...>           |
| Monthly Cashflow <RM...>           |
+------------------------------------+
| [Property] [Mortgage] [Rental]     |
| [Cash Flow] [Schedule] [Export]    |
+------------------------------------+
```

## Review flags

1. **M08**: Excel automatically uses maximum net rental; the earlier UI draft's manual rental-mode selector was misleading. This mockup corrects the display but does not change Excel behavior.
2. **M10**: ROI is the workbook's nonstandard definition; avoid silently showing a conventional ROI.
3. **M03/M14**: fees and RPGT are *historical workbook calculations*, not current legal advice.
4. **M15**: save, compare, export formats, and authentication are not approved.
5. Source-to-field traceability, numeric precision, and exception cases remain unverified.
