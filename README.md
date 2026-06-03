# Public Signals of Python-Enabled AI in Finance: Disclosure Patterns and Outcome Claims in NYSE Institutions

[![SSRN](https://img.shields.io/badge/SSRN-6267458-blue)](https://ssrn.com/abstract=6267458)
[![DOI](https://img.shields.io/badge/DOI-10.2139%2Fssrn.6267458-green)](http://dx.doi.org/10.2139/ssrn.6267458)
[![Zenodo](https://img.shields.io/badge/Zenodo-18646800-orange)](https://doi.org/10.5281/zenodo.18646800)
[![Python](https://img.shields.io/badge/Python-AI%20Disclosure-yellow)]()
[![Open Science](https://img.shields.io/badge/Open%20Science-Reproducible-success)]()

---

## Overview

Artificial Intelligence (AI) is reshaping financial services, yet public evidence of AI implementation remains fragmented, inconsistent, and difficult to verify. At the same time, Python has become the dominant programming language for analytics, machine learning, and model deployment across finance.

This repository supports the paper **"Public Signals of Python-Enabled AI in Finance: Disclosure Patterns and Outcome Claims in NYSE Institutions"** by providing a replication-ready framework for mapping Python-enabled AI disclosure across NYSE-listed financial institutions.

The study examines **180 NYSE financial institutions** using a triangulated corpus of:

- Regulatory filings
- Employer and recruitment portals
- Corporate communications
- Investor-facing materials
- Sectoral and financial press sources

Each institution is classified into one of three disclosure states:

1. **Explicit Python disclosure**
2. **Indirect AI disclosure only**
3. **No observable AI/Python disclosure**

---

## Key Findings

| Disclosure Category | Share of Firms |
|---|---:|
| Explicit Python Disclosure | **76.7%** |
| Indirect AI Disclosure Only | **2.2%** |
| No Public Disclosure | **21.1%** |

A visibility-weighted analysis produces an effective explicit disclosure share of:

> **Visibility-Weighted Explicit Python Share = 0.629**

---

## Technology Stack Identified

The analysis shows a common Python analytics backbone across financial institutions:

- **pandas**
- **NumPy**
- **scikit-learn**

Additional libraries are mapped to specialized finance-related AI tasks, including text analytics, tabular risk modeling, payments analytics, market microstructure analysis, optimization, probabilistic modeling, and visualization.

---

## Analytical Dimensions

Detected Python libraries are mapped into seven analytical dimensions:

| Dimension | Example Libraries |
|---|---|
| Natural Language Processing | spaCy, NLTK, Transformers |
| Machine Learning | scikit-learn, XGBoost |
| Deep Learning | TensorFlow, PyTorch |
| Reinforcement Learning | Stable-Baselines, RLlib |
| Probabilistic Modeling | PyMC, Stan |
| Optimization | SciPy Optimize, CVXPY |
| Visualization | Matplotlib, Plotly, Seaborn |

---

## Outcome Claims Index

The paper introduces an **Outcome Claims Index (OCI)** to identify quantified public claims about AI performance, such as:

- Risk reduction
- Accuracy gains
- Fraud detection improvements
- Processing-time reductions
- Cost or efficiency improvements

The findings show that quantified outcome claims are extremely rare across subsectors:

> **OCI values are effectively zero across subsectors.**

This suggests that while Python-enabled AI capabilities are widely signaled, measurable performance outcomes are rarely disclosed in the public record.

---

## Methodology

### Sample

- **180 NYSE-listed financial institutions**
- Observation window through **January 2026**

### Evidence Triangulation

Sources are combined across regulatory, corporate, labor-market, and sectoral evidence channels to improve robustness and reduce reliance on a single disclosure venue.

### Library Detection

Named Python libraries are detected through:

- Sentence-level dictionary matching
- Contextual filters
- Manual validation
- Domain mapping into AI capability categories

### Statistical Analysis

The study applies:

- Descriptive disclosure analysis
- Subsector comparison
- Visibility-weighted disclosure estimation
- Rare-event inference
- Frequentist and Bayesian approaches for sparse outcome claims

---

## Repository Structure

```text
├── data/
│   ├── raw/
│   ├── processed/
│   └── disclosure_classifications/
│
├── notebooks/
│   ├── exploratory_analysis.ipynb
│   ├── oci_estimation.ipynb
│   └── visualization.ipynb
│
├── src/
│   ├── preprocessing/
│   ├── disclosure_detection/
│   ├── library_mapping/
│   ├── oci_analysis/
│   └── visualization/
│
├── figures/
├── outputs/
├── paper/
└── README.md
```

---

## Reproducibility

This project follows open-science principles. The complete replication package, including scripts for preprocessing, model estimation, and figure generation, is permanently archived on Zenodo.

### Zenodo Archive

https://doi.org/10.5281/zenodo.18646800

### SSRN Paper

https://ssrn.com/abstract=6267458

---

## Citation

```bibtex
@article{Drakopoulou2025PythonFinanceAI,
  author = {Drakopoulou, Veliota},
  title = {Public Signals of Python-Enabled AI in Finance: Disclosure Patterns and Outcome Claims in NYSE Institutions},
  year = {2025},
  institution = {Higher Colleges of Technology and Embry-Riddle Aeronautical University},
  doi = {10.2139/ssrn.6267458},
  url = {https://ssrn.com/abstract=6267458}
}
```

---

## Author

**Veliota Drakopoulou**  
Higher Colleges of Technology  
Embry-Riddle Aeronautical University

---

## Keywords

`NYSE` · `Financial Institutions` · `Python` · `Artificial Intelligence` · `Disclosure` · `Outcome Claims Index` · `Replication` · `Open Science`
"""


def write_readme(output_path: str = "README.md") -> Path:
    """Write the GitHub README file and return the created path."""
    path = Path(output_path)
    path.write_text(README_TEXT, encoding="utf-8")
    return path


if __name__ == "__main__":
    created_file = write_readme()
    print(f"README generated successfully: {created_file.resolve()}")
