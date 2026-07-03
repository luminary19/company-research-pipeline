# research/

Working folders land here, one per company, created by `/research-company`. The layout each engagement gets:

```
research/{company-slug}/
├── 00-scope.md                 why this company, what decision, your stated prior
├── 00-recon.md                 the provisional first pass (never the truth)
├── 00-coverage-map.md          the living solid / needs-verify / missing ledger
├── 00-progress.md              one line per session; the backflow log table
├── dossier-thesis.md           the seven dossiers, written one per session
├── dossier-company.md
├── dossier-product.md
├── dossier-buyers.md
├── dossier-competitive.md
├── dossier-activity.md
├── dossier-people.md
├── synthesis.md                the final answer to the scope question
└── {topic}/                    per-topic working evidence
    ├── 01-gather/              gather agents' reports + the compiled merge
    ├── 02-verification/        adversarial verification batches
    └── inbound-queue/
        ├── pending/            findings routed here by other topics, awaiting absorption
        └── archive/            absorbed findings (the move is the audit trail)
```

Raw evidence files are immutable once written: correction happens in dossiers and verification reports, never by editing evidence. If a company's research is sensitive, add `research/{company-slug}/` to `.gitignore` before committing.
