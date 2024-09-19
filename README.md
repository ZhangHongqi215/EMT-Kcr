# EMT-Kcr: A Bioinformatics Tool for Lysine Crotonylation Site Identification

**EMT-Kcr** is a novel bioinformatics tool designed to identify lysine crotonylation (Kcr) sites in proteins using advanced deep learning techniques. It integrates the **ESM2 protein language model** with **multi-task auxiliary learning** to improve prediction accuracy across multiple species. This tool can aid researchers in understanding protein post-translational modifications (PTMs), which play key roles in biological processes, disease diagnosis, and drug development.

## Features

- **Multi-task Auxiliary Learning**: Enhances prediction accuracy by simultaneously training on multiple tasks.
- **ESM2 Protein Language Model**: Leverages a state-of-the-art protein language model for superior feature extraction.
- **Cross-Species Generalization**: Demonstrates high accuracy across various species, including humans, plants, animals, and microorganisms.
- **User-Friendly Web Interface**: Allows easy input of protein sequences to obtain predictions via a web server.

## Table of Contents
1. [Installation](#installation)
2. [Data Preparation](#data-preparation)
3. [Web Server](#web-server)
4. [Evaluation](#evaluation)

## Installation

To use EMT-Kcr, follow these installation steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ZhangHongqi215/EMT-Kcr.git
   cd EMT-Kcr
   ```

2. **Create a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```


## Data Preparation

EMT-Kcr accepts protein sequences as input. You can format your data as follows:

- Each sequence should be in the **FASTA** format.

To prepare your dataset, place your input files in the `data/` directory or the specified location in the configuration.

## Web Server

A web-based interface for EMT-Kcr is available, allowing you to input protein sequences and get Kcr site predictions. Visit:

[http://emt-kcr.lin-group.cn](http://emt-kcr.lin-group.cn)

- Navigate to the **TOOL** tab.
- Input a protein sequence or upload a FASTA file.
- Click **Submit** to view the predicted Kcr sites.

## Evaluation

EMT-Kcr has been rigorously evaluated using various datasets from multiple species. Key evaluation metrics include:

- **Accuracy (ACC)**
- **Precision (Pre)**
- **Recall (Rec)**
- **F1 Score**
- **Matthew’s Correlation Coefficient (MCC)**

The tool has outperformed several state-of-the-art models like DeepCap-Kcr, demonstrating high predictive power across species.

