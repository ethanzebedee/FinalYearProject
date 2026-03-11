# Final Year Project: Classical vs Quantum Machine Learning

This repository contains the notebooks, result files, and supporting material for my final year project comparing classical machine learning models with quantum machine learning models on classification tasks.

The project evaluates classical and quantum approaches across standard datasets and records model accuracy together with CPU and memory usage. Quantum experiments are split between local Qiskit-based runs and Azure Quantum runtime executions.

## Project Scope

The repository focuses on comparing:

- Classical models: Neural Network and Support Vector Machine
- Quantum models: Quantum Support Vector Classifier and Variational Quantum Classifier
- Execution environments: local simulation and Azure Quantum backends

Datasets used in the experiments include:

- Iris
- Wine
- Breast Cancer

## Repository Structure

| Path                                 | Description                                                                             |
| ------------------------------------ | --------------------------------------------------------------------------------------- |
| [ClassicalAlg](./ClassicalAlg)       | Jupyter notebooks for the classical baselines: Neural Network and SVM                   |
| [LocalQuantumAlg](./LocalQuantumAlg) | Jupyter notebooks for locally executed quantum models using Qiskit                      |
| [AzureRuntimeAlg](./AzureRuntimeAlg) | Jupyter notebooks for running quantum workloads through Azure Quantum                   |
| [Results](./Results)                 | CSV outputs containing experiment metrics such as accuracy, CPU usage, and memory usage |
| [Graphs](./Graphs)                   | Generated graphs and visual outputs used in the project                                 |
| [Utils](./Utils)                     | Utility notebooks for producing figures and supporting analysis                         |

## Notebooks

### Classical Algorithms

- [ClassicalAlg/NN.ipynb](./ClassicalAlg/NN.ipynb): neural network baseline experiments
- [ClassicalAlg/SVM.ipynb](./ClassicalAlg/SVM.ipynb): support vector machine baseline experiments

### Local Quantum Algorithms

- [LocalQuantumAlg/QSVC.ipynb](./LocalQuantumAlg/QSVC.ipynb): local Qiskit QSVC experiments
- [LocalQuantumAlg/VQC.ipynb](./LocalQuantumAlg/VQC.ipynb): local Qiskit VQC experiments

### Azure Quantum Runtime

- [AzureRuntimeAlg/QSVC_Runtime.ipynb](./AzureRuntimeAlg/QSVC_Runtime.ipynb): QSVC execution against Azure Quantum targets
- [AzureRuntimeAlg/VQC_Runtime.ipynb](./AzureRuntimeAlg/VQC_Runtime.ipynb): VQC execution against Azure Quantum targets

## Result Files

The [Results](./Results) directory contains the exported CSV files from the experiments:

- [Results/NN_results.csv](./Results/NN_results.csv)
- [Results/SVM_results.csv](./Results/SVM_results.csv)
- [Results/Qiskit_QSVC_results.csv](./Results/Qiskit_QSVC_results.csv)
- [Results/Qiskit_VQC_results.csv](./Results/Qiskit_VQC_results.csv)
- [Results/QSVC_runtime_results.csv](./Results/QSVC_runtime_results.csv)
- [Results/VQC_runtime_results.csv](./Results/VQC_runtime_results.csv)
- [Results/VQC_results.csv](./Results/VQC_results.csv)

These results include measurements such as:

- Training and test scores
- Classification accuracy
- CPU usage
- Memory usage
- Backend-specific runtime results for Azure Quantum experiments

## Requirements

The notebooks use Python libraries from the classical ML and quantum ML ecosystem, including:

- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- psutil
- qiskit
- qiskit-machine-learning
- azure-quantum

## Running The Notebooks

1. Create and activate a Python environment.
2. Install the dependencies required by the notebooks.
3. Open the repository in VS Code or Jupyter.
4. Run the notebooks in the relevant folder depending on whether you want classical, local quantum, or Azure Quantum experiments.

For the Azure notebooks, you will need access to an Azure Quantum workspace and valid provider configuration before executing runtime jobs.

## Notes

- The Azure runtime notebooks are environment-specific and may require replacing workspace configuration values before they can be run in another account.
- The notebooks load standard sklearn datasets directly, so no separate raw dataset directory is required.
- Figures used for analysis can be generated from the result CSV files and the utility notebook in [Utils](./Utils).

## Author

- [Ethan Hammond](https://github.com/ethanzebedee)
- Dr. Simon Caton, Supervisor
