# 07 - ASCII 界面设计

状态：Wireframe Draft v0.1（信息架构草案，未完成用户评审）
基准：`Property Calculation v2.xlsx`。字段与结果应以逐格 Formula Map 为最终依据。
约定：`[          ]` 可编辑输入；`<computed>` 只读计算结果；`(...)` 选择项；`[Button]` 操作。
所有金额均为 placeholder，不能据此判断 Excel 计算已经验证。

## 01. Investment Overview
```text
+-------------------------------------------------------------------+
| PROPERTY INVESTMENT CALCULATOR                                    |
+-------------------------------------------------------------------+
| Overview | Property | Fees | Loan | Renovation | Rental | Schedule |
+-------------------------------------------------------------------+
| Scenario [Property A             ]    [Save? TBD] [Export]        |
|                                                                   |
| Purchase/Loan                         Investment                  |
| Purchase Price     <RM ---.-->        Total Cash Out <RM ---.--> |
| Total Loan         <RM ---.-->        Monthly Cashflow<RM --.--> |
| Monthly Installment<RM ---.-->        Rental Yield   <--.--%>    |
|                                      ROI            <--.--%>      |
+-------------------------------------------------------------------+
| [Review input assumptions]       [Open monthly schedule]          |
+-------------------------------------------------------------------+
```

## 02. Property Information
```text
+-------------------------------------------------------------------+
| PROPERTY INFORMATION                                              |
+-------------------------------------------------------------------+
| Property Name        [________________________]                   |
| Location / State     [________________________]                   |
| Developer            [________________________]                   |
| Completion Year      [________]                                   |
| Tenure               (Freehold) (Leasehold)                       |
| Land Title           [________________________]                   |
| Built-up Size        [________]                                   |
| Bedrooms             [__]  Partition Rooms [__]                  |
| Purchase/Net Price   [RM _____________]                           |
| Bank Value / SPA     [RM _____________]                           |
|                                                                   |
| [Back]                                    [Next: Fees]           |
+-------------------------------------------------------------------+
```

## 03. Purchase & Legal Fees
```text
+-------------------------------------------------------------------+
| PURCHASE COST & FEES                                              |
+-------------------------------------------------------------------+
| Deposit                 [RM _________]                            |
| SPA Legal Fee           <RM _________>   Paid? (Yes/No)           |
| MOT / Transfer Duty     <RM _________>   Transfer [________]      |
| Loan Legal Fee          <RM _________>   Paid? (Yes/No)           |
| Loan Stamp Duty         <RM _________>                            |
| Valuation Fee           [RM _________]                            |
| Vendor Legal Fee        [RM _________]                            |
| MRTA / CRTA             [RM _________]                            |
| Partner Sharing (1)     [RM _________]                            |
| Partner Sharing (2)     [RM _________]                            |
| Other                   [RM _________]                            |
|                                                                   |
| Initial Purchase Costs  <RM _________>                            |
| [Back]                                    [Next: Loan]           |
+-------------------------------------------------------------------+
```
Note: exact editability and fee brackets remain pending cell-level validation.

## 04. Mortgage Calculator
```text
+-------------------------------------------------------------------+
| MORTGAGE                                                          |
+-------------------------------------------------------------------+
| Loan Percentage        [____%]   Tenure [____ years]              |
| Annual Interest Rate   [____%]                                    |
| Base Loan Amount       <RM _________>                             |
| Financed Fees          <RM _________>                             |
| Total Loan Amount      <RM _________>                             |
|                                                                   |
| Monthly Installment    <RM _________>                             |
| Monthly Interest       <RM _________>                             |
| Monthly Principal      <RM _________>                             |
| Net Price Loan         <RM _________>                             |
| Cash Out Loan          <RM _________>                             |
|                                                                   |
| [View Repayment Schedule]                                         |
+-------------------------------------------------------------------+
```

## 05. Renovation Budget
```text
+-------------------------------------------------------------------+
| RENOVATION BUDGET                                                 |
+-------------------------------------------------------------------+
| Item             Quantity    Unit Cost       Need?    Total       |
| Bedroom          [__]        [RM _____]      (Y/N)    <RM --->    |
| Partition Room   [__]        [RM _____]      (Y/N)    <RM --->    |
| Living Room      [__]        [RM _____]      (Y/N)    <RM --->    |
| Aircond          [__]        [RM _____]      (Y/N)    <RM --->    |
| Smart Meter      [__]        [RM _____]      (Y/N)    <RM --->    |
| Door Lock        [__]        [RM _____]      (Y/N)    <RM --->    |
| Other            [__]        [RM _____]      (TBD)    <RM --->    |
|                                                                   |
| Total Renovation <RM __________>                                  |
+-------------------------------------------------------------------+
```

## 06. Whole Unit Rental
```text
+-------------------------------------------------------------------+
| RENTAL - WHOLE UNIT                                               |
+-------------------------------------------------------------------+
| Monthly Rental          [RM _________]                            |
| Agent Commission        [RM _________]                            |
| TA Stamping             [RM _________]                            |
| Operation Cost          [RM _________]                            |
| Internet                [RM _________]                            |
| Other Operating Expense [RM _________]                            |
|                                                                   |
| Monthly Net Rental      <RM _________>                            |
| Net Rental Yield        <____%>                                   |
| [Compare with Room Rental]                                        |
+-------------------------------------------------------------------+
```

## 07. Room Rental
```text
+-------------------------------------------------------------------+
| RENTAL - ROOM BY ROOM                                             |
+-------------------------------------------------------------------+
| Bedroom 1             [RM _________]                              |
| Bedroom 2             [RM _________]                              |
| Bedroom 3             [RM _________]                              |
| Bedroom 4             [RM _________]                              |
| Partition Room 1      [RM _________]                              |
| Partition Room 2      [RM _________]                              |
| ... Additional rooms (availability TBD)                           |
|                                                                   |
| Total Room Rent        <RM _________>                             |
| Rental Expenses        <RM _________>                             |
| Monthly Net Rental     <RM _________>                             |
| Net Rental Yield       <____%>                                    |
+-------------------------------------------------------------------+
```

## 08. Cash Flow & ROI
```text
+-------------------------------------------------------------------+
| MONTHLY CASH FLOW & ROI                                           |
+-------------------------------------------------------------------+
| Rental Model        (Whole Unit) (Room Rental)                    |
| Income             <RM _________>                                |
| Rental Expenses    <RM _________>                                |
| Mortgage Payment   <RM _________>                                |
| Other Expenses     <RM _________>                                |
|                                                                   |
| Net Cash Flow      <RM _________>                                |
| Coverage Status    <Cover / Didn't cover>                        |
| Net Cash Out       <RM _________>                                |
| ROI                <____%>                                       |
| Months Alive       <____>        Years Alive <____>              |
+-------------------------------------------------------------------+
```

## 09. Loan Repayment Schedule
```text
+-------------------------------------------------------------------+
| MONTHLY SCHEDULE                                                  |
+-------------------------------------------------------------------+
| Month | Payment | Interest | Principal | Outstanding | Cashflow   |
|-------+---------+----------+-----------+-------------+------------|
| 1     | RM --   | RM --    | RM --     | RM --       | RM --      |
| 2     | RM --   | RM --    | RM --     | RM --       | RM --      |
| ...   | ...     | ...      | ...       | ...         | ...        |
| N     | RM --   | RM --    | RM --     | RM --       | RM --      |
|                                                                   |
| [Jump to Month ____]    [Export? TBD]                              |
+-------------------------------------------------------------------+
```

## 10. Property Appreciation
```text
+-------------------------------------------------------------------+
| PROPERTY APPRECIATION                                             |
+-------------------------------------------------------------------+
| Starting Market Value   [RM _________]                            |
| Appreciation Rate       [____%]                                   |
| Year / Month            [____]                                    |
|                                                                   |
| Estimated Market Value  <RM _________>                            |
| Outstanding Loan        <RM _________>                            |
| Accumulated Cashflow    <RM _________>                            |
|                                                                   |
| [Open Sell Simulation]                                            |
+-------------------------------------------------------------------+
```

## 11. Selling Simulation
```text
+-------------------------------------------------------------------+
| SELLING SCENARIO                                                  |
+-------------------------------------------------------------------+
| Hold Until (month)      [____]                                    |
| Estimated Market Value  <RM _________>                            |
| Sell @ 90% MV           <RM _________>                            |
| Sell @ 60% MV           <RM _________>                            |
| RPGT Individuals        <TBD>                                     |
| Loan Settlement         <RM _________>                            |
| Profit Scenario 1       <RM _________>                            |
| Profit Scenario 2       <RM _________>                            |
|                                                                   |
| NOTE: selling formula/tax assumptions pending Excel verification. |
+-------------------------------------------------------------------+
```

## 12. Export Summary
```text
+-------------------------------------------------------------------+
| EXPORT SUMMARY                                                    |
+-------------------------------------------------------------------+
| Property Information           [Include? TBD]                    |
| Purchase & Financing           [Include? TBD]                    |
| Renovation                     [Include? TBD]                    |
| Rental & Cash Flow             [Include? TBD]                    |
| Schedule                       [Include? TBD]                    |
| Appreciation / Sale            [Include? TBD]                    |
|                                                                   |
| Summary Preview                                                   |
| +---------------------------------------------------------------+ |
| | Purchase    Loan    Renovation    Rental    Cashflow    Profit | |
| |   --        --        --          --         --         --    | |
| +---------------------------------------------------------------+ |
|                                                                   |
| [Export format TBD]                                               |
+-------------------------------------------------------------------+
```

## Cross-screen behaviors still open
- Persistence, scenario duplication/comparison, export format, recalculation triggers and mobile layout.
- Whether each fee is input-only or computed must be determined by the source formula map.
- The ASCII wireframes define proposed structure only; they are not implementation or calculation acceptance evidence.
