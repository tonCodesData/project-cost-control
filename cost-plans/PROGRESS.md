# Project Cost Control Dashboard — Progress Log

## NHS Acute Hospital Wing (£18M)

### Cost Plan Tab
- [x] BCIS elemental structure (elements and sub-elements)
- [x] Column headers — Budget, Authorised Changes, Revised Budget, Committed, Actual to Date, Forecast Final Cost, Variance, % Complete
- [x] Budget figures — £18,000,000 total
- [x] Authorised Changes — £315,000 across 5 packages
- [x] Revised Budget formulas (=C+D)
- [x] Committed figures — £16,020,550 (87.4% of revised budget)
- [x] Actual to Date figures — £13,526,650
- [x] Forecast Final Cost (EAC) — £18,719,000
- [x] Variance formulas — £-404,000 overspend
- [x] % Complete — weighted SUMPRODUCT formulas on element headers, 72% overall
- [x] Conditional formatting — variance RAG
- [x] Row grouping — collapse/expand elements
- [x] Dynamic report date — TODAY() formula

### CVR Tab
- [x] Monthly value vs cost table (October 2025 to March 2026)
- [x] Gross margin calculation
- [x] CPI trend — 1.04 deteriorating to 0.97
- [x] Running EAC — £18.9M at March 2026
- [x] Cumulative value vs cost line chart
- [x] RAG conditional formatting on gross margin column
- [x] Professional formatting — matching cost plan header style

### Project Info Tab
- [x] Basic project details
- [x] Dynamic % complete pulling from Cost Plan

---

## Urban Highway Improvement Scheme (£32M)

### Cost Plan Tab
- [x] NEC4 ECC contract type
- [x] Highway-specific BCIS elemental structure
- [x] Budget figures — £32,000,000 total
- [x] Authorised Changes — £640,000 (contamination, utilities, structures, prelims)
- [x] Revised Budget — £32,640,000
- [x] Committed figures — £23,152,000 (70.9% of revised budget)
- [x] Actual to Date — £14,638,500
- [x] EAC — £33,610,000 (£970,000 overspend, 3.0%)
- [x] Variance — £-970,000
- [x] % Complete — 45% weighted
- [x] Conditional formatting — variance RAG
- [x] Row grouping

### CVR Tab
- [x] 19 months data — September 2024 to March 2026
- [x] CPI running at 0.94 throughout
- [x] Dynamic EAC pulling from Cost Plan revised budget
- [x] Chart — cost consistently ahead of value

### Project Info Tab
- [x] Dynamic % complete pulling from Cost Plan

---

## Government Office Refurbishment (£7.5M)

### Cost Plan Tab
- [x] JCT Intermediate contract type
- [x] Refurbishment-specific BCIS elemental structure
- [x] Budget figures — £7,500,000 total
- [x] Authorised Changes — £200,000 (asbestos, MEP upgrades, prelims)
- [x] Revised Budget — £7,700,000
- [x] Committed figures — £6,594,750 (85.6% of revised budget)
- [x] Actual to Date — £4,893,250
- [x] EAC — £7,760,000 (£60,000 overspend, 0.8%)
- [x] Variance — £-60,000
- [x] % Complete — 64% weighted
- [x] Conditional formatting — variance RAG
- [x] Row grouping

### CVR Tab
- [x] 9 months data — July 2025 to March 2026
- [x] Dynamic EAC pulling from Cost Plan revised budget
- [x] Chart — cost ahead of value throughout

### Project Info Tab
- [x] Dynamic % complete pulling from Cost Plan

---

## Primary School Expansion (£4.2M)

### Cost Plan Tab
- [x] JCT Intermediate contract type
- [x] Education new build BCIS elemental structure
- [x] Budget figures — £4,200,000 total
- [x] Authorised Changes — £78,000 (glazing, IT cabling, playground)
- [x] Revised Budget — £4,278,000
- [x] Committed figures — £4,110,000 (96.1% of revised budget)
- [x] Actual to Date — £4,110,000
- [x] EAC — £4,110,000 (£168,000 underspend, 3.9%)
- [x] Variance — £+168,000
- [x] % Complete — 100%
- [x] Conditional formatting — variance RAG
- [x] Row grouping
- [x] Contingency excluded from overall % complete formula

### CVR Tab
- [x] 7 months data — September 2025 to March 2026
- [x] Value consistently ahead of cost — well managed project
- [x] CPI above 1.0 throughout
- [x] Lines converge at completion — £4,110,000 final cost

### Project Info Tab
- [x] Dynamic % complete pulling from Cost Plan

---

## Data Centre Shell & Core (£22M)

### Cost Plan Tab
- [x] JCT Design and Build contract type
- [x] Data centre specific BCIS elemental structure
- [x] Critical MEP at 50%+ of total budget
- [x] Budget figures — £22,000,000 total
- [x] Authorised Changes — £320,000 (power density, UPS, security)
- [x] Revised Budget — £22,320,000
- [x] Committed figures — £10,165,000 (45.5% of revised budget)
- [x] Actual to Date — £2,825,000
- [x] EAC — £22,510,000 (£190,000 overspend, 0.9%)
- [x] Variance — £-190,000
- [x] % Complete — 11% weighted (MEP-heavy weighting explains gap vs 20% programme completion)
- [x] Conditional formatting — variance RAG
- [x] Row grouping

### CVR Tab
- [x] 2 months data — February 2026 to March 2026
- [x] CPI improving from 0.89 to 0.93
- [x] Early stage cost pressure on power infrastructure

### Project Info Tab
- [x] Dynamic % complete pulling from Cost Plan

---

## Documentation
- [x] PROGRESS.md
- [x] README.md — full portfolio analysis and technical architecture
- [x] Project Build Guide PDF

---

## SQL
- [x] Database and tables
- [x] Portfolio summary view
- [x] Elemental drill-through view
- [x] Python load script

## Power BI
- [ ] Page 1 — Portfolio overview
- [ ] Page 2 — Project drill-through
- [ ] Page 3 — ONS benchmarking
- [ ] Page 4 — Executive summary

## README
- [x] Project overview
- [x] Portfolio results table
- [x] Project narratives
- [x] Architecture explanation
- [x] Skills demonstrated
- [x] EAC methodology note