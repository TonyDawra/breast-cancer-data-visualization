# Breast Cancer Data Analysis & Visualization

A collection of notebook-based visual analyses and a **Power BI correlation report**. The Python notebook explores the Wisconsin Diagnostic Breast Cancer dataset through class distributions, feature relationships, PCA projections, model comparisons, and evaluation charts.

[Analysis notebook](Untitled10.ipynb) · [Report](Visualization.pdf) · [Power BI file](correlation%20%281%29.pbix)

## Visual analysis

The notebook includes:

- Class-distribution charts before and after oversampling.
- A feature-correlation heatmap.
- Cumulative explained variance and PCA component plots.
- A two-component projection colored by class.
- Comparisons of model accuracy with and without PCA.
- Probability distributions, confusion matrices, and precision-recall analysis.

The Power BI file contains a correlation matrix, a feature-pair table, and a ranked column chart built from a long-form correlation table.

![Cumulative explained variance for principal components](assets/pca-variance.png)

*Saved notebook output from the PCA exploration.*

## Run the Python analysis

~~~bash
git clone https://github.com/TonyDawra/Data-Visualization-project.git
cd Data-Visualization-project
python -m pip install notebook numpy pandas matplotlib seaborn scikit-learn imbalanced-learn xgboost ucimlrepo
jupyter notebook Untitled10.ipynb
~~~

The notebook retrieves the dataset using `ucimlrepo` with dataset ID `17`. Run its analysis cells in order; internet access is required for retrieval.

## Open the Power BI report

1. Download `correlation (1).pbix`.
2. Open it in **Power BI Desktop on Windows**.
3. Explore the matrix, pair table, and ranked correlation chart.
4. Before refreshing, inspect the data-source settings and update any local paths used by the original report.

The repository does not include a separate correlation CSV or documented refresh pipeline. The notebook and PBIX should therefore be treated as separate analytical artifacts until their data lineage is explicitly connected.

## Repository contents

| File | Purpose |
| --- | --- |
| `Untitled10.ipynb` | Python exploration, model comparisons, and charts |
| `Visualization.pdf` | Accompanying report |
| `correlation (1).pbix` | Interactive correlation report |

## Interpretation

The notebook's model scores are exploratory: oversampling, scaling, and PCA occur before the train/test split. Rebuild the evaluation with training-only transformations before treating the scores as evidence of generalization.

Correlation does not establish causation. PCA plots show projections of the data and do not independently demonstrate classifier performance.

## Next steps

Document a common data-preparation pipeline for the notebook and Power BI file, add report screenshots, give the notebook a descriptive filename, and pin the Python environment.

## Maintainer

[Tony Dawra](https://github.com/TonyDawra)
