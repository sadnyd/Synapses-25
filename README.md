# Synapses-25
gods_of_new_world
# Uplift Modeling Analysis on Criteo Dataset

## Introduction

This project implements and evaluates uplift modeling techniques on the large-scale Criteo Uplift Prediction dataset. Uplift modeling (also known as heterogeneous treatment effect estimation or causal impact modeling) aims to predict the incremental impact of a treatment (e.g., showing an advertisement) on an individual's behavior (e.g., converting).

The analysis largely follows the methodologies and uses the dataset presented in the paper:

* Diemert, E., Betlei, A., Renaudin, C., & Amini, M. R. (2018). *A Large Scale Benchmark for Uplift Modeling*. Proceedings of AdKDD & TargetAd (ADKDD'18). ([HAL link](https://hal.science/hal-02515860v1))

The goal is to provide a practical implementation of common uplift techniques and evaluation metrics.

## Features

* Loads the Criteo Uplift Prediction dataset via the `datasets` library.
* Performs essential preprocessing: Feature normalization (StandardScaler).
* Includes a crucial sanity check: Classifier Two-Sample Test (C2ST) to verify treatment independence from features.
* Implements two standard uplift modeling meta-learners:
    * **Two-Model Approach:** Trains separate models for treatment and control groups.
    * **Revert-Label (Class Transformation) Approach:** Transforms the target variable and trains a single model.
* Evaluates models using uplift-specific metrics:
    * **Qini Curve & Coefficient:** Measures incremental gains.
    * **Uplift Curve & AUUC (Area Under Uplift Curve):** Measures cumulative uplift.
* Includes a method to identify **Feature Importance for Uplift** using interaction terms within a RandomForest model.
* Visualizes evaluation results (Qini/Uplift curves) and feature importances.

## Setup / Installation

1.  **Open your terminal and run:**
```bash
git clone https://github.com/sadnyd/Synapses-25.git
cd Synapses-25
```

2.  **Install required libraries:**
    It's recommended to use a virtual environment.
    ```bash
    pip install datasets scikit-learn pandas numpy matplotlib seaborn
    ```

## 📓 Google Colab Notebooks

In case some of the notebooks in this repository do not work properly, you can access the working versions using the links below:

- [Notebook 1](https://colab.research.google.com/drive/1N2N58pT68NdIglxk2Rx0QujB8mr_4P_X?usp=sharing)
- [Notebook 2](https://colab.research.google.com/drive/1XWflc61wj_BFvd2J0HXnODiO8WOrkls6?usp=sharing)

Feel free to open them in Google Colab and run the code directly!


