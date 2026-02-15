# nyse-python-ai-disclosure-replication

# NYSE Python AI Disclosure – Replication Package

This repository contains the blinded replication package for  
**“Public Signals of Python‑Enabled AI in Finance: Disclosure Patterns and Outcome Claims in NYSE Institutions”** (Financial Innovation, 2026, forthcoming). :contentReference[oaicite:0]{index=0}  

The code reproduces the main text and appendix tables/figures from a single configuration file.

## Repository structure

- `code/` – Python scripts, config file, and notebook
- `data/` – Harmonized firm roster and evidence CSVs (inputs) + analysis workbook (output)
- `figures/` – Main-text and appendix figures (PNG/CSV)
- `appendix/` – Appendix workbook and document
- `MANIFEST.txt` – List of files in the archive

## Quick start

1. **Install dependencies** (Python 3.9+):

   ```bash
   pip install pandas numpy scipy statsmodels pyyaml matplotlib openpyxl xlsxwriter
