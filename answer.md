# Task 1
Label: repeat_purchase_flag, this is the target variable the model is being trained to predict (1 = repeat purchase, 0 = no repeat purchase).
Leaky feature: discount_used_on_repeat_order, this column contains information that only exists because a repeat purchase happened. Including it as a feature gives the model illegitimate access to the outcome it is supposed to predict, which would inflate performance and make the model useless in production where this value would not yet exist.
# Task 2

Any two of the following are acceptable:

Data auditing : Before modeling, the dataset should be checked for missing values, outliers, ethical concerns, and privacy issues (e.g., customer_id should not be used as a feature). Skipping this risks building a model on flawed or biased data.
Establishing a baseline model : A simple baseline (e.g., predicting the most frequent class: whichever of 0 or 1 appears more often) should be set up first. This defines the minimum performance bar the complex model must beat to justify its use.
Proper data splitting : The dataset must be divided into training, validation, and test sets before any modeling begins. Skipping this means there is no reliable way to know whether the final model actually generalizes to new customers.
