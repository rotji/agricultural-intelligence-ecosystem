# Spreadsheet Operating Model — Google Sheets Companion

**Version:** 1.0  
**Date:** 20 November 2026  
**Status:** Workbook prepared; native Google Sheets connection not yet established.

## 1. Purpose

The spreadsheet is the structured, filterable operating interface for the agricultural intelligence project. It complements the version-controlled Markdown governance and records in GitHub.

The import-ready workbook is named: Agricultural_Intelligence_Ecosystem_Workbook.xlsx

It contains:
- Dashboard
- Product_Catalogue
- Market_Observations
- Producer_Registry
- Opportunity_Register
- Action_Tracker
- Investigation_History
- Evidence_Register
- Decision_Log
- Geography
- Start_Here
- Lists (dropdown reference values)

## 2. Current system-of-record arrangement

Until a verified Google Drive/Sheets connection is available:

- **GitHub repository** rotji/agricultural-intelligence-ecosystem remains the versioned source of truth for governance and registered project records.
- **Workbook** is an importable operational companion for structured viewing, filtering, analysis and data entry.
- The workbook and GitHub are **not synchronised automatically**. A change made in one must be reconciled to the other deliberately.
- Daily automation may read/write GitHub only when its operations are confirmed. It must not claim that it read, wrote or synchronised Google Sheets.

Dataset ownership, sync direction, conflict resolution, audit logging and the cutover gate are now defined in [Synchronization Governance](SYNCHRONIZATION_GOVERNANCE.md). GitHub remains the current master until every cutover check passes.

## 3. Workbook sheet definitions

| Sheet | Responsibility |
|---|---|
| Dashboard | Formula-driven counts of records and opportunity status; not a verification score |
| Product_Catalogue | Open-ended product, processed-form, input, co-product and by-product index |
| Market_Observations | Time- and location-specific market quotations and transactions |
| Producer_Registry | Farms, companies, producer groups, processors, traders and facilities |
| Opportunity_Register | Opportunity hypotheses and lifecycle |
| Action_Tracker | Concrete next steps, dependencies, owners and evidence of completion |
| Investigation_History | Questions, sources consulted, findings and unresolved issues |
| Evidence_Register | Source provenance, claims supported, limitations and related IDs |
| Decision_Log | Actual decisions, rationale, alternatives and outcomes |
| Geography | Nationwide state coverage and Plateau's 17 LGAs |
| Start_Here | User guidance and system boundaries |
| Lists | Dropdown values for data consistency |

## 4. Identifier conventions

Use stable IDs shared with the GitHub registers:
- Product: PRD-0001, PRD-0002, ...
- Entity: ENT-0001, ENT-0002, ...
- Opportunity: OPP-0001, OPP-0002, ...
- Action: ACT-0001, ACT-0002, ...
- Investigation: INV-0001, INV-0002, ...
- Evidence: EVD-0001, EVD-0002, ...
- Decision: DEC-0001, DEC-0002, ...
- Market observation: OBS-0001, OBS-0002, ...

Do not reuse or renumber IDs. Before creating a record, check both the workbook and GitHub register for an existing matching item.

## 5. Core data rules

### Products
The catalogue is open-ended. The former 60-item list is not a limit, nor is 100. Keep raw products, inputs, processed forms, varieties/grades, co-products and by-products distinct where their identity or market use differs. The exact historical 60-item list has not yet been recovered; do not recreate it and label it as the original.

### Market observations
Each observation is tied to a date, location, market level, unit, grade, volume and delivery terms where available. Distinguish asking prices, quotations, completed transactions and qualitative market signals. A quote is not a completed transaction.

### Entities
Directory presence, legal status, operational status, product permissions, stock, quality certification and willingness to partner are separate facts. Record the evidence for each; do not infer one from another.

### Opportunities
A product is not automatically a business opportunity. Opportunity status means:
- Discovered
- Investigating
- Validated
- Pursuing
- Parked
- Closed — completed
- Closed — rejected/irrelevant

Validation of a problem/opportunity is not proof of commercial success or revenue.

### Actions
Only mark Completed when completion evidence is recorded. Use Unassigned or Not set when no owner/date has been established.

## 6. Google Sheets import procedure

1. Download Agricultural_Intelligence_Ecosystem_Workbook.xlsx.
2. Open Google Drive.
3. Use **New → File upload** and select the workbook.
4. In Drive, open the uploaded workbook with Google Sheets.
5. Review imported date formats, formulas, dropdown validations, filters and column widths.
6. Optionally use **File → Save as Google Sheets** to create a native Google Sheets copy. Retain the original .xlsx as the setup baseline.
7. Do not share the workbook publicly unless its contents have been reviewed for confidential or personal information.

The current ChatGPT Google Drive/Sheets connector is not available in this environment, so the file cannot be placed directly into the user's Drive or linked to a native Sheet from this setup session.

## 7. Synchronisation rules until cutover

- GitHub remains canonical. Put proposed spreadsheet edits into Change_Queue with stable IDs and evidence.
- Reconcile approved changes to GitHub explicitly and record confirmed commits in Sync_Log.
- Preserve history; do not silently overwrite previous observations or decisions.
- Do not claim automation or real-time sync.
- Follow SYNCHRONIZATION_GOVERNANCE.md for target dataset owners, one-way snapshot rules and the cutover gate.
- Keep public contact details distinct from private personal data.

## 8. Future integration gate

Before enabling automated Google Sheets updates:
1. Confirm the connector can read the correct Google account and target spreadsheet.
2. Confirm read and write permissions.
3. Define the authoritative store for each record type.
4. Define stable-ID allocation and duplicate detection.
5. Define conflict resolution and append-only history.
6. Test with a non-critical sample row and verify both sides.
7. Only then update the daily automation to use the Sheet.
