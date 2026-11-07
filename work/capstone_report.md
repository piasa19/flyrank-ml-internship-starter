# Capstone Report — Content Refresh Prioritization

- **Author:** Piasa Das
- **Lane:** Refresh / Content Opportunity Scoring
- **Repo:** https://github.com/piasa19/flyrank-ml-internship-starter
- **Date:** 7 November 2026

## 1. Problem Framing

Content teams manage a large number of web pages and often find it difficult to decide which pages should be reviewed or refreshed first.

This project focuses on the content refresh prioritization problem related to FlyRank.

The unit of analysis is an individual content page. The output is a priority score or ranking that helps identify pages that may need further review.

A human editor can use this ranking to decide which pages should be checked first.

A wrong prediction may cause an important page to be ignored or an unnecessary page to receive attention.

Machine learning can help by analyzing multiple performance signals together and providing a structured way to prioritize content reviews.

## 2. Data Safety

This project uses an anonymized dataset containing search and analytics performance information.

The dataset includes performance signals such as clicks, impressions, CTR and pageviews.

The following precautions were considered:

- Client-identifying information was not used.
- Pseudonymous client IDs were used only for grouping during validation, not as model features.
- `trend_direction` and `trend_pct` were treated as potential leakage risks and excluded from the cleaned feature set.
- Only relevant and available performance features were considered for modelling.

No client-identifying information is intentionally included in the project report or public work files.

## 3. Baseline

A transparent rule-based baseline was developed before applying machine learning.

The baseline used available content performance signals to create an initial prioritization approach.

This provided a simple reference point for evaluating whether a machine learning model could improve the prioritization process.

The baseline and machine learning model should be compared using the same dataset, evaluation split and metric.

**Baseline results:**
- Precision@K: [Insert actual baseline result]
- ROC AUC: [Insert if calculated]

## 4. Model / Analysis

A Random Forest classifier was selected for the machine learning approach.

Random Forest was chosen because it can capture relationships between multiple input features and provide feature importance for interpretation.

The target represents a proxy indication of whether a content page may require refresh-related attention.

The model uses available search and analytics performance signals.

Potentially leaked features and client-identifying identifiers were excluded deliberately.

The purpose of the model is to support prioritization rather than automatically decide which content must be updated.

## 5. Evaluation

The model was evaluated using validation methods designed to reduce the risk of data leakage.

Grouped-by-client validation was considered to test performance on unseen client groups.

The cleaned model achieved the following recorded results:

- ROC AUC: 0.903
- Precision@50: 0.928

The results indicate that the model can distinguish between different levels of refresh priority in the evaluated dataset.

However, Precision@50 should also be interpreted alongside the positive-class base rate and the baseline result.

A proper comparison requires both the baseline and model to use the same validation split.

## 6. Interpretation

The model uses content performance signals to identify pages that may deserve further review.

The results suggest that machine learning can help organize content review priorities using multiple performance indicators.

An important learning from this project was the effect of potential data leakage on model evaluation.

Removing potentially leaked features and considering grouped validation made the evaluation more realistic.

The results should be interpreted as decision-support findings rather than proof that refreshing a page will improve its performance.

## 7. Recommendation

The model can be used as an initial decision-support tool for content editors.

Recommended actions:

1. Review pages with high predicted refresh priority first.
2. Check clicks, impressions and CTR before making decisions.
3. Manually inspect the content quality and relevance.
4. Verify whether a page genuinely needs updating.
5. Monitor page performance after any content changes.

The model should not replace human editorial judgment.

Confidence in the results is limited by the proxy target, dataset characteristics and validation assumptions.

## 8. Reproducibility

The project was developed using Python and Google Colab.

Main libraries used include:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

The project notebooks and supporting files are maintained in the GitHub repository.

Repository:

https://github.com/piasa19/flyrank-ml-internship-starter

For reproducibility, the notebook should be executed in order using the required anonymized dataset.

The model uses a fixed random seed where applicable.

The exact environment and package versions should be recorded in the project requirements.

---

## Final Conclusion

This project explored how machine learning can support content refresh prioritization using anonymized search and analytics data.

The Random Forest model showed promising evaluation results after considering potential leakage risks and grouped validation.

The main outcome is a structured approach to identifying content pages that may require human review.

The project also highlights the importance of data quality, leakage prevention and realistic model evaluation in applied machine learning.
