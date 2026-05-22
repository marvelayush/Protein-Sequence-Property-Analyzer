# 🧬 Bioinformatics – Protein Sequence Property Analyzer

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Biopython](https://img.shields.io/badge/Biopython-Used-green?style=for-the-badge)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?style=for-the-badge)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Handling-yellow?style=for-the-badge)

A **Python-based bioinformatics project** for analyzing protein sequences and extracting important biochemical, structural, and physicochemical properties.  
The project reads protein sequences in **FASTA format**, performs protein analysis using **Biopython**, computes **hydropathy profiles**, detects **motifs**, classifies proteins based on stability and hydrophobicity, and visualizes the results using **Matplotlib**.

---

## 📌 Project Overview

Proteins are biological macromolecules made up of amino acid chains, and their properties determine how they behave in a cell.  
This project focuses on **sequence-based protein analysis** and produces a detailed report for each protein sequence provided in the input.

The analyzer calculates:

- **Protein Length**
- **Molecular Weight**
- **Isoelectric Point (pI)**
- **GRAVY Score** (Grand Average of Hydropathy)
- **Instability Index**
- **Secondary Structure Fractions**
- **Hydropathy Profile**
- **Motif Locations**
- **Protein Classification**

---

## ✨ Features

- 🧾 **FASTA Parsing**
  - Reads protein sequences from FASTA format
  - Supports sequence names and sequence data separation

- 📂 **External FASTA File Support**
  - Can be extended to load `.fasta`, `.fa`, or `.txt` FASTA files from:
    - local system
    - project folder
    - downloads folder
    - any custom file path

- 🧪 **Protein Property Analysis**
  - Uses `Bio.SeqUtils.ProtParam.ProteinAnalysis`
  - Computes:
    - molecular weight
    - isoelectric point
    - GRAVY
    - instability index
    - helix fraction
    - turn fraction
    - sheet fraction

- 🌊 **Hydropathy Plot**
  - Uses a sliding-window method to calculate local hydropathy values
  - Helps identify hydrophobic and hydrophilic regions in the protein

- 🔍 **Motif Detection**
  - Uses regular expressions to identify sequence motifs
  - Default motif used in the project:
    ```text
    N[^P][ST]
    ```

- 🧠 **Protein Classification**
  - Classifies proteins as:
    - `Stable & Hydrophobic`
    - `Stable & Hydrophilic`
    - `Unstable Protein`

- 📊 **Tabular Summary**
  - Displays all computed values in a Pandas DataFrame

- 📈 **Graphical Visualization**
  - Generates hydropathy plots for each protein sequence

---

## 🛠️ Technologies Used

- **Python**
- **Biopython**
- **Matplotlib**
- **Pandas**
- **Regular Expressions (`re`)**

---

## ⚙️ How It Works

### 1. FASTA Input

The program begins with protein sequences written in **FASTA format**.

#### Example:
```text
>Protein_Name
SEQUENCE
