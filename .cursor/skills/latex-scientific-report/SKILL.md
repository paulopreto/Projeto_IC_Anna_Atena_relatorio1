---
description: LaTeX scientific report writing standards for the LCA project.
---

# latex-scientific-report

Assists in writing the IC report according to USP/LaBioCoM standards.

## Document Structure
- **Preamble**: Uses `article` class, `biblatex`/`natbib`, `tikz` for diagrams.
- **Sections**: Resumo, Abstract, Introdução, Justificativa, Objetivos, Materiais e Métodos, Resultados (preliminares), Cronograma, Referências.

## TikZ Conventions
Use TikZ for pipeline diagrams. Standard components:
- `markerless`: purple!15
- `dataset`: blue!15
- `preprocess`: gray!15
- `training`: green!15
- `evaluation`: white!20
- `score`: red!20

## Status Reporting
When reporting project progress:
- Mention the number of active collections (currently 6).
- Document participant dropouts/withdrawals.
- Link biomechanical findings to clinical expert scores.

## BEPE Integration
When mentioning Internationalization:
- Mention FAPESP funding and BEPE fellowship.
- Cite University of North Florida (UNF) and Prof. Dr. Guilherme Manna Cesar as the host.
- Focus on "cross-cultural validation" and "model generalizability" as key BEPE goals.
