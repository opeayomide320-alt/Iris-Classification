# Iris Species Classification

A Jupyter Notebook project that predicts the species of an iris flower from
sepal and petal measurements. It compares Logistic Regression and Decision Tree
classifiers using the Iris dataset.

## Overview

The dataset contains 150 flower observations across three species:

- `setosa`
- `versicolor`
- `virginica`

Each observation includes four numerical features:

| Feature | Description |
|---|---|
| `sepal_length` | Sepal length in centimeters |
| `sepal_width` | Sepal width in centimeters |
| `petal_length` | Petal length in centimeters |
| `petal_width` | Petal width in centimeters |

The project:

- Loads and explores `iris.csv`
- Checks the dataset for missing values and class balance
- Visualizes feature distributions and relationships
- Splits the data into stratified training and test sets
- Trains Logistic Regression and Decision Tree models
- Compares model predictions and classification metrics

## Results

The dataset was split with 80% for training (120 observations) and 20% for
testing (30 observations). With `random_state=42`, both models achieved
**93.3% test accuracy**.

| Model | Accuracy |
|---|---:|
| Logistic Regression | 93.3% |
| Decision Tree | 93.3% |

Both models correctly classified 28 of the 30 test flowers and achieved a
macro F1 score of 0.933. They made the same two errors, misclassifying one
versicolor as virginica and one virginica as versicolor.

Both models classify `setosa` perfectly and achieve 90% precision and recall
for `versicolor` and `virginica` in the held-out test set.

## Project Structure

```text
Iris-Classification/
|-- iris.csv
|-- iris_classification.ipynb
|-- README.md
`-- .gitignore
```

## Requirements

- Python 3.10 or newer
- Jupyter Notebook or JupyterLab
- pandas
- seaborn
- matplotlib
- scikit-learn

## Setup

Clone the repository and enter the project directory:

```bash
git clone https://github.com/opeayomide320-alt/Iris-Classification.git
cd Iris-Classification
```

Create and activate a virtual environment:

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# macOS/Linux
source .venv/bin/activate
```

Install the required packages:

```bash
python -m pip install --upgrade pip
python -m pip install jupyter pandas seaborn matplotlib scikit-learn
```

## Run the Notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `iris_classification.ipynb`, then select **Run All**. The notebook can also
be opened in JupyterLab or an IDE with Jupyter support.

## Data Source

The project uses the Iris dataset distributed in the
[Seaborn data repository](https://github.com/mwaskom/seaborn-data). The local
copy is stored as `iris.csv`.
