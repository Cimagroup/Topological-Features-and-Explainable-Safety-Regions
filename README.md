# Topological Features and Explainable Safety Regions

This repository contains data and experiments associated to the paper Toscano-Duran, V., Narteni, S., Carlevaro, A., Guzzi, J., Gonzalez-Diaz, R. and Mongelli, M. (2025) "Safe and Efficient Social Navigation through Explainable Safety Regions Based on Topological Features". Submitted and Accepted to The 3rd World Conference on eXplainable Artificial Intelligence [(XAI-2025)](https://xaiworldconference.com/2025/). Preprint available in [arXiv](https://www.arxiv.org/abs/2503.16441).

The paper deals with simulated social robotics navigation problem that involves a fleet of mobile robots moving in a Cross scenario, governed by a human-like behavior. With the purpose of avoiding negative events, as collisions or deadlocks, we show how to topological features can improve the accuracy and effectiveness of safe and explainable AI (XAI) methods being an useful tool to know and adjust whether a simulation will be safe(free of collisions) or not, efficient(free of deadlocks) or not, and compliant (free of both, collisions and deadlocks) or not.

# Repository structure

- ExpTopologicalCollision: Experiments for avoid collisions, using safety regions and topological features.

- ExpTopologicalDeadlock: Experiments for avoid deadlocks, using safety regions and topological features.

- ExpTopologicalAdvanced: Extension experiments using more topological features for build safety regions (not included in the paper).

# Usage

1) Clone this repository and create a virtual enviromment (It requires Python>=3.10, and it has been developed specifically with Python3.10.11):
```bash
virtualenv -p python3.10 env
```

Next, activate the virtual environment 
```bash
env\Scripts\activate
```

2) Install the necessary dependencies: (first install navground and then the rest of the dependencies)

```bash
pip install navground[all]
```

```bash
pip install pandas==2.2.3 seaborn==0.13.2 scikit-learn==1.3.0 skope-rules==1.0.1 numpy==1.25.1 qpsolvers[open_source_solvers] cvxopt anchor-exp gudhi
```

3) **Simulation and dataset collection (including simulations and topological features)**: run the `getdataset_TopologicalFeatures.py` script with the YAML settings contained in `configTopological.yaml` file. Dataset used in further experiments.

4) **Native rule generation**: run `SkopeRules.ipynb` for training skope-rules model, and `NativeXAI_performance.ipynb` for its evaluation.

5) **Scalable Classifiers for Probabilistic/Conformal safety regions**: run `ConfidenceRegions_SVM.ipynb`.

6) **Local Rule Extraction from PSR/CSR**: run `Anchor_PSR.ipynb`, `Anchor_CSR.ipynb` for Anchors extraction, and `AnchorAnalysis_PSR.ipynb`, `AnchorAnalysis_CSR.ipynb`for their evaluation.

# Citation and reference

If you want to use our code or data for your experiments, please cite our paper.

For further information, please contact us at: vtoscano@us.es, sara.narteni@cnr.it

