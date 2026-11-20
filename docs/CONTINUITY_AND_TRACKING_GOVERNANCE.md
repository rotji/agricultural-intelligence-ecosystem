# Continuous Investigation and Opportunity Tracking Governance

**Version:** 1.0  
**Date:** 20 November 2026  
**Applies to:** Agricultural Ecosystem Intelligence and Opportunity Discovery System

## 1. Purpose

Ensure that important discoveries, investigations, opportunities, evidence, actions and decisions accumulate over time. A new daily brief must not erase, restart or obscure work already in progress.

## 2. Foundational rule

Every significant discovery must be traceable from identification through investigation, validation, pursuit, completion, rejection or deliberate suspension.

Each active item must have:
- A unique stable identifier.
- A clear problem, question or objective.
- Evidence and source references.
- Current status and priority.
- Next concrete action.
- Dependencies and unresolved questions.
- Review date or revisit condition.
- Update history.

New information must be able to change an item's status or priority and reopen a previously parked or closed item.

## 3. Record types and identifier prefixes

| Record type | Prefix | Example |
|---|---|---|
| Opportunity | OPP | OPP-0001 |
| Action | ACT | ACT-0001 |
| Investigation | INV | INV-0001 |
| Decision | DEC | DEC-0001 |
| Evidence/source record | EVD | EVD-0001 |
| Daily brief | BRF | BRF-2026-11-20 |

IDs are stable and never reused. Link related records explicitly.

## 4. Lifecycle status definitions

### Discovered
A potentially significant signal, problem, solution or opportunity has been captured, but investigation has not yet established its nature or strength.

### Investigating
Evidence, demand, providers, alternatives, access conditions, feasibility or risks are being examined.

### Validated
Sufficient evidence supports the stated problem or opportunity. This does not mean revenue, customer adoption or commercial success has been achieved.

### Pursuing
A deliberate route has been selected and one or more execution actions are underway or authorised.

### Parked
The item is deliberately paused. Record the reason, what would cause it to be revisited and a review date where appropriate.

### Closed — completed
The stated objective has been achieved and completion evidence is recorded. Record the actual outcome, not just the intended result.

### Closed — rejected/irrelevant
Evidence shows the item is not worth pursuing, was incorrect, or is no longer relevant. Record reasons and key evidence. Retain the record.

Closed items can be reopened only when meaningful new evidence or changed conditions justify it. Preserve the old history.

## 5. Priority levels

- **Priority A:** active investigation or action due to strong evidence, urgency, material change or actionable opportunity.
- **Priority B:** meaningful relevance; continue regular monitoring.
- **Discovery queue:** new or poorly understood item awaiting classification and initial investigation.

Priority is independent of lifecycle status. Explain the basis for a priority change.

## 6. Minimum opportunity record

| Field | Required handling |
|---|---|
| ID | Stable OPP identifier |
| Title | Clear, specific description |
| Date discovered | Initial capture date |
| Origin | Brief, source or discovery record |
| Evidence | Links/IDs, level and confidence |
| Problem/demand | What need or gap may exist |
| Geography | Where relevant |
| Product/value chain | Product family, form and stage |
| Existing solutions | Known providers and alternatives |
| Opportunity type | Service, partnership, processing, distribution, etc. |
| Revenue mechanism | Known, proposed or unknown |
| Status | Defined lifecycle state |
| Priority | A, B or discovery queue |
| Objective | What the investigation seeks to establish |
| Next action | Concrete next step |
| Dependency | Access, approval, information or other prerequisite |
| Owner | Named only if actually assigned; otherwise Unassigned |
| Review date | Date or condition for reassessment |
| History | Dated changes and decisions |

## 7. Minimum action record

Every action should include:
- Stable ACT identifier.
- Related opportunity/investigation/decision IDs.
- Action description and expected result.
- Status: Not started, In progress, Blocked, Completed or Cancelled.
- Responsible party, or Unassigned.
- Dependency/blocker.
- Target/review date.
- Completion evidence.
- Last update date.

Do not mark an action completed merely because it was recommended, discussed, attempted or scheduled.

## 8. Daily carry-forward protocol

At the beginning of each research cycle:

1. Retrieve the current repository registers and relevant previous briefs when access is available.
2. Identify active opportunities, investigations and actions.
3. Check for new evidence, changed conditions and deadlines.
4. Record completed actions only when completion evidence is available.
5. Identify overdue and blocked actions, stating why.
6. Update status and priority when evidence supports the change.
7. Decide whether an item should continue, be reprioritised, parked, closed or reopened.
8. Assign a concrete next action and review date to each active item.
9. Check for duplicates before creating a new ID.
10. Summarise important carry-forward items in the front brief and provide the fuller register delta in the report.

If repository/register access fails, state that continuity could not be verified. Provide a proposed update list but do not claim persistent records were read or saved.

## 9. Different time horizons

- **Daily:** action progress, new information, blockers, urgent changes.
- **Weekly:** investigation progress, stalled tasks, dependency resolution and priority reassessment.
- **Monthly:** commercial relevance, provider landscape, economics, feasibility and strategic fit.
- **Quarterly:** architecture, coverage, long-term assumptions and strategic direction.

These are review cadences, not mandatory deadlines for closing an item.

## 10. Transient signals versus durable opportunities

Maintain separate records where needed:
- A one-day asking-price movement is a time-sensitive observation.
- A persistent supply gap may be an enduring opportunity.
- A single seller advertisement is not proof of repeatable demand.
- A completed transaction may support a market claim only for its recorded date, grade, quantity and terms.

Never overwrite an earlier observation to make the latest value appear historical. Preserve timestamps and provenance.

## 11. Decision and closure discipline

Every significant decision should link to the evidence and alternatives considered. Rejections and parked items must retain reasons. Completed objectives must record outcomes and evidence. Do not convert lack of information into a positive or negative conclusion.

## 12. Repository and automation integrity

The Git repository is the intended durable source of truth for project records. A scheduled daily research automation is not itself a persistent database. It must retrieve and write repository content through an authorised, functioning integration before claiming continuity or changes.

Chat messages and daily reports may contain useful information, but they do not constitute a repository commit. Confirm each write and preserve commit history.

## 13. Core operating cycle

**Discover → Record → Investigate → Verify → Decide → Act → Review → Learn → Reprioritise.**
