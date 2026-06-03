📊 Public Signals of Python-Enabled AI in Finance
Disclosure Patterns and Outcome Claims in NYSE Institutions


Overview

Artificial Intelligence (AI) is reshaping financial services, yet public evidence of AI implementation remains fragmented, inconsistent, and often difficult to verify. At the same time, Python has emerged as the dominant programming language for analytics, machine learning, and model deployment across the financial sector.

This project presents the first systematic mapping of Python-enabled AI disclosure among New York Stock Exchange (NYSE) financial institutions, examining how firms publicly communicate their AI capabilities, software ecosystems, and performance outcomes.

The study analyzes 180 NYSE-listed financial institutions through a triangulated evidence framework incorporating:

SEC and regulatory filings
Corporate websites and investor communications
Recruitment and employer portals
Industry and financial press sources

The resulting dataset provides a subsector-level view of Python adoption, AI disclosure practices, and quantified performance claims across the U.S. financial industry.

Key Findings
Python Disclosure is Widespread
Disclosure Category	Share of Firms
Explicit Python Disclosure	76.7%
Indirect AI Disclosure Only	2.2%
No Public Disclosure	21.1%

A visibility-weighted analysis yields an effective explicit disclosure share of:

Visibility-Weighted Python Disclosure = 0.629

Dominant Technology Stack

Across institutions, a common analytical backbone emerges:

pandas
NumPy
scikit-learn

These libraries are frequently complemented by specialized frameworks tailored to:

Natural Language Processing (NLP)
Credit and risk modeling
Payments analytics
Market microstructure analysis
Optimization and forecasting
Outcome Claims Remain Rare

To assess whether organizations publicly quantify AI benefits, this study introduces the:

Outcome Claims Index (OCI)

OCI identifies statements such as:

"Risk losses reduced by 15%"

"Fraud detection accuracy improved by 23%"

"Processing time decreased by 40%"

Results indicate that quantified outcome claims are exceptionally uncommon.

Across subsectors:

OCI ≈ 0

This suggests that financial institutions rarely place measurable AI performance outcomes into the public record.

Research Contributions

This repository contributes:

A systematic disclosure taxonomy for Python-enabled AI
A replication-ready measurement framework
Library-level mapping of AI technology stacks
Visibility-weighted disclosure metrics
Outcome Claims Index (OCI)
Frequentist and Bayesian inference workflows
A reproducible open-science research pipeline
Analytical Dimensions

Detected Python libraries are mapped into seven AI capability domains:

Dimension	Examples
Natural Language Processing	spaCy, NLTK, Transformers
Machine Learning	scikit-learn, XGBoost
Deep Learning	TensorFlow, PyTorch
Reinforcement Learning	Stable-Baselines, RLlib
Probabilistic Modeling	PyMC, Stan
Optimization	SciPy Optimize, CVXPY
Visualization	Matplotlib, Plotly, Seaborn
Methodology
Sample
180 NYSE-listed financial institutions
Data collection through January 2026
Evidence Triangulation

Each institution was classified into one of three disclosure states:

Explicit Python
Indirect AI
No Observable Disclosure
Detection Framework

Named Python libraries were identified using:

Dictionary matching
Contextual sentence filters
Manual validation procedures
Statistical Analysis
Descriptive analytics
Subsector comparisons
Bayesian estimation for rare-event outcomes
Visibility-weighted disclosure measures
Repository Structure
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
│
├── outputs/
│
├── paper/
│
└── README.md
Reproducibility

All code, processing scripts, analytical workflows, and figure-generation routines used in the study are publicly archived.

Zenodo Archive

https://doi.org/10.5281/zenodo.18646800

SSRN Paper

https://ssrn.com/abstract=6267458

Citation
@article{Drakopoulou2025PythonFinanceAI,
  author = {Drakopoulou, Veliota},
  title = {Public Signals of Python-Enabled AI in Finance: Disclosure Patterns and Outcome Claims in NYSE Institutions},
  year = {2025},
  institution = {Higher Colleges of Technology and Embry-Riddle Aeronautical University},
  doi = {10.2139/ssrn.6267458},
  url = {https://ssrn.com/abstract=6267458}
}
Author

Veliota Drakopoulou

Higher Colleges of Technology (HCT)
Embry-Riddle Aeronautical University

📧 Academic inquiries and collaboration proposals are welcome.

Open Science Statement

This research follows open-science principles. The complete replication package—including preprocessing scripts, analytical workflows, statistical estimation routines, and figure-generation code—is publicly available to support transparency, reproducibility, and future research on AI disclosure in financial services.


