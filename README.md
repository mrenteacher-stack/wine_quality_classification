# Wine Quality Analysis

An academic machine learning project that explores whether physicochemical properties can help classify red wine quality. The notebook compares supervised classification models, applies K-Means clustering, and uses PCA to visualize the data in two dimensions.

## Project objectives

- Convert the original wine quality score into two classes: **low quality** and **high quality**.
- Train and compare a Logistic Regression model and a Decision Tree classifier.
- Use K-Means to identify groups of wines with similar physicochemical properties.
- Use Principal Component Analysis (PCA) to visualize patterns in the dataset.

## Dataset

The notebook uses the `winequality-red.csv` dataset. It contains **1,599 wine samples** and 12 columns:

- 11 physicochemical measurements, including acidity, residual sugar, chlorides, sulfur dioxide, density, pH, sulphates, and alcohol.
- `quality`, the original quality score.

The notebook reports no missing values. It also notes **240 duplicate records**, which should be considered when interpreting the model evaluation.

### Target definition

The original `quality` score is converted into a binary target named `quality_class`:

| Original score | Class | Meaning |
|---|---:|---|
| `quality < 6` | `0` | Low quality |
| `quality >= 6` | `1` | High quality |

The original `quality` column is excluded from the model features to prevent target leakage.

## Requirements

- Python
- Google Colab and a Google account, if following the notebook's current Drive-based setup
- The `winequality-red.csv` dataset

The notebook uses:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

## How to run

1. Open `QualidadedeVinho.ipynb` in [Google Colab](https://colab.research.google.com/ ).
2. Upload `winequality-red.csv` to the Google Drive folder expected by the notebook, or update the CSV path in the data-loading cell.
3. Run the cells in order, from top to bottom.
4. Review the tables, metrics, and visualizations displayed in the notebook.

The current notebook reads the dataset from:

```text
/content/drive/MyDrive/ANÁLISE DE VINHO TINTO - UNIFOR/winequality-red.csv
