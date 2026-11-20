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
  findings_cvss.csv          Final verified vulnerabilities with CWE, OWASP, severity, and CVSS
  testcase_results.csv       Per-application pass/fail results for the ASVS test cases
  prompts_coded.csv          De-identified participant prompts with codebook codes
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

## Privacy and redactions

This dataset has been de-identified before release:

- Raw automated-tool outputs are **withheld**, as they contain application URLs and
  sensitive configuration.
- Personal information (names, email addresses, passwords) has been **removed** from
  the prompts and replaced with placeholders such as `<EMAIL>` and `<NAME>`.
- Exploit-specific details (payloads, queries, and application URLs) have been
  **removed** from the test-case results; only the pass/fail outcome and a generic
  description of each check are provided.
- Applications and participants are identified only by anonymised IDs.

## Reproducing the analysis

The scripts in `scripts/` read the CSV files in `data/` and produce the metrics and
figures reported in the thesis. See the comments at the top of each script for the
expected input files.



Hamal, P. (2026). *An Empirical Study of Security Vulnerabilities in AI-Generated
Business Applications Developed by Non-Technical Users* [Master's thesis, Asian
Institute of Technology].
