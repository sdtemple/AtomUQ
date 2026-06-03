# AtomUQ

AtomUQ is a small machine learning workspace for predicting ligand-to-metal binding affinity in support of downstream decision-making for rare earth materials recycling.

This is a part of the UQ Incubator workshop at the University of Michigan, Ann Arbor, from May 31 to June 3, 2026.

The immediate goal is to build sklearn-based models that estimate whether a ligand is likely to bind strongly to a target metal, then use those predictions to rank candidate ligands and support screening decisions. The longer-term goal is to pair the affinity model with uncertainty estimates so model outputs are easier to trust in a resource-constrained recycling workflow.

## Problem Framing

This repository is intended for supervised learning tasks built around ligand-metal binding data. Typical modeling targets may include:

- Binding affinity regression
- Binding/non-binding classification
- Ranking candidate ligands for follow-up experiments
- Uncertainty-aware screening for rare earth recovery workflows

## Suggested Workflow

1. Gather and clean ligand-metal binding data.
2. Engineer features from ligand identity, metal identity, and experimental context.
3. Train baseline sklearn models.
4. Evaluate with cross-validation and holdout testing.
5. Calibrate or quantify uncertainty where possible.
6. Use the best model to support downstream screening decisions.

## Environment

Create the Python environment with the included conda spec:

```bash
conda env create -f environment.yml
conda activate atomuq
```

If you prefer pip, install the equivalent packages manually from the YAML file.

## Included Stack

The environment is set up for common scientific Python and sklearn workflows, including:

- numpy
- pandas
- scipy
- scikit-learn
- matplotlib
- seaborn
- joblib
- jupyterlab
- ipykernel

