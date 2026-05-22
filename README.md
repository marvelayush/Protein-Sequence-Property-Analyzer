# 🧬 Bioinformatics – Protein Sequence Property Analyzer

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Biopython](https://img.shields.io/badge/Biopython-Used-success?style=for-the-badge)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?style=for-the-badge)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Handling-yellow?style=for-the-badge)

A **Python-based bioinformatics project** for analyzing protein sequences and extracting important biochemical and structural properties.  
This project reads protein sequences in **FASTA format**, performs sequence-level analysis using **Biopython**, computes **hydropathy profiles**, detects **motifs**, classifies proteins based on stability and hydrophobicity, and visualizes the results using **Matplotlib**.

---

## 📌 Project Overview

Proteins are made up of amino acid sequences, and their properties determine how they behave in biological systems.  
This project focuses on **sequence-based protein analysis** and generates a detailed report for each protein sequence provided in the input.

The analyzer computes:

- **Length** of the protein sequence
- **Molecular Weight**
- **Isoelectric Point (pI)**
- **GRAVY score** (Grand Average of Hydropathy)
- **Instability Index**
- **Secondary Structure Fractions**
- **Hydropathy Profile**
- **Motif Positions**
- **Protein Classification**

---

## ✨ Features

- 🧾 **FASTA Parser**  
  Reads and stores protein sequences from FASTA-style input.

- 🧪 **Protein Property Analysis**  
  Uses `Bio.SeqUtils.ProtParam.ProteinAnalysis` from Biopython to compute:
  - molecular weight
  - isoelectric point
  - GRAVY
  - instability index
  - secondary structure fractions

- 🌊 **Hydropathy Plot**  
  Generates a sliding-window hydropathy profile for every sequence.

- 🔍 **Motif Detection**  
  Finds biological motifs using regular expressions.  
  Default motif used in the project:
  `N[^P][ST]`

- 🧠 **Protein Classification**  
  Classifies each protein as:
  - `Stable & Hydrophobic`
  - `Stable & Hydrophilic`
  - `Unstable Protein`

- 📊 **Tabular Output**  
  Displays all results in a Pandas DataFrame.

- 📈 **Visualization**  
  Plots hydropathy graphs using Matplotlib.

---

## 🛠️ Technologies Used

- **Python**
- **Biopython**
- **Matplotlib**
- **Pandas**
- **Regular Expressions (re)**

---

## ⚙️ How It Works

### 1. FASTA Input
The program begins with protein sequences written in FASTA format.

Example:
```text
>Protein_Name
SEQUENCE
