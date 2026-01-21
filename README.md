# Stellar Luminosity - Linear and Polynomial Models for Regression

## 1. Introduction and Motivation

Astronomy is a data-driven science in which relationships between physical quantities are inferred and validated through observation. Classical examples include the relationships between stellar mass, temperature, radius, and luminosity. In this homework, you will implement linear regression and polynomial regression from first principles, without using machine-learning libraries.

Rather than calling pre-built fitting routines, you will explicitly define the hypothesis function, the loss function, and the optimization algorithm. The astronomical problem studied here is a simplified stellar luminosity modeling task, inspired by main-sequence behavior: luminosity grows rapidly with mass, and additional properties can introduce nonlinear and interaction effects.

## 2. Motivation for Cloud Execution and Enterprise Context

This homework is part of a four-week Machine Learning Bootcamp embedded in a course on Digital Transformation and Enterprise Architecture. In this context, machine learning is treated as a core architectural capability of modern enterprise systems.

Today, intelligence is increasingly considered a first-class quality attribute alongside scalability, availability, security, and performance. Intelligent behavior is no longer confined to offline analytics; it is embedded into platforms, decision-support services, and autonomous or semi-autonomous components.

As enterprise architects, it is not sufficient to understand what models do. We must also understand how they are built from first principles, executed and validated in controlled environments, and operated within cloud platforms.

## 3. General Rules and Delivery Requirements

- Deliver all work in a single GitHub repository.
- The repository must contain two Jupyter notebooks and one README.md.
- All code must be written inside the notebooks.
- All datasets must be defined directly in the notebooks (as hard-coded NumPy arrays).
- **Allowed libraries:** Python, NumPy, Matplotlib (inline plots only).
- **Not allowed:** scikit-learn, statsmodels, TensorFlow/PyTorch, or any high-level regression/optimization library.

## 4. Repository Structure

```
/
├── README.md
├── 01_part1_linreg_1feature.ipynb
└── 02_part2_polyreg.ipynb
```

## 5. Dataset and Notation

Use the following notation throughout:

- **M**: stellar mass (in units of solar mass, M⊙)
- **T**: effective stellar temperature (Kelvin, K)
- **L**: stellar luminosity (in units of solar luminosity, L⊙)

### Part I dataset (one feature)

```python
M = [0.6, 0.8, 1.0, 1.2, 1.4, 1.6, 1.8, 2.0, 2.2, 2.4]
L = [0.15, 0.35, 1.00, 2.30, 4.10, 7.00, 11.2, 17.5, 25.0, 35.0]
```

### Part II dataset (two features)

```python
M = [0.6, 0.8, 1.0, 1.2, 1.4, 1.6, 1.8, 2.0, 2.2, 2.4]
T = [3800, 4400, 5800, 6400, 6900, 7400, 7900, 8300, 8800, 9200]
L = [0.15, 0.35, 1.00, 2.30, 4.10, 7.00, 11.2, 17.5, 25.0, 35.0]
```

## 6. Notebook 1: 01_part1_linreg_1feature.ipynb

See the notebook for full implementation details.

## 7. Notebook 2: 02_part2_polyreg.ipynb

See the notebook for full implementation details.

## 8. AWS SageMaker Requirement (Execution Only)

- Upload both notebooks to AWS SageMaker (Studio or Notebook Instances).
- Run all cells successfully (no errors).
- No model deployment, endpoints, or MLOps pipelines are required.

## 9. AWS SageMaker Execution Evidence

> **TODO:** Complete this section with the required evidence.

### How notebooks were uploaded to SageMaker

*[Describe the upload process here]*

### Screenshots

- [ ] Both notebooks visible/open in SageMaker
- [ ] Successful execution (cells run and outputs visible)
- [ ] At least one plot rendered in SageMaker

*[Insert screenshots here]*

### Comparison: Local Execution vs SageMaker Execution

*[Note any differences observed between local and SageMaker execution]*

## 10. Evaluation Criteria

- Correctness of implementation (loss, gradients, training loop)
- Proper use of vectorization (where required)
- Quality and completeness of plots (dataset, cost surface, interaction cost, convergence)
- Quality of explanations and interpretations
- Successful SageMaker execution with documented evidence in the README