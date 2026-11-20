# Security Vulnerabilities in AI-Generated Business Applications Developed by Non-Technical Users

Supporting data and analysis for the master's thesis *"An Empirical Study of
Security Vulnerabilities in AI-Generated Business Applications Developed by
Non-Technical Users"* (Asian Institute of Technology).

This repository provides the de-identified and analysed data from a controlled
experiment in which 36 non-technical participants, working in 18 teams, each built
an invoice-management application on Bolt.new or Lovable. Each application was
assessed with four automated tools and manual ASVS-based testing, and the verified
vulnerabilities were classified by CWE, OWASP Top 10:2025, and severity, then
attributed to their origin.

## Repository structure

```
data/
  vulnerability_mapping.csv          Final verified vulnerabilities with CWE, OWASP, severity, and CVSS
  prompts_coding_check.csv          De-identified participant prompts with codebook codes
scripts/
  (analysis scripts used to produce the figures and metrics)
README.md
```

## File descriptions

- **data/vulnerability_mapping.csv and data/method_cvss.csv** — the 20 verified vulnerability categories with their
  CWE, OWASP Top 10:2025 category, severity, CVSS v3.1 vector and score, the number
  of applications affected, whether each was detected by an automated tool or only
  by manual testing, and its attributed origin (platform default, AI implementation
  gap, or prompt-associated).
- **data/prompts_coding_check.csv** — participant prompts with their assigned codebook codes
  (A/B/C) and AI reply codes (R1–R8). Prompts are de-identified.


## Reproducing the analysis

The scripts in `scripts/` read the CSV files in `data/` and produce the metrics and
figures reported in the thesis. See the comments at the top of each script for the
expected input files.
