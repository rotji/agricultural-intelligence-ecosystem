# Agricultural Intelligence Ecosystem

A continuously expanding intelligence and opportunity-discovery system for agriculture and the agrifood economy.

## Mission

Discover, verify, connect and continuously investigate agricultural products, markets, production locations, supply chains, technologies, organisations, risks and commercial opportunities. Turn evidence into practical decisions and track investigations through to outcomes.

The system covers Plateau State, all Nigerian states and the FCT, and relevant international developments. It does not restrict discovery to a fixed commodity list.

## Operating principles

- **Capability before technology; assemble before building.** Prefer existing providers, partnerships, integration, distribution, implementation and services before proposing new software or infrastructure.
- **Open-ended product discovery.** The product catalogue is an evolving index, not a research boundary. Discover unlisted products, processed forms, inputs, co-products, by-products and residues.
- **Evidence before conclusions.** Distinguish verified transactions, identifiable quotations, unverified claims and qualitative market signals.
- **Continuous investigation.** Significant discoveries receive stable IDs, evidence references, statuses, next actions, dependencies and review dates.
- **No invented progress.** Never report an action as completed or a register as updated without evidence.
- **Broad geography.** Do not narrow research permanently to a few states, LGAs, actors or commodities.
- **Practical opportunity discovery.** Evaluate participation routes from zero-capital to strategic-capital opportunities, with risks and uncertainties.

## Start here

1. [Master System Architecture](docs/MASTER_SYSTEM_ARCHITECTURE.md)
2. [Tracking Governance](docs/CONTINUITY_AND_TRACKING_GOVERNANCE.md)
3. [Tracking System Guide](docs/TRACKING_SYSTEM_GUIDE.md)
4. [Spreadsheet Operating Model](docs/SPREADSHEET_OPERATING_MODEL.md)
5. [Synchronization Governance](docs/SYNCHRONIZATION_GOVERNANCE.md)
6. [Opportunity Register](registers/OPPORTUNITY_REGISTER.md)
7. [Product Catalogue](registers/PRODUCT_CATALOGUE.md)
8. [Action Tracker](registers/ACTION_TRACKER.md)
9. [Investigation History](registers/INVESTIGATION_HISTORY.md)
10. [Decision and Learning Log](registers/DECISION_AND_LEARNING_LOG.md)
11. [Evidence Register](evidence/EVIDENCE_REGISTER.md)

## Repository structure

```text
.
├── README.md
├── docs/
│   ├── MASTER_SYSTEM_ARCHITECTURE.md
│   ├── CONTINUITY_AND_TRACKING_GOVERNANCE.md
│   └── TRACKING_SYSTEM_GUIDE.md
├── registers/
│   ├── OPPORTUNITY_REGISTER.md
│   ├── PRODUCT_CATALOGUE.md
│   ├── ACTION_TRACKER.md
│   ├── INVESTIGATION_HISTORY.md
│   └── DECISION_AND_LEARNING_LOG.md
├── daily-briefs/
│   └── README.md
└── evidence/
    ├── EVIDENCE_REGISTER.md
    └── README.md
```

## Current implementation status

This repository currently establishes the governance and documentation foundation. It is not yet a live commodity database, automated market crawler, transaction-verification service, producer registry or price API. Those capabilities must only be described as implemented after they have actually been built, connected and tested.

Daily research automation is a separate scheduled process. It must consult and update repository records only when repository access and confirmed write operations are available. A report in a chat or automation run is not, by itself, a committed repository update.

## Current initial investigation seeds

The initial 19 November 2026 intelligence brief identified three leads for verification:
- OPP-0001 — Seed-quality and supplier-to-farmer coordination.
- OPP-0002 — Fertiliser distribution coordination.
- OPP-0003 — Grain market-information and sourcing services.

These are discoveries requiring investigation, not validated commercial opportunities.

## Change discipline

Record meaningful architecture decisions and material changes. Preserve history and stable IDs. Do not silently overwrite old evidence or delete closed opportunities.