# VISTA Pipeline 1 - Visual Intelligent System for Threat Analysis

## Overview

**VISTA Pipeline 1** is a machine learning pipeline developed for cyber threat detection in Industrial IoT (IIoT) environments. This pipeline focuses on **multi-dataset integration and attack type prediction** using advanced data fusion and classification techniques.

## Datasets

This pipeline integrates two publicly available Industrial IoT datasets:

- **X-IIoTID**  
- **WUSTL_IIoT_2021**

Each dataset contains records of IIoT network traffic with various **cyberattack types** and **shared as well as unique features**.

## Data Fusion Strategy

To effectively merge heterogeneous data sources, the pipeline uses a **mid-fusion strategy** consisting of:

- **Autoencoder-based representation learning** (unsupervised):  
  Learns a compressed representation of both datasets to capture latent structure and reduce noise.
  
- **Manifold Alignment**:  
  Aligns the datasets in a common latent space to preserve statistical relationships across domains.

This fusion enables meaningful comparison and integration of both datasets for joint analysis.

## Model

After fusion, a **Random Forest** classifier is trained on the combined feature space to **predict the type of cyberattack**.

Random Forest was chosen for its robustness, ability to handle mixed feature types, and interpretability.

## Folder Structure

