# aisi304-flow-stress-optimizer

An end-to-end machine learning project that uses an Artificial Neural Network (ANN) to predict and optimize the flow stress of AISI 304 stainless steel under hot deformation conditions.

## Overview

During hot deformation, the flow stress of stainless steel is influenced by three key parameters — temperature, strain rate, and strain. Classical approaches model this relationship using Arrhenius-type equations. This project replaces that manual fitting process with a trained multilayer perceptron (MLP) that learns the relationship directly from experimental data.

Once trained, the model is used as a surrogate to find the **optimal input parameters** that produce a target flow stress — exposed via a clean REST API.

## Key Features

- Data interpolation to expand the experimental dataset
- MLP trained on normalized flow stress (σ/σmax) across temperature, strain rate, and strain
- Optimization over the trained model to find optimal process parameters
- FastAPI backend with `/predict` and `/optimize` endpoints
- Auto-generated Swagger documentation

## Inputs & Output

| Input | Description |
|---|---|
| Temperature (T) | Deformation temperature in Kelvin |
| Strain Rate (ε̇) | Rate of deformation |
| Strain (ε) | Accumulated deformation |

| Output | Description |
|---|---|
| σ/σmax | Normalized flow stress |

## Tech Stack

- **Python** — core language
- **TensorFlow / Keras** — ANN model
- **Scikit-learn** — preprocessing & evaluation
- **SciPy** — data interpolation
- **FastAPI** — API layer
- **Pandas / NumPy** — data handling

## Project Status

In active development

## Material

AISI 304 Austenitic Stainless Steel
### Written by:
Darlene Wendy Nasimiyu