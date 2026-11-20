# Data Synchronisation Governance

**Version:** 1.0  
**Effective date:** 20 November 2026  
**Status:** Approved operating design; pre-cutover. Google Sheets connection and cutover have not been completed.

## 1. Purpose

Define how the GitHub repository and Agricultural Intelligence Google Sheets workbook cooperate without creating duplicate records, conflicting edits, lost history or false claims of synchronisation.

## 2. Two phases — current mode and target mode

### Phase 0 — PRE-CUTOVER (current)

GitHub is the authoritative system of record for all current project registers and governance documents.

The XLSX workbook is a generated baseline companion. Even after the user uploads it into Drive and opens it in Google Sheets, it remains a working copy until the cutover gate is formally completed.

- Do not assume an uploaded XLSX file is a native Google Sheet.
- Do not assume a Google Sheet is connected to ChatGPT or the daily automation.
- Do not edit GitHub master records silently from an unreviewed spreadsheet change.
- Put spreadsheet-originated proposed edits into the workbook's Change_Queue sheet, with an existing record ID, proposed values and evidence.
- Reconcile proposed changes deliberately to the GitHub master and record the confirmed GitHub commit in Sync_Log.
- The daily automation remains GitHub-only. It must not claim to read, write or synchronise Google Sheets.

At the 20 November 2026 setup check, the Google Drive connector was reported as disabled by the administrator and unavailable in this ChatGPT environment. No native Google Sheet ID, connector read test or write test has been verified.

### Phase 1 — Native Sheet created, but not cut over

The user may upload the workbook to Google Drive and save it as a native Google Sheet. That alone does not change canonical ownership.

GitHub remains master until:
- The native Sheet URL and spreadsheet ID are recorded.
- Authorized read and write access are verified.
- A harmless test row can be written and read back.
- The workbook baseline has been backed up.
- Existing records have been migrated and reconciled by stable IDs.
- Formula, date, dropdown, permission and privacy checks pass.
- The cutover decision is recorded.

### Phase 2 — OPERATIONAL CUTOVER (future; requires successful tests and explicit approval)

After the cutover gate passes, Google Sheets becomes the canonical store for defined structured operational records. GitHub remains canonical for governance, long-form knowledge and immutable reports.

There will be one canonical owner per field/dataset. No unrestricted two-way live sync will be used.

## 3. Canonical ownership by dataset

| Dataset | Current owner (pre-cutover) | Target owner after cutover | GitHub's continuing role |
|---|---|---|---|
| Architecture, governance, schemas and operating procedures | GitHub | GitHub | Canonical documents and version history |
| Full dated daily briefs and long-form reports | GitHub | GitHub | Immutable dated archive |
| Product catalogue structured rows | GitHub | Google Sheets | Weekly versioned CSV/JSON snapshot and durable methodology |
| Market observations / price records | GitHub (no live observations yet) | Google Sheets | Append-only dated snapshots |
| Producer, farm, company and facility registry rows | GitHub | Google Sheets | Weekly snapshot; detailed source-backed narratives where necessary |
| Opportunity current-state rows | GitHub | Google Sheets | Weekly snapshot and formal opportunity case notes when needed |
| Action tracker rows | GitHub | Google Sheets | Weekly snapshot; GitHub remains archive of significant decisions and outcomes |
| Investigation index, status, next action and review date | GitHub | Google Sheets | Detailed investigation narratives, source extracts/links and conclusions |
| Evidence source index and metadata | GitHub | Google Sheets | Original public source remains at source; permitted durable evidence files and long-form notes |
| Formal decision rationale and learning narratives | GitHub | GitHub | Canonical decision record; Sheet may show a concise index/link only |
| Geography definitions and official reference hierarchy | GitHub architecture | GitHub | Canonical reference; workbook copy is controlled/read-only |

The table is authoritative. Do not let both systems independently edit the same operational fields after cutover.

## 4. Data flow

### Initial migration at cutover

1. Freeze the GitHub master registers and record the baseline commit SHA.
2. Import current records into the native Google Sheet, retaining all stable IDs and dates.
3. Compare row counts and sample records for every dataset.
4. Resolve duplicates and mapping problems before cutover.
5. Record the native Google Sheet ID, migration timestamp, row counts and GitHub baseline commit in Sync_Log.
6. Approve the cutover explicitly.

### After cutover

- Google Sheets → GitHub: export versioned snapshots of operational tables to data/snapshots/YYYY/MM/ as CSV or JSON. Default cadence is weekly; material action/opportunity changes may be included in a daily snapshot when automation and access support it.
- GitHub → Google Sheets: governance/schema/reference changes only, after review; not a round-trip overwrite of operational rows.
- Full daily briefs remain GitHub files in daily-briefs/. They link to the relevant OPP, ACT, INV, PRD and EVD IDs.
- Formal decisions and their rationale remain GitHub documents; the Sheet keeps only a concise linked index if useful.

Snapshots are archival copies, not a second live master. Never import a snapshot back over the current Sheet as a routine sync operation.

## 5. Stable identifiers and record integrity

Use stable IDs:
- PRD-XXXX — product
- ENT-XXXX — producer/company/facility/entity
- OBS-XXXX — market observation
- OPP-XXXX — opportunity
- ACT-XXXX — action
- INV-XXXX — investigation
- EVD-XXXX — evidence/source
- DEC-XXXX — formal decision

Rules:
1. An ID is assigned once and never changes, even when names or status change.
2. Check for an existing record before creating a new ID.
3. Do not use row numbers as identifiers; sorting/filtering must not change IDs.
4. Before cutover, GitHub allocates IDs. After cutover, the canonical Sheet/authorized writer allocates operational IDs.
5. Only one canonical writer may allocate IDs for a given dataset at a time. If automated writers run concurrently, queue creation requests and serialize allocation.
6. Preserve created date, last updated date, source/evidence links and update history.
7. Market observations are append-only records. A new price observation never overwrites an older observation. Corrections must preserve the original value and record the correction reason/date.

## 6. Conflict resolution

If the same record or field has different values in two systems:
1. Identify which system is the canonical owner for that dataset at that point in the cutover lifecycle.
2. Preserve both versions and their timestamps.
3. Do not auto-merge or overwrite.
4. Put the non-canonical proposal into Change_Queue (pre-cutover) or a conflict/review queue (post-cutover).
5. Compare evidence and decide the accepted value.
6. Update the canonical record once.
7. Record the resolution, evidence, actor/date and affected record ID in Sync_Log and, where material, the relevant investigation/decision history.

The canonical owner wins only for system authority; new evidence from a non-canonical copy may still justify a correction after review.

## 7. Audit log requirements

Every actual import, export, snapshot, reconciliation, failed transfer or cutover event must be recorded in Sync_Log with:
- Sync event ID.
- Timestamp (Africa/Lagos).
- Dataset and record/file IDs.
- Source and destination.
- Direction and operation.
- Result (completed/failed/partial/not attempted).
- Verification reference, including Git commit SHA and/or spreadsheet ID/range where available.
- Row counts or record counts.
- Notes, errors and follow-up action.

Do not log a proposed or planned transfer as completed. A successful write must be followed by a read-back or equivalent verification before it is marked verified.

## 8. Workbook controls

The synchronization-aware workbook includes:
- Sync_Control: current operating phase, dataset owners, flow rules and cutover checklist.
- Sync_Log: append-only audit of confirmed transfers and reconciliations.
- Change_Queue: proposed spreadsheet changes awaiting review while GitHub remains master.

Use Change_Queue for pre-cutover edits. A queued change is not an applied change. Do not delete sync history.

## 9. Cutover gate

The following must all pass before changing operating phase:

1. Workbook uploaded and saved as a native Google Sheet; native URL and ID captured.
2. Google connector or other authorized integration can read the intended Sheet.
3. A harmless test row can be written to a test tab and read back.
4. Current GitHub baseline and workbook are backed up.
5. All structured datasets migrated with stable IDs and reconciled row counts/sample checks.
6. Formulas, dropdowns, date formats, filters and sheet protections validated after import.
7. Sharing permissions and privacy reviewed.
8. Canonical ownership and sync cadence confirmed.
9. User-approved cutover decision recorded.
10. Daily automation updated and tested only after the integration is genuinely available.

A failure at any gate leaves the system in PRE-CUTOVER.

## 10. Failure, recovery and rollback

- On connector or API failure, stop the affected sync attempt; do not repeat writes blindly.
- Preserve failed payloads or proposed changes in a review queue.
- Read current canonical records again before retrying.
- Use GitHub commit history and dated snapshots for recovery.
- Never restore by overwriting current data without comparing the latest canonical version.
- Record recovery steps and the reason for rollback.
- If the Sheet is unavailable, continue with GitHub governance and report generation; clearly disclose that Sheet continuity was not checked.

## 11. Privacy and access

- Keep the native Sheet private to the minimum necessary collaborators.
- Do not place passwords, API keys, personal identification data or unnecessary sensitive contact details in public GitHub files.
- Record public business contact details only where relevant and source-backed.
- Review access permissions before any external sharing.
- Avoid copying third-party source material beyond permitted use; store source URLs and concise evidence notes.

## 12. Current operational instruction

Until the cutover gate has passed:
- GitHub remains the only authoritative master for current registers.
- The generated XLSX/native Sheet is a companion baseline only.
- Proposed spreadsheet edits belong in Change_Queue.
- Confirmed manual reconciliation to GitHub must be recorded in Sync_Log.
- The daily automation must continue using GitHub only and must explicitly disclose that Google Sheets was not synchronised.
