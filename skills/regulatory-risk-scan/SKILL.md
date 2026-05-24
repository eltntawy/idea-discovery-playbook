---
name: regulatory-risk-scan
description: >-
  Screens software ideas for regulatory, compliance, and platform-policy risks
  before scaling validation or build. Use for regulated markets, compliance risk,
  HIPAA, fintech, legal tech, health AI, or privacy-heavy products.
disable-model-invocation: true
---

# Regulatory Risk Scan

Lightweight **desk scan** — not legal advice. Flag risks so validation and build plans include compliance work.

## When to run

- Health, medical, mental health, children
- Money movement, lending, insurance, crypto
- Legal advice, immigration, employment law automation
- Biometrics, surveillance, scraping at scale
- EU/UK users (GDPR), US state privacy laws, sector rules (HIPAA, PCI, etc.)

Run early in `discovery-playbook` phase 1–2 if any trigger applies.

## Checklist

| Area                    | Questions                                                          |
| ----------------------- | ------------------------------------------------------------------ |
| **Activity regulation** | Is the *activity* regulated even if software is not?               |
| **Data**                | PII, PHI, financial data, minors — storage and processing?         |
| **Claims**              | Does marketing imply licensed outcome (medical, legal, financial)? |
| **Third parties**       | API ToS, app store rules, ad platform policies                     |
| **Geography**           | Which countries/states from day one?                               |
| **AI-specific**         | Automated decisions, disclosure, training data rights              |

## Risk levels

| Level      | Action                                                               |
| ---------- | -------------------------------------------------------------------- |
| **Low**    | Document assumptions; proceed with standard privacy                  |
| **Medium** | Add compliance tasks to v1 scope; consult professional before launch |
| **High**   | Pause scale tests; narrow wedge or pivot; expert review required     |

## Output

Save to `discovery/<topic-slug>/research/YYYY-MM-DD-<slug>-regulatory.md`.

Sections: Facts, Assumptions, **Risk table** (area | level | mitigation | owner), Decision (proceed / narrow / pause), Next step.

Link from `discovery-synthesis` and cap **Strong go** if High risks lack mitigation plan.
