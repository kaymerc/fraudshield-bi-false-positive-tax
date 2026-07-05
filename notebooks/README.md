# Analysis Notebook

[`FraudShield_BI_Analysis.ipynb`](FraudShield_BI_Analysis.ipynb) is the complete notebook used for the FraudShield BI capstone analysis.

## Workflow Covered

1. Data loading and validation
2. Cleaning and feature engineering
3. Exploratory data analysis
4. Chi-square and Mann-Whitney U testing
5. Class-weighted logistic regression
6. Logistic-regression threshold and cost analysis
7. False-positive segmentation
8. Histogram-based gradient boosting
9. Gradient-boosting threshold and cost analysis
10. Model comparison and hypothesis decisions
11. Export of validated CSV tables and report figures

## Running the Notebook

1. Download `fraudTrain.csv` and `fraudTest.csv` as described in [`../data/README.md`](../data/README.md).
2. Place both CSV files in `data/`.
3. Install dependencies from the repository root:

```bash
pip install -r requirements.txt
```

4. Start Jupyter from the repository root and open the notebook, or change into `notebooks/` before running it. The notebook uses relative paths such as `../data/` and `../outputs/`.

The repository version adds explanatory Markdown section headings for readability. The analysis code and saved analytical outputs from the original notebook were not changed.
