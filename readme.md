# Voting Made Safe and Easy — Replication Package

This repository contains the replication materials for:

> *Voting Made Safe and Easy: The Impact of e-voting on Citizen Perceptions*  
> Political Science Research and Methods, 1(1): 117–137

The files in this repository allow full replication of the analyses, tables, and figures reported in the article and its online appendix.

---

## 📂 Repository Structure

### Data
- `salta_data.Rdata`  
  Original survey data used in the analysis.
- `datamatch.Rdata`  
  Recoded dataset produced during preprocessing.
- `datamatched.Rdata`  
  Matched dataset used for the main analyses.

### Scripts
- `script1_recoding.R`  
  Recodes raw survey variables.  
  **Input:** `salta_data.Rdata` → **Output:** `datamatch.Rdata`
- `script2_analysis.R`  
  Replicates Tables 1–5 from the paper using matching methods.  
  **Input:** `datamatch.Rdata` → **Output:** `datamatched.Rdata`, `m.out.Rdata`
- `script3_multilev.R`  
  Estimates multilevel models and replicates Figure A4 and Table A4 (Online Appendix 4).  
  **Input:** `datamatched.Rdata`

### Model Files
- `m.out.Rdata`  
  MatchIt object produced during the matching procedure.
- `model.bug`  
  JAGS model specification for multilevel analyses.
- `coda.samples.Rdata`  
  Posterior samples from JAGS estimation.

---

## Replication Order

1. Run `script1_recoding.R`  
2. Run `script2_analysis.R`  
3. Run `script3_multilev.R`

---

## Notes

- All analyses are implemented in **R**, with multilevel models estimated using **JAGS**.
- Scripts are designed to be run sequentially as outlined above.
