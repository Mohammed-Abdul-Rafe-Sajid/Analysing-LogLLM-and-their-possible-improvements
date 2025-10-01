# Log-Based Anomaly Detection Using BERT Embeddings and Random Forest

## Overview
This repository contains the implementation of a log-based anomaly detection pipeline inspired by the research paper:

**Guan, W., Cao, J., Qian, S., & Gao, J. (2023). LogLLM: Log-based Anomaly Detection Using Large Language Models.**

The goal of this project is to demonstrate how **BERT embeddings** combined with a **Random Forest classifier** can detect anomalies in system logs (HDFS dataset) while reducing the complexity of the full LogLLM framework.

## Features
- Preprocessing of HDFS logs (regex cleaning, extracting EventTemplates)
- Feature extraction using BERT embeddings for each log line
- Classification of logs into **Normal (0)** and **Anomaly (1)** using Random Forest
- Evaluation using **accuracy, precision, recall, F1-score, and confusion matrix**
- Lightweight, beginner-friendly implementation

## Dataset
- HDFS log dataset: `HDFS_2k.log` (raw logs) and structured versions (`HDFS_2k.log_structured.csv`, `HDFS_2k.log_templates.csv`)
- Contains real-world system logs from Hadoop Distributed File System operations
- Anomalies are defined as log entries with **low-frequency EventIds**, while frequent EventIds are considered normal

## Requirements
- Python 3.x
- Libraries:
```bash
pip install pandas numpy scikit-learn transformers torch

## Usage

Clone this repository:
```bash
git clone <your-repo-link>


- Open Log_Anomaly_Detection.ipynb in Google Colab or Jupyter Notebook

## Run the notebook step by step:

- Load dataset

- Preprocess logs

- Generate BERT embeddings

- Train Random Forest classifier

- Evaluate model performance

- View results: classification report, confusion matrix, and accuracy

## Results

- Accuracy: 100% (327 Normal, 73 Anomaly)

- Confusion matrix demonstrates perfect separation between normal and anomalous logs


## References

- Guan, W., Cao, J., Qian, S., & Gao, J. (2023). LogLLM: Log-based Anomaly Detection Using Large Language Models. SJTU.


## Author

- Mohammed Abdul Rafe Sajid
- abdulrafesajid@gmail.com
