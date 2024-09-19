
# EMT-Kcr: A Bioinformatics Tool for Lysine Crotonylation Site Identification

**EMT-Kcr** is a novel bioinformatics tool designed to identify lysine crotonylation (Kcr) sites in proteins using advanced deep learning techniques. It integrates the **ESM2 protein language model** with **multi-task auxiliary learning** to improve prediction accuracy across multiple species. This tool can aid researchers in understanding protein post-translational modifications (PTMs), which play key roles in biological processes, disease diagnosis, and drug development.

## Features

- **Multi-task Auxiliary Learning**: Enhances prediction accuracy by simultaneously training on multiple tasks.
- **ESM2 Protein Language Model**: Leverages a state-of-the-art protein language model for superior feature extraction.
- **Visualization and Interpretability**: Provides visualization techniques like t-SNE and attention mechanisms to offer insights into the spatial relationship of Kcr sites.
- **Cross-Species Generalization**: Demonstrates high accuracy across various species, including humans, plants, animals, and microorganisms.
- **User-Friendly Web Interface**: Allows easy input of protein sequences to obtain predictions via a web server.

## Table of Contents
1. [Installation](#installation)
2. [Data Preparation](#data-preparation)
3. [Usage](#usage)
4. [Web Server](#web-server)
5. [Evaluation](#evaluation)
6. [References](#references)

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

3. **Install Required Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download ESM2 Pretrained Model**:
   Download the ESM2 model from the provided Facebook AI Model Zoo link and place it in the appropriate directory as specified in the code.

## Data Preparation

EMT-Kcr accepts protein sequences as input. You can format your data as follows:

- Each sequence should be in the **FASTA** format.
- The tool expects the protein sequences to contain valid amino acid residues.

To prepare your dataset, place your input files in the `data/` directory or the specified location in the configuration.

## Usage

1. **Run Predictions**:

   After preparing your data and setting up the environment, you can run predictions using the following command:

   ```bash
   python run_emt_kcr.py --input data/protein_sequences.fasta --output results/predictions.csv
   ```

   The results will be saved as a CSV file in the output directory with the predicted Kcr sites and associated probabilities.

2. **Visualization**:
   
   To visualize the results and gain insights into the model's attention mechanisms:
   ```bash
   python visualize.py --input results/predictions.csv
   ```

   This will generate attention maps and t-SNE visualizations of the protein sequences.

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

## References

For further information, please refer to the [research article](https://www.sciencedirect.com/science/article/abs/pii/S0141813024001147) and associated documentation.
