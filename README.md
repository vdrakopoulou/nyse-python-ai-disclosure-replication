#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Generate a polished GitHub README.md for:
Public Signals of Python-Enabled AI in Finance

This version intentionally removes all findings, percentages, and fixed results
because the research is being revised.

Run:
    python generate_readme.py
    python generate_readme.py --output README.md
    python generate_readme.py --preview

On Windows, try:
    py generate_readme.py --output README.md
"""

from __future__ import annotations

import argparse
from pathlib import Path
from textwrap import dedent


PROJECT_TITLE = "Public Signals of Python-Enabled AI in Finance"
PROJECT_SUBTITLE = "Disclosure Patterns and Outcome Claims in NYSE Institutions"
AUTHOR = "Veliota Drakopoulou"
AFFILIATIONS = "Higher Colleges of Technology; Embry-Riddle Aeronautical University"
SSRN_URL = "https://ssrn.com/abstract=6267458"
SSRN_DOI = "10.2139/ssrn.6267458"
ZENODO_DOI = "10.5281/zenodo.18646800"
ZENODO_URL = f"https://doi.org/{ZENODO_DOI}"


def shield(label: str, message: str, color: str, link: str = "") -> str:
    """Return a GitHub badge in Markdown format."""
    safe_label = label.replace("-", "--").replace(" ", "%20")
    safe_message = message.replace("-", "--").replace(" ", "%20").replace("/", "%2F")
    badge = f"https://img.shields.io/badge/{safe_label}-{safe_message}-{color}?style=for-the-badge"
    return f"[![{label}]({badge})]({link})" if link else f"![{label}]({badge})"


def build_readme() -> str:
    """Build and return the complete README content."""
    ssrn_badge = shield("SSRN", "6267458", "1f77b4", SSRN_URL)
    doi_badge = shield("DOI", SSRN_DOI, "2ca02c", f"https://dx.doi.org/{SSRN_DOI}")
    zenodo_badge = shield("Zenodo", ZENODO_DOI, "ff7f0e", ZENODO_URL)
    python_badge = shield("Python", "Reproducible Research", "3776AB")
    open_science_badge = shield("Open Science", "Replication Ready", "6f42c1")

    return dedent(
        f"""
        # {PROJECT_TITLE}

        ## {PROJECT_SUBTITLE}

        {ssrn_badge}
        {doi_badge}
        {zenodo_badge}
        {python_badge}
        {open_science_badge}

        ---

        > A reproducible research framework for studying public signals of Python-enabled artificial intelligence in NYSE-listed financial institutions.

        ## Project Overview

        Artificial intelligence is increasingly embedded in financial services, yet public evidence of AI use remains fragmented across regulatory filings, corporate communications, recruitment platforms, technology blogs, and sectoral press.

        This repository supports the research paper **{PROJECT_TITLE}: {PROJECT_SUBTITLE}**. It provides a transparent workflow for identifying, classifying, and analyzing public signals of Python-enabled AI capability among New York Stock Exchange financial institutions.

        This GitHub version is designed as a research and replication hub. It focuses on methodology, taxonomy, code structure, and reproducible workflow rather than fixed findings while the study is being updated.

        ---

        ## Research Objectives

        This project investigates how NYSE-listed financial institutions publicly communicate Python-enabled AI capabilities.

        The study seeks to:

        - identify public references to Python, AI, machine learning, analytics, and related software capabilities;
        - classify firms into transparent disclosure states using a reproducible coding framework;
        - detect named Python libraries and map them to AI capability domains;
        - compare disclosure patterns across financial subsectors;
        - evaluate whether firms attach quantified outcome claims to AI and software disclosures;
        - provide a reusable pipeline for future AI-disclosure research.

        The project does **not** claim to measure internal AI adoption directly. It measures publicly observable disclosure signals.

        ---

        ## Disclosure Framework

        Each institution can be coded into one of three disclosure states:

        | Disclosure State | Description |
        |---|---|
        | Explicit Python | Public materials directly reference Python or Python libraries. |
        | Indirect AI | Public materials reference AI, machine learning, automation, or analytics without direct Python evidence. |
        | No Observable Disclosure | No qualifying public signal is identified within the evidence frame. |

        ---

        ## Python Library Mapping

        Detected libraries are mapped to seven analytical dimensions:

        | Dimension | Example Libraries |
        |---|---|
        | Natural Language Processing | spaCy, NLTK, Transformers |
        | Machine Learning | scikit-learn, XGBoost, LightGBM |
        | Deep Learning | TensorFlow, PyTorch, Keras |
        | Reinforcement Learning | Stable-Baselines, RLlib |
        | Probabilistic Modeling | PyMC, Stan, NumPyro |
        | Optimization | SciPy, CVXPY, PuLP |
        | Visualization | Matplotlib, Plotly, Seaborn |

        ---

        ## Outcome Claims Index

        The project includes an **Outcome Claims Index**, or **OCI**, for identifying quantified performance assertions in public disclosures.

        Examples of possible OCI-style claims include:

        - reduced risk exposure;
        - improved fraud detection;
        - faster processing;
        - accuracy gains;
        - cost reductions;
        - productivity improvements.

        The index is intended to separate general AI narratives from measurable claims placed in the public record.

        ---

        ## Suggested Repository Structure

        ```text
        .
        |-- README.md
        |-- LICENSE
        |-- requirements.txt
        |-- pyproject.toml
        |
        |-- data/
        |   |-- raw/
        |   |-- interim/
        |   |-- processed/
        |   `-- dictionaries/
        |
        |-- notebooks/
        |   |-- 01_exploration.ipynb
        |   |-- 02_disclosure_coding.ipynb
        |   |-- 03_library_mapping.ipynb
        |   `-- 04_oci_analysis.ipynb
        |
        |-- src/
        |   |-- collect/
        |   |-- clean/
        |   |-- classify/
        |   |-- detect_libraries/
        |   |-- oci/
        |   |-- statistics/
        |   `-- visualization/
        |
        |-- outputs/
        |   |-- tables/
        |   |-- figures/
        |   `-- logs/
        |
        |-- paper/
        |   |-- manuscript.pdf
        |   `-- citation.bib
        |
        `-- tests/
        ```

        ---

        ## Reproducibility Workflow

        ```bash
        git clone <repository-url>
        cd python-enabled-ai-finance-disclosure
        python -m venv .venv
        source .venv/bin/activate
        pip install -r requirements.txt
        python -m src.clean.prepare_corpus
        python -m src.classify.code_disclosure_states
        python -m src.detect_libraries.match_python_libraries
        python -m src.oci.compute_oci
        python -m src.visualization.make_figures
        ```

        Windows PowerShell activation:

        ```powershell
        .venv\\Scripts\\Activate.ps1
        ```

        ---

        ## Open Science Materials

        - Zenodo DOI: [{ZENODO_DOI}]({ZENODO_URL})
        - SSRN paper: [{SSRN_URL}]({SSRN_URL})
        - SSRN DOI: [{SSRN_DOI}](https://dx.doi.org/{SSRN_DOI})

        ---

        ## Citation

        ```bibtex
        @article{{Drakopoulou2025PythonFinanceAI,
          author = {{{AUTHOR}}},
          title = {{{PROJECT_TITLE}: {PROJECT_SUBTITLE}}},
          year = {{2025}},
          institution = {{{AFFILIATIONS}}},
          doi = {{{SSRN_DOI}}},
          url = {{{SSRN_URL}}}
        }}
        ```

        ---

        ## Author

        **{AUTHOR}**  
        {AFFILIATIONS}

        ---

        ## Open Science Statement

        This project follows open-science principles. Code, documentation, and replication materials are organized to support transparency, reproducibility, and future research on AI disclosure in financial services.

        ---

        ## Status Notice

        This repository is under active revision. Numerical results, tables, percentages, and outcome claims should be treated as provisional until the revised research workflow is finalized.
        """
    ).strip() + "\n"


def write_file(output_path: Path, content: str) -> None:
    """Write content to output_path, creating parent folders when needed."""
    output_path.parent.mkdir(parents=True, exist_ok=True)
    output_path.write_text(content, encoding="utf-8")


def parse_args() -> argparse.Namespace:
    parser = argparse.ArgumentParser(description="Generate a polished GitHub README.md file.")
    parser.add_argument("--output", default="README.md", help="Output path. Default: README.md")
    parser.add_argument("--preview", action="store_true", help="Print README content instead of writing a file")
    return parser.parse_args()


def main() -> None:
    args = parse_args()
    content = build_readme()

    if args.preview:
        print(content)
        return

    output_path = Path(args.output).expanduser().resolve()
    write_file(output_path, content)
    print(f"README generated successfully: {output_path}")


if __name__ == "__main__":
    main()
