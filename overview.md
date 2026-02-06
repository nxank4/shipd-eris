# Overview

The objective is to predict a Kaggle notebook's upvote count based on various features related to the notebook and its author. Upvotes are a key metric of quality and popularity on Kaggle. Correctly predicting upvote counts can help understand what makes a notebook successful.

This dataset includes numerical, categorical, date, and text features, designed to challenge participants to use features effectively and creatively.

## Evaluation

Your goal is to predict the upvote count. Submissions are evaluated using a modified mean absolute error (MAE) in log space:

```
MAE = min(mean(|log(y_i + 1) - log(ŷ_i + 1)| for all i), 999)
```

Where:
- `y_i` is the true upvote count
- `ŷ_i` is the predicted upvote count

The log transformation handles the right-skewed distribution and ensures the metric isn't dominated by outliers.

## Submission

Submit a CSV file with `content_id` and the predicted upvote count:

| content_id   | upvotes |
|--------------|---------|
| nb_eafe3010  | 100     |
| nb_05570170  | 200     |
| nb_699ec80a  | 300     |

