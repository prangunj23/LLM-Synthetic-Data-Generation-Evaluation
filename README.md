# LLM Synthetic Data Generation & Evaluation

Research project exploring the use of large language models (LLMs) to generate synthetic conversational data and evaluate how well that data captures the statistical and semantic properties of real-world online communities.

## Overview

This project investigates whether LLM-generated synthetic conversations can reproduce meaningful characteristics of naturally occurring online discourse.

The study uses conversational data from online gaming communities, including **Reddit and Dota 2**, and compares real and synthetic data along multiple dimensions:

* **Distributional similarity** — comparing statistical properties of real and generated conversations
* **Semantic similarity** — measuring whether synthetic conversations preserve the semantic structure of real data
* **Classification** — training classifiers to distinguish between real and synthetic examples
* **Feature attribution** — identifying linguistic and semantic features that differentiate generated and human-authored content
* **Generative modeling** — using LLMs to produce synthetic conversational data under controlled prompts

## Research Questions

The project investigates several questions:

1. How closely can LLM-generated conversations reproduce the statistical properties of real online communities?
2. What semantic characteristics are preserved or lost during synthetic generation?
3. Can downstream models distinguish synthetic conversations from real human conversations?
4. Which linguistic features contribute most strongly to this distinction?
5. How does synthetic data quality vary across different online communities and generation settings?

## Methodology

The pipeline consists of four main stages:

### 1. Data Collection

Real conversational data is collected from online communities, including Reddit and Dota 2.

### 2. Synthetic Data Generation

LLMs are prompted to generate conversational examples based on characteristics of the underlying communities.

### 3. Representation & Classification

Generated and real examples are transformed into machine-learning representations and used to train classifiers for distinguishing between the two distributions.

### 4. Statistical & Interpretability Analysis

The project evaluates generated data using distributional metrics and model interpretability techniques, including:

* Maximum Mean Discrepancy (MMD)
* Wasserstein distance
* SHAP
* KeyBERT
* Log-odds analysis

These analyses provide both quantitative measures of similarity and insight into *why* synthetic and real conversations differ.

## Repository Structure

```text
.
├── data/               # Processed datasets
├── dota2/              # Dota 2 conversational data and analysis
├── reddit/             # Reddit conversational data and analysis
├── dspy/               # LLM prompting / generation experiments
├── shap/               # SHAP-based interpretability analysis
├── speeches/           # Generated / real conversational examples
├── utilities/          # Data processing and analysis utilities
├── MMID.ipynb          # Distributional analysis
├── classifier.ipynb    # Real vs. synthetic classification
├── averaged_results.ipynb
└── presentation.ipynb  # Project results and analysis
```

## Key Idea

Rather than evaluating synthetic text solely through human inspection or language-model-based metrics, this project treats synthetic data as a **distribution-matching problem**.

The goal is to determine whether generated conversations capture the underlying structure of real communities — and, when they do not, identify the characteristics responsible for the discrepancy.

## Technologies

* Python
* PyTorch / scikit-learn
* DSPy
* Large Language Models
* SHAP
* KeyBERT
* Statistical distribution analysis
* Jupyter

## Motivation

LLM-generated synthetic data is increasingly used for experimentation, model development, and simulation. However, generated examples can differ systematically from the populations they are intended to represent.

Understanding these differences is important for determining **when synthetic data is useful, what information it preserves, and where it introduces artifacts or biases**.

This project explores these questions through empirical evaluation of synthetic conversational data.

---

**Author:** Pranit Gunjal
**Institution:** California Institute of Technology
