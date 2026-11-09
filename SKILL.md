---
name: hu-legal-mcp-skill
description: Official Hungary (HU) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Hungary Legal Research & Multi-Tier Case Law Skill (`hu-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Hungary (HU)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `ECLI:HU:KURI:2024:100 or 2013. évi V. törvény`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** 113 Járásbíróságok (District Courts across Hungary)
   - **Second Instance (Cantonal / Regional / Appellate):** 20 Törvényszékek (Regional Courts) & 5 Ítélőtáblák (Regional Courts of Appeal: Budapest, Debrecen, Győr, Pécs, Szeged)
   - **Supreme & Constitutional Instance:** Kúria (Supreme Court of Hungary) & Alkotmánybíróság (Constitutional Court)
   - **Primary Tiered Database:** Bírósági Határozatok Gyűjteménye BHGY (eakta.birosag.hu — Járásbíróságok, Törvényszékek, Ítélőtáblák & Kúria) (`https://eakta.birosag.hu/anonimizalt-hatarozatok`)
