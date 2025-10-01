Log-Based Anomaly Detection Using BERT Embeddings and Random Forest
Overview

This repository contains the implementation of a simplified log-based anomaly detection pipeline inspired by the research paper:

Guan, W., Cao, J., Qian, S., & Gao, J. (2023). LogLLM: Log-based Anomaly Detection Using Large Language Models.

The goal of this project is to demonstrate how BERT embeddings combined with a Random Forest classifier can detect anomalies in system logs (HDFS dataset) while reducing the complexity of the full LogLLM framework.

Features

Preprocessing of HDFS logs (regex cleaning, extracting EventTemplates).

Feature extraction using BERT embeddings for each log line.

Classification of logs into Normal (0) and Anomaly (1) using Random Forest.

Evaluation using accuracy, precision, recall, F1-score, and confusion matrix.

Beginner-friendly, lightweight pipeline for log anomaly detection.

Dataset

HDFS log dataset: HDFS_2k.log (raw logs) and structured versions (HDFS_2k.log_structured.csv, HDFS_2k.log_templates.csv).

The dataset contains real-world system logs from Hadoop Distributed File System operations.

Anomalies are defined as log entries with low-frequency EventIds, while frequent EventIds are considered normal.

Requirements

Python 3.x

Libraries:

pip install pandas numpy scikit-learn transformers torch


Google Colab or local environment with GPU recommended for BERT embeddings.

Usage

Clone this repository:

git clone <your-repo-link>


Open Log_Anomaly_Detection.ipynb in Google Colab or Jupyter Notebook.

Run the notebook step by step:

Load dataset

Preprocess logs

Generate BERT embeddings

Train Random Forest classifier

Evaluate model performance

View results: classification report, confusion matrix, and accuracy.

Results

Accuracy: 100% (327 Normal, 73 Anomaly)

Confusion Matrix shows perfect separation between normal and anomalous logs.

Screenshots of outputs are included in the notebook for reference.

Future Work

Extend the pipeline to include sequence-aware models (e.g., LLaMA, Transformers) for capturing temporal log patterns.

Test on larger, more complex datasets with noisy and unstructured logs.

Explore lightweight embeddings or model distillation for real-time deployment.

References

Guan, W., Cao, J., Qian, S., & Gao, J. (2023). LogLLM: Log-based Anomaly Detection Using Large Language Models. SJTU.

Devlin, J., Chang, M. W., Lee, K., & Toutanova, K. (2019). BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. NAACL-HLT.

Vaswani, A., et al. (2017). Attention Is All You Need. NeurIPS.

Author

Your Name – Cybersecurity Student – [Your Email or Contact Info]
