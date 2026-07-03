# Coverage Map Template

The living ledger of the engagement, at `research/{company}/00-coverage-map.md`. Updated at recon, after every compile step, and after every verification batch. It answers one question at a glance: where does the picture stand?

---

```markdown
---
type: Coverage Map
company: {company-slug}
updated: {YYYY-MM-DD}
---

# Coverage Map: {Company}

## Known name collisions

- {Entity sharing the name} ({what it is}) - exclude via {domain / disambiguator}.

## Status by topic

### thesis

| Area | Status | Note |
|---|---|---|
| {why-now forces} | solid | {verified S-date} |
| {moat premise} | needs-verify | {single-source; check against rivals' shipped state} |
| {what must be true} | missing | {not yet gathered} |

### company

{same table shape}

### product

{...}

### buyers

{...}

### competitive

{...}

### activity

{...}

### people

{...}

## Dossier status

| Dossier | Status | Written | Queue pending |
|---|---|---|---|
| thesis | final | {date} | 0 |
| company | in progress | - | 2 |
| ... | | | |
```

---

## Rules

- Three statuses only: **solid** (primary-verified), **needs-verify** (gathered, unverified), **missing** (not yet covered). No fourth state; ambiguity here defeats the ledger's purpose.
- The map records status, never findings. Findings live in gather reports and dossiers.
- Inbound-queue counts come from `ls {topic}/inbound-queue/pending/`, not memory.
