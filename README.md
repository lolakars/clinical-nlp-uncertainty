# Linguistic Uncertainty in Clinical Documentation
**An interpretable, genre-aware NLP analysis for HealthTech applications**

## Overview
This project examines whether simple linguistic features can serve as proxies for clinical uncertainty in real-world medical documentation. Focusing on linguistic hedging and syntactic complexity, the analysis shows that these signals cannot be interpreted uniformly across documentation types.

## Why this matters
HealthTech and clinical NLP systems often rely on lightweight text features to support monitoring, analytics, or decision-making. This project demonstrates that without genre awareness, such features can be misleading: the same linguistic signal may reflect procedural detail, reporting conventions, or epistemic uncertainty depending on the documentation type.

## Dataset
- **MTSamples** (public, de-identified clinical transcription corpus)
- ~5,000 clinical notes across multiple documentation genres

## Methods
- **Hedge rate**: lexicon-based measure of explicit linguistic uncertainty
- **Syntactic complexity**: average sentence length
- **Analysis**: descriptive statistics, ANOVA, and linear regression with interaction terms  
  (`hedge_rate ~ avg_sentence_len × documentation_type`)

## Key findings
- Documentation type strongly shapes sentence structure.
- Linguistic uncertainty varies across note types.
- The relationship between sentence length and uncertainty is **context-dependent**:
  - In surgical notes, longer sentences reflect procedural detail rather than uncertainty.
  - In radiology reports, hedging follows genre conventions and is largely independent of sentence length.

## Takeaway
Linguistic uncertainty and syntactic complexity capture distinct aspects of clinical documentation. Interpretable, context-aware NLP is essential for reliable HealthTech applications.

## Repository structure
- `notebooks/` – analysis notebook
- `results/` – aggregated results and derived features
- `data/` – dataset description (raw data not included)

## Tools
Python · pandas · numpy · statsmodels · matplotlib
