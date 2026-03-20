<div align="center">

# Guilherme Lizardo

**Data Analyst & Backend Developer**

Turning operational chaos into structured systems — dashboards, automations and full-stack tools built around real business problems.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-glizardx-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/glizardx)
[![Email](https://img.shields.io/badge/Email-glizardo171@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:glizardo171@gmail.com)

</div>

---

## Projects

---

### Noise Dosimetry Report System
`FastAPI` `React` `PostgreSQL` `pdfplumber` `WeasyPrint`

End-to-end platform built for an occupational health company, replacing a fully manual process of generating noise exposure reports with a structured digital workflow.

**The problem:** technicians collected field data on paper, then manually typed results into Word documents to produce legally required reports — error-prone and time-consuming.

**What I built:**
- PDF parser that extracts measurement data from SONUS 2 dosimeter exports using multi-pattern regex with confidence scoring and name similarity matching (difflib) — resilient to different firmware versions
- REST API with JWT auth and role-based access (Field Technician vs Administrative Staff)
- Automated PDF report generation compliant with NR-15 and NHO-01 Brazilian regulations
- SHA-256 hashing and immutability enforcement on generated reports (audit trail)
- Full React frontend with field data collection, SONUS 2 upload, review and download flow

**Impact:** report generation time reduced from ~2 hours to under 15 minutes. ~80 reports/month.

---

### Operational Quality Dashboard
`Power BI` `Power Query` `DAX` `Excel`

Analytical dashboard built to monitor operational quality KPIs across a financial services operation (Sicoob client).

**What I built:**
- Dimensional data model (fact + dimension tables) consolidating data from multiple sources
- Individual and team-level performance indicators with drill-down capability
- Automated report refresh, eliminating manual data updates
- Used by coordination and management for decision-making and action plan prioritization

**Stack:** Power BI, Power Query, Modelagem Dimensional, DAX, Excel

---

### Operational Risk Report by Flow
`Power BI` `Power Query` `DAX` `Excel`

Structured risk analysis of document deviations across financial flows for the same client.

**What I built:**
- Analytical base in Power BI to identify recurrence patterns and fault concentration by flow type (PF, PJ, income, address, assets, relationships, tax)
- Cross-referenced operational data with internal compliance manuals to translate technical deviations into regulatory and financial risks
- Delivered executive-level risk mapping with evidence documentation and corrective action prioritization

**Stack:** Power BI, Power Query, DAX, Excel

---

### Microsoft Teams Scraper
`Python` `Playwright` `SQLite` `asyncio`

Automated tool to extract and archive messages, images and files from Microsoft Teams — built out of a real need to preserve institutional communication that would otherwise be lost.

**What I built:**
- Async scraper using Playwright that intercepts Teams' internal API calls across multiple Microsoft domains (chatsvcagg, graph.microsoft.com, substrate.office.com) instead of scraping the DOM — more reliable and complete
- SQLite database to store messages, channels, group chats and metadata with deduplication
- Fallback DOM extraction for content not captured via API interception
- Scheduled execution via `schedule` — runs daily at a configured time, exports messages as `.txt` and media files organized by conversation

**The interesting part:** Teams doesn't offer a simple export API, so the scraper works by intercepting the actual network requests the app makes internally — capturing structured JSON payloads directly.

---

## Skills

| Area | Tools |
|---|---|
| Data & BI | Power BI, Power Query, DAX, Excel, Modelagem Dimensional |
| Backend | Python, FastAPI, SQLAlchemy, PostgreSQL, REST APIs |
| Automation | Playwright, pdfplumber, WeasyPrint, schedule |
| Frontend | React, Vite, Axios |
| Concepts | KPIs, Data Quality, Risk Analysis, JWT Auth, PDF Generation |
