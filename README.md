# Consent-Document-Ethics-in-Clinical-Trials

## Overview

This repository accompanies the study **"Linguistic Coherence and Ethical Richness in Informed Consent Forms: A Bioethical Analysis of Trial Success Predictors"**, which investigates how ethical and linguistic properties of informed consent forms (ICFs) correlate with clinical trial outcomes. By applying natural language processing (NLP) and statistical inference to a curated dataset of ICFs from completed and terminated trials, the study provides empirical insights into consent quality, ethical communication, and trial viability.

## Repository Structure

```
CONSENT-DOCUMENT-ETHICS-IN-CLINICAL-TRIALS/
├── Data/                      # Cleaned ICFs and metadata
├── R_files/                  # R scripts for statistical models and visualisations
├── research_documents/       # Drafts, supporting literature, and notes
├── .gitignore                # Git exclusions
├── LICENSE                   # License file (MIT)
├── List of Trials.pdf        # Metadata of included clinical trials
├── notebook.ipynb            # Jupyter notebook with NLP analysis
├── README.md                 # Project documentation
├── requirements.txt          # Python dependencies
```

## Project Goals

- Quantify the semantic coherence of ICFs using Sentence-BERT
- Measure ethical clause presence using pattern-based detection
- Examine statistical associations between document features and trial outcomes
- Highlight ethical risks of over-standardisation and information overload

## Methodology

- **Text Embedding**: Sentence-BERT (all-MiniLM-L6-v2) was used to compute document-level cosine similarity.
- **Clause Identification**: Ethical disclosures (e.g., purpose, risks, withdrawal) were detected using regular expressions.
- **Statistical Tests**: Mann–Whitney U and logistic regression models evaluated the impact of linguistic and ethical factors on trial completion.
- **Tools**: Python 3.12.1 for NLP, R 4.3.2 for statistical modelling.

## Key Findings

- Completed trials had significantly **higher semantic similarity** and **greater ethical clause coverage** than terminated trials.
- **Edit distance** (structural variation) was not a significant predictor of trial outcome.
- High **clause counts** negatively predicted trial success, suggesting that complexity may impair comprehension.

## Visual Summary

- Logistic models predicted trial success based on cosine similarity and ethical richness.
- Probability of completion rose steeply with improved semantic coherence.
- Excessive document length or clause density correlated with higher termination risk.

## Reproducibility

You can replicate the analysis using the files in this repository.

### Install dependencies

```bash
pip install -r requirements.txt
```

R scripts in the `R_files/` directory require:

- `tidyverse`
- `ggplot2`
- `broom`
- `ResourceSelection`

See `requirements.txt` and R script headers for full package lists.

## Data Source

ICFs were sourced from publicly available clinical trial records on [ClinicalTrials.gov](https://clinicaltrials.gov/). Document preprocessing and metadata collection methods are documented in `notebook.ipynb`.

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute the code with attribution.

## Citation

Please cite the accompanying study if you use this work:

> Osei, F. (2025). *Statistical Inference and Natural Language Analysis of Consent Document Ethics in Clinical Trials*. Journal of Bioethical Inquiry (forthcoming).  
> https://github.com/Franosei/Consent-Document-Ethics-in-Clinical-Trials

## Contact

**Francis Osei**  
Bayezian Limited
[francis@bayezian.com](mailto:francis@bayezian.com)
