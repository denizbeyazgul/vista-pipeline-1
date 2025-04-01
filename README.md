# VISTA Pipeline 1 - Visual Intelligent System for Threat Analysis

## Overview

**VISTA Pipeline 1** is a machine learning pipeline developed for cyber threat detection in Industrial IoT (IIoT) environments. This pipeline focuses on **multi-dataset integration and attack type prediction** using advanced data fusion and classification techniques.

> ⚠️ **Note:** The code for the data fusion component (Autoencoder and Manifold Alignment) is **not included in this repository** as it is part of a private implementation.

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

> 🔒 While the fusion methodology is described here, the actual implementation code is proprietary and not shared in this repository.

## Model

After fusion, a **Random Forest** classifier is trained on the combined feature space to **predict the type of cyberattack**.

Random Forest was chosen for its robustness, ability to handle mixed feature types, and interoperability.


## Model Explainability

To enhance transparency and trust in the model's predictions, both **global and local explainability** techniques were applied using **SHAP (SHapley Additive exPlanations)**:

- **Global SHAP:**  
  Highlights which features are generally most influential in predicting multi-class attack types.

- **Local SHAP:**  
  Visualizes the contribution of each feature to individual predictions, enabling case-by-case attack investigation.
