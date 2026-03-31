Here is a **clean, professional, GitHub-ready README** with badges, formatted formally and without emojis or informal styling.

---

# Analysis of LLM Outputs for Country-Based Question Answering

<p align="center">
  <img src="https://img.shields.io/badge/Project-Research-blue">
  <img src="https://img.shields.io/badge/Domain-NLP-green">
  <img src="https://img.shields.io/badge/Model-TinyLlama-orange">
  <img src="https://img.shields.io/badge/Framework-PyTorch-red">
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen">
</p>

---

## Authors

Swakatha Bandyopadhyay
Pramiti Tewari

Supervisor: Prof. Arnab Bhattacharya
Mentor: Pramit Bhattacharyya

---

## Abstract

This project investigates the behavior of Large Language Models in few shot question answering tasks involving country based factual queries such as capitals, continents, and official languages. The study focuses on both performance evaluation and internal model interpretability.

Using TinyLlama 1.1B Chat v1.0, the research analyzes how models respond to structured prompts and how their internal components such as attention heads and MLP layers contribute to predictions. The project applies mechanistic interpretability techniques including activation patching, ablation, and attention visualization to identify circuits responsible for in context learning.

The findings demonstrate that while zero shot performance remains limited, few shot prompting significantly improves accuracy. The work contributes to understanding how compact models generalize knowledge and how they can be made more reliable and interpretable.

---

## Objectives

Evaluate few shot learning performance of language models

Compare zero shot and few shot accuracy

Identify important attention heads and layers

Analyze robustness across prompt variations

Understand internal mechanisms using interpretability techniques

Assess reliability and consistency of model outputs

---

## Technology Stack

Programming Language
Python 3.10 or higher

Frameworks and Libraries
PyTorch
Hugging Face Transformers
transformer_lens

Data and Visualization
Pandas
NumPy
Matplotlib
Seaborn
Plotly

Development Environment
Google Colab with GPU
Jupyter Notebook
VS Code

---

## Dataset

Source
Wikipedia list of national capitals

Attributes
Country
Capital
Continent

Preprocessing
Removal of noisy text and annotations
Normalization of country names
Handling multiple capital entries
Structured conversion into question answering format

---

## Methodology

Data Collection
Web scraping using requests and BeautifulSoup

Data Cleaning
Normalization and filtering of inconsistent entries

Prompt Engineering
Design of structured question answering prompts
Implementation of chat style and formatted prompts

Evaluation Strategy

Zero Shot Evaluation
Model prediction without examples

Few Shot Evaluation
Model prediction with varying number of examples ranging from 1 to 150

---

## Interpretability Techniques

Activation Patching
Replacing activations between clean and corrupted runs to identify important components

Attention Analysis
Visualization of attention weights to track token level focus

Ablation Studies
Selective disabling of attention heads or layers to observe performance degradation

---

## Results

Zero shot performance was low for factual question answering

Few shot prompting significantly improved accuracy

Accuracy increased with the number of examples provided

Certain attention heads consistently contributed to correct predictions

Model performed better on widely known countries compared to less common ones

---

## Key Findings

Compact models can effectively learn patterns through in context examples

Prompt structure plays a critical role in determining output quality

Models rely heavily on pattern recognition rather than deep reasoning

Interpretability techniques can successfully identify critical internal components

Data quality and normalization are essential for reliable evaluation

---

## Limitations

Performance decreases for rare or ambiguous country names

Model sensitivity to prompt structure variations

Limited reasoning capability beyond factual recall

Interpretability methods require significant computational resources

---

## Future Work

Extension to larger models such as LLaMA and GPT Neo

Exploration of multilingual datasets

Improvement in robustness to ambiguous inputs

Automation of circuit discovery methods

Application to other domains such as healthcare and education

---

## Project Structure

```
project_root/
│
├── data/
│   └── cleaned_dataset.csv
│
├── notebooks/
│   ├── data_preprocessing.ipynb
│   ├── few_shot_experiments.ipynb
│   └── interpretability_analysis.ipynb
│
├── src/
│   ├── prompt_builder.py
│   ├── evaluation.py
│   └── ablation.py
│
├── results/
│   ├── accuracy_plots/
│   └── attention_heatmaps/
│
├── report.pdf
└── README.md
```

---

## Setup and Execution

Install dependencies

```
pip install torch transformers transformer_lens pandas matplotlib seaborn
```

Run the notebooks in Google Colab or a local environment with GPU support

Steps
Load dataset
Preprocess data
Generate prompts
Run model inference
Evaluate accuracy
Visualize results

---

## Acknowledgement

The authors express sincere gratitude to Prof. Arnab Bhattacharya for his guidance and to Pramit Bhattacharyya for technical mentorship and support throughout the project.

---

## License

This project is intended for academic and research purposes only.


