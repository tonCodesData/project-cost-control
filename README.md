# Project Cost Control Dashboard

A professional construction cost management dashboard built to demonstrate cost management, 
commercial reporting, and data analytics skills in a tier-1 consultancy context.

Built by Mohammad Mamunor Rashid Tonmoy | github.com/tonCodesData

---

## Project Overview

This project simulates the cost management portfolio of Meridian Cost Consultants — a 
fictional QS consultancy managing five live construction projects across healthcare, 
infrastructure, public sector, education, and commercial sectors.

It mirrors the real workflow used by cost managers at firms such as Turner & Townsend, 
Mace, and Faithful+Gould:

- Excel cost plans maintained per project in BCIS elemental format
- Monthly CVR reporting tracking value, cost, margin, CPI and EAC
- SQL Server consolidation layer as single source of truth for portfolio reporting
- Power BI dashboard for executive and client-facing reporting

---

## The Portfolio

| Project | Sector | Value | Status | EAC | Variance |
|---|---|---|---|---|---|
| NHS Acute Hospital Wing | Healthcare | £18,000,000 | In Progress — 72% | £18,719,000 | -£404,000 |
| Urban Highway Improvement Scheme | Infrastructure | £32,000,000 | In Progress — 45% | £33,610,000 | -£970,000 |
| Government Office Refurbishment | Public Sector | £7,500,000 | In Progress — 64% | £7,760,000 | -£60,000 |
| Primary School Expansion | Education | £4,200,000 | Complete — 100% | £4,110,000 | +£168,000 |
| Data Centre Shell & Core | Commercial | £22,000,000 | In Progress — 11% | £22,510,000 | -£190,000 |
| **Total Portfolio** | | **£83,700,000** | | **£86,709,000** | **-£1,456,000** |

---

## Portfolio Analysis

### Overall Position
The portfolio is currently forecast to overspend by £1,456,000 against a total revised 
budget of £86,224,000 — a variance of 1.7%. This is within acceptable tolerance for a 
mixed portfolio at varying stages of completion.

### Project Narratives

**NHS Acute Hospital Wing — £404,000 overspend (2.2%)**
Cost pressure driven by MEP packages — mechanical and electrical installations running 
over budget due to specification changes and extended programme. Preliminaries overspend 
reflects programme delay. CPI deteriorated from 1.04 in April 2024 to 0.97 by October 
2025, triggering a formal cost warning to the client. Contingency partially intact at 
£850,000.

**Urban Highway Improvement Scheme — £970,000 overspend (3.0%)**
Unforeseen contamination discovered during excavation and underground utilities 
diversions have driven cost overruns on earthworks and structures packages. £640,000 
of authorised changes agreed with Transport for Greater Manchester. CPI running at 
0.94 throughout — EAC on a CPI basis suggests £34.5M, but cost manager's judged EAC 
of £33.6M assumes recovery actions in the second half of the programme.

**Government Office Refurbishment — £60,000 overspend (0.8%)**
Minor overspend driven by asbestos discovery during strip out requiring additional 
structural repairs, and MEP specification upgrades requested by HMRC. Well contained — 
the smallest variance in the portfolio in percentage terms on an active project.

**Primary School Expansion — £168,000 underspend (3.9%)**
Only completed project in the portfolio. Delivered under revised budget — contingency 
not fully drawn down, reflecting strong cost management throughout. CPI remained above 
1.0 throughout the programme, value consistently ahead of cost.

**Data Centre Shell & Core — £190,000 overspend (0.9%)**
Early stage project, only 2 months in. Cost pressure emerging on High Voltage Power 
Infrastructure due to increased power density requirements from the client. CPI 
improving from 0.89 in February 2026 to 0.93 in March 2026 as the project settles. 
Too early to draw firm conclusions — position to be monitored closely.

---

## Technical Architecture
Excel Workbooks (per project)
↓
Python (openpyxl + pyodbc)
↓
SQL Server Express (RetailDW)
↓
Power BI Desktop

**Why this architecture?**
Cost plans are maintained in Excel as working documents — the industry standard for 
QS cost management. A Python consolidation script reads all five workbooks and loads 
them into SQL Server, creating a single source of truth for portfolio reporting. 
Power BI connects to SQL Server rather than individual Excel files, avoiding 
maintenance issues and enabling cross-project aggregation and drill-through.

This mirrors how major consultancies increasingly structure their reporting 
infrastructure — Excel at project level, centralised database for portfolio oversight.

---

## Excel Workbook Structure

Each project workbook contains three sheets:

- **Project Info** — client, contract type, value, dates, status
- **Cost Plan** — BCIS elemental breakdown with Budget, Authorised Changes, 
  Revised Budget, Committed, Actual to Date, Forecast Final Cost, Variance, % Complete
- **CVR** — monthly cumulative value vs cost, gross margin, CPI, EAC, line chart

### Key Excel Features Used
- SUMPRODUCT weighted average for % complete (budget-weighted, not simple average)
- Dynamic report date using TODAY() formula
- Conditional formatting RAG on variance column (percentage-based threshold)
- Row grouping for element collapse/expand
- Custom number format for negative variance display
- Dynamic % complete on Project Info pulling from Cost Plan

---

## Repository Structure

cost-plans/     — Five Excel workbooks, one per project
reports/        — Power BI dashboard (.pbix)
data/           — ONS Construction Output Price Index data
README.md       — This file
PROGRESS.md     — Build log

---

## How to Run

### Prerequisites
- Microsoft Excel
- SQL Server 2025 Express
- Python 3.x with openpyxl, pyodbc, pandas
- Power BI Desktop

### Steps
1. Clone the repository
2. Open Excel workbooks in cost-plans/ to review project data
3. Run data_generation/load_to_sql.py to load data into SQL Server
4. Open reports/dashboard.pbix in Power BI Desktop
5. Refresh data source if prompted

---

## Skills Demonstrated

**Cost Management**
- BCIS elemental cost breakdown across five project types
- Authorised change management
- EAC as informed professional judgement vs mechanical CPI calculation
- CVR monthly reporting — value, cost, margin, CPI trend
- Portfolio-level variance analysis and narrative reporting

**Excel**
- SUMPRODUCT weighted averages
- Conditional formatting with formula-based percentage thresholds
- Dynamic formulas — TODAY(), cross-sheet references
- Row grouping and outline
- Professional client-ready formatting

**Data & Reporting**
- SQL Server consolidation of multi-project Excel data
- Power BI portfolio dashboard with drill-through
- ONS construction price index benchmarking

---

## Note on EAC Methodology

Two EAC figures appear in this project:

1. **Cost Plan EAC** — the cost manager's informed professional judgement, 
   drawing on committed contracts, actual spend, site intelligence, subcontractor 
   feedback, and trend analysis. This is the authoritative figure.

2. **CVR EAC** — mechanically calculated as Revised Budget / CPI. More pessimistic 
   than the judged EAC on overspending projects because it assumes current inefficiency 
   continues to completion with no recovery.

The gap between these two figures is intentional and realistic. It reflects the 
professional skill of cost management — the ability to make a defensible, 
evidence-based forecast that goes beyond mechanical calculation.