# Stellar Luminosity - Linear and Polynomial Models for Regression

Implementation of linear and polynomial regression models from first principles to predict stellar luminosity based on mass and temperature, executed on AWS SageMaker.

## Getting Started

These instructions will give you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on deploying the project on AWS SageMaker.

### Prerequisites

Requirements for running the notebooks:

- [Python 3.x](https://www.python.org/)
- [NumPy](https://numpy.org/) - Numerical computing
- [Matplotlib](https://matplotlib.org/) - Inline plots only
- [Jupyter Notebook](https://jupyter.org/) - For local execution
- [AWS Account](https://aws.amazon.com/) - For SageMaker execution

> **Not allowed:** scikit-learn, statsmodels, TensorFlow/PyTorch, or any high-level regression/optimization library.

### Installing

A step by step series to get a development environment running:

1. Clone the repository

    ```bash
    git clone https://github.com/AnderssonProgramming/regression-aws-ai.git
    cd regression-aws-ai
    ```

2. Install the required libraries

    ```bash
    pip install numpy matplotlib jupyter
    ```

3. Launch Jupyter Notebook

    ```bash
    jupyter notebook
    ```

4. Open and run the notebooks in order:
   - `01_part1_linreg_1feature.ipynb`
   - `02_part2_polyreg.ipynb`

## Introduction and Motivation

Astronomy is a data-driven science in which relationships between physical quantities are inferred and validated through observation. Classical examples include the relationships between stellar mass, temperature, radius, and luminosity. In this project, you will implement linear regression and polynomial regression from first principles, without using machine-learning libraries.

Rather than calling pre-built fitting routines, you will explicitly define the hypothesis function, the loss function, and the optimization algorithm. The astronomical problem studied here is a simplified stellar luminosity modeling task, inspired by main-sequence behavior: luminosity grows rapidly with mass, and additional properties can introduce nonlinear and interaction effects.

### Motivation for Cloud Execution and Enterprise Context

This project is part of a four-week Machine Learning Bootcamp embedded in a course on Digital Transformation and Enterprise Architecture. In this context, machine learning is treated as a core architectural capability of modern enterprise systems.

Today, intelligence is increasingly considered a first-class quality attribute alongside scalability, availability, security, and performance. Intelligent behavior is no longer confined to offline analytics; it is embedded into platforms, decision-support services, and autonomous or semi-autonomous components.

As enterprise architects, it is not sufficient to understand what models do. We must also understand how they are built from first principles, executed and validated in controlled environments, and operated within cloud platforms.

## Dataset and Notation

Use the following notation throughout:

| Symbol | Description | Units |
|--------|-------------|-------|
| **M** | Stellar mass | Solar mass (M⊙) |
| **T** | Effective stellar temperature | Kelvin (K) |
| **L** | Stellar luminosity | Solar luminosity (L⊙) |

### Part I Dataset (One Feature)

```python
M = [0.6, 0.8, 1.0, 1.2, 1.4, 1.6, 1.8, 2.0, 2.2, 2.4]
L = [0.15, 0.35, 1.00, 2.30, 4.10, 7.00, 11.2, 17.5, 25.0, 35.0]
```

### Part II Dataset (Two Features)

```python
M = [0.6, 0.8, 1.0, 1.2, 1.4, 1.6, 1.8, 2.0, 2.2, 2.4]
T = [3800, 4400, 5800, 6400, 6900, 7400, 7900, 8300, 8800, 9200]
L = [0.15, 0.35, 1.00, 2.30, 4.10, 7.00, 11.2, 17.5, 25.0, 35.0]
```

## Repository Structure

```
/
├── README.md                           # Project documentation
├── 01_part1_linreg_1feature.ipynb      # Linear Regression with one feature
└── 02_part2_polyreg.ipynb              # Polynomial Regression
```

### Notebook 1: Linear Regression with One Feature

`01_part1_linreg_1feature.ipynb` - Implements linear regression from scratch using gradient descent to model the relationship between stellar mass and luminosity.

### Notebook 2: Polynomial Regression

`02_part2_polyreg.ipynb` - Extends the model to polynomial regression with two features (mass and temperature) to capture nonlinear relationships.

## Deployment

### AWS SageMaker Execution

To deploy and run this project on AWS SageMaker:

1. Upload both notebooks to AWS SageMaker (Studio or Notebook Instances)
2. Run all cells successfully (no errors)
3. No model deployment, endpoints, or MLOps pipelines are required

### AWS SageMaker Execution Evidence

The successful execution of both notebooks on AWS SageMaker is documented in the following video:

📹 **[aws-sagemaker-ai-notebooks-video.mp4](aws-sagemaker-ai-notebooks-video.mp4)**

The video demonstrates:
- ✅ Both notebooks open in AWS SageMaker JupyterLab
- ✅ Successful execution of all cells (no errors)
- ✅ Rendered plots and visualizations
- ✅ Complete training loop outputs

#### How notebooks were uploaded to SageMaker

For detailed step-by-step instructions on setting up AWS SageMaker (creating domains, user profiles, JupyterLab spaces, and uploading notebooks), see the **[SageMaker Setup Guide](SAGEMAKER_SETUP.md)**.

#### Comparison: Local Execution vs SageMaker Execution

> **TODO:** Note any differences observed between local and SageMaker execution.

## Built With

- [Python](https://www.python.org/) - Programming language
- [NumPy](https://numpy.org/) - Numerical computing library
- [Matplotlib](https://matplotlib.org/) - Visualization library
- [AWS SageMaker](https://aws.amazon.com/sagemaker/) - Cloud ML platform

## Evaluation Criteria

| Criterion | Description |
|-----------|-------------|
| Correctness | Implementation of loss, gradients, and training loop |
| Vectorization | Proper use of vectorization where required |
| Plots | Quality and completeness (dataset, cost surface, interaction cost, convergence) |
| Explanations | Quality of explanations and interpretations |
| SageMaker | Successful execution with documented evidence |

## Authors

- **Andersson David Sánchez Méndez** - *Developer* - [AnderssonProgramming](https://github.com/AnderssonProgramming)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Machine Learning Bootcamp - Digital Transformation and Enterprise Architecture course
- Inspiration from main-sequence stellar behavior models
- AWS SageMaker for cloud ML execution capabilities
