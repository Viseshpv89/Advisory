# Case Law Memory — Vinpro Advisory Knowledge Base

> This directory is Claude's persistent memory for legal research, case law, and advisory precedents.
> Claude writes to this directory after every substantive advisory session.
> Claude reads from this directory at the start of every session to recall past research.

---

## How It Works

1. **After every advisory query** where case law, statutory interpretation, or a formal opinion was produced, Claude MUST offer to save the research here.
2. **At the start of every session**, Claude reads the index file and relevant domain files to recall past positions.
3. **Cross-referencing** — When a new query arrives, Claude checks if similar facts/issues have been addressed before and builds on prior analysis.

---

## Directory Structure

```
case-law-memory/
├── README.md                     ← This file
├── INDEX.md                      ← Master index of all saved research (searchable)
├── gst/                          ← GST domain memory
│   ├── aggregator-compliance.md  ← Example: Cabbazaar GST position
│   ├── place-of-supply.md
│   └── itc-disputes.md
├── income-tax/                   ← IT domain memory
│   ├── tds-defaults.md
│   └── transfer-pricing.md
├── company-law/                  ← ROC/MCA domain memory
│   ├── director-disqualification.md
│   └── rpt-compliance.md
├── labour/                       ← Labour law domain memory
│   ├── pf-esi-disputes.md
│   └── contractor-vs-employee.md
├── fema/                         ← FEMA domain memory
├── cross-domain/                 ← Matters spanning multiple laws
└── client-positions/             ← Client-specific compliance history
    ├── cabbazaar.md
    └── [other-clients].md
```

## File Format (for each saved research)

Every file in this directory follows this structure:
```markdown
# [Topic Title]
Last Updated: [Date]
Related Files: [links to other relevant memory files]

## Facts Pattern
[When does this research apply? What facts trigger it?]

## Legal Position
[The substantive analysis — sections, interpretation, our view]

## Case Law Cited
[All cases referenced, with confidence markers]

## Circulars/Notifications
[Relevant administrative guidance]

## Cross-References
[Links to related research in this memory system]

## Client History
[Which clients had this issue, what position was taken, outcome]
```
