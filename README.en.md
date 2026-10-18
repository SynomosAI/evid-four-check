# evid-four-check

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Domain Profile](https://img.shields.io/badge/domain-law-blue.svg)](domain.manifest.json)
[![Status: RESERVED](https://img.shields.io/badge/status-RESERVED-orange.svg)](domain.manifest.json)
[![MCP Checker](https://img.shields.io/badge/checker-MCP%20tool-8a2be2.svg)](checker.io.json)
[![Privacy by Design](https://img.shields.io/badge/privacy-by--design-2ea44f.svg)](privacy.json)

> **Status: RESERVED (placeholder · open for claiming)** — This repo holds the four-piece industry-access skeleton for the legal electronic-evidence domain, waiting for a qualified operator to claim and fill in real rules.

We break the four-attribute review of electronic evidence into verifiable attributes, so AI only searches and suggests and never decides admissibility.

**Keywords**: electronic evidence · four-attribute review · authenticity · legality · relevance · integrity · chain of custody · domain profile · MCP checker

## Quick Start

This repo is a **domain configuration pack** (not a runnable SDK). Clone it to inspect the four-piece skeleton.

```bash
# 1. Clone
git clone https://github.com/SynomosAI/evid-four-check.git
cd evid-four-check

# 2. Read the domain manifest (attributes / issuer / red lines)
cat domain.manifest.json

# 3. Read the checker I/O contract (MCP tool schema)
cat checker.io.json
```

```bash
# 4. Read the gate map (action friction levels and blocking rules)
cat gate-map.json

# 5. Read the privacy statement (default-off / minimal / withdrawable / erasable)
cat privacy.json
```

## What this domain covers

Four-attribute review of electronic evidence: authenticity, legality, relevance, integrity.

Whether electronic evidence is admitted is the authority of the judiciary. AI can lay out where each of the four dimensions stands, what is missing, and what should be supplemented — it never substitutes for a judge's conclusion.

## Domain identity

| Item | Value |
|---|---|
| Domain ID | `law` (globally unique, never reused) |
| Domain name | Legal · Electronic Evidence |
| Profile version | `domain/1.0` |
| Current status | `RESERVED` |
| Reserved since | 2026-09-12 |

## Attribute list

| Attribute key | Type | Description |
|---|---|---|
| `law.evidence_authenticity` | enum | Authenticity: original vs. derived, known author/time · verified/unverified/disputed/refuted |
| `law.evidence_legality` | enum | Legality: collection means and source · lawful/unlawful/pending_review |
| `law.evidence_relevance` | enum | Relevance: logical link to the fact · direct/indirect/irrelevant |
| `law.evidence_integrity` | enum | Integrity: completeness, no tampering · complete/partial/tampered/unverifiable |
| `law.chain_of_custody` | enum | Chain of custody from collection to submission · documented/incomplete/broken/absent |

## Red lines (machine-readable)

1. No final ruling on authenticity or admissibility — that is the judiciary's authority.
2. No conclusions that substitute for forensic appraisal, notarization, or court findings.
3. No "evidence sufficient" wording when the chain of custody is broken or integrity is in doubt.

> Each red line has a matching blocking rule in `gate-map.json`. The platform validator checks "every red line is covered by a rule" — missing coverage fails validation.

## How to claim

This domain is open to qualified organizations. After claiming:

1. Fork this repo and fill in `operator` and `checker_endpoint`.
2. Calibrate attribute values and red-line wording against current rules.
3. Run the platform-side self-check (all five criteria must pass).
4. Open a PR with qualification evidence and rule references.

## License

Code and configuration are under MIT. Prose content copyrights belong to SynomosAI.

© 2026 SynomosAI. All rights reserved.
