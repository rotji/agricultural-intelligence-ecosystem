# Tracking System Guide

## 1. Purpose

This guide explains how to maintain the agricultural intelligence registers consistently. The Markdown registers are the initial human-readable source of truth. A future database or application must preserve the same meanings and history.

## 2. Register responsibilities

| Register | Primary purpose |
|---|---|
| OPPORTUNITY_REGISTER.md | What could be pursued and why |
| ACTION_TRACKER.md | What must happen next |
| INVESTIGATION_HISTORY.md | What has been checked and learned |
| DECISION_AND_LEARNING_LOG.md | Why a route was selected, changed or rejected |

Daily briefs preserve dated reporting. Evidence records preserve source provenance and observations.

## 3. Identifier conventions

Use uppercase prefixes and four-digit sequential numbers:
- OPP-0001
- ACT-0001
- INV-0001
- DEC-0001
- EVD-0001

Do not reuse IDs, renumber existing records or create duplicate items. Cross-link related IDs.

## 4. Evidence labels

- L1: verified completed transaction.
- L2: verified quotation from an identifiable source.
- L3: unverified advertisement, seller post or informal quotation.
- L4: qualitative signal or contextual report.

Confidence (high/medium/low/unknown) is a separate assessment. A high-confidence statement that a report was published does not necessarily mean the underlying market claim has been independently verified.

## 5. Opportunity capital levels

- Level 0: zero capital.
- Level 1: low capital.
- Level 2: medium capital.
- Level 3: high capital.
- Level 4: complex or strategic capital.

Record whether the capital classification is evidenced, estimated or unknown. Zero-capital routes may still require time, skills, licensing, trust, transport or other resources.

## 6. Status handling

Opportunity lifecycle: Discovered → Investigating → Validated → Pursuing → Parked or Closed.

Action status: Not started / In progress / Blocked / Completed / Cancelled.

Investigation status: Not started / In progress / Blocked / Concluded.

A status change must include the date, reason and supporting evidence. Never infer completion from silence.

## 7. Review-date rules

Choose review dates based on:
- External deadlines or seasonal windows.
- Expected time to obtain a response or evidence.
- Speed at which market conditions change.
- Cost of delay.
- User's practical availability.

Do not invent a deadline from a speculative assumption. Use Not set when no defensible date exists, and state the condition that should trigger review.

## 8. Daily report integration

The daily report should show:
1. Most important active actions and overdue dependencies.
2. Actions completed since the prior review, with evidence.
3. Changed opportunities and investigations.
4. New discoveries with IDs.
5. Items to reprioritise, park, close or reopen.
6. Next action and review date for active items.

Keep the five-minute front brief compact. Put detailed record changes in the full report.

## 9. Update format

Use dated entries rather than deleting or silently rewriting history:

### Update — YYYY-MM-DD
- Previous status:
- New status:
- New evidence:
- Decision/change:
- Next action:
- Dependency:
- Review date:
- Source references:

## 10. Automation boundary

An automation may analyse and propose register changes. It must not state that a Markdown file was committed unless repository write access was used and GitHub confirmed the operation. If the register is inaccessible, provide a clearly labelled proposed update for later application.
