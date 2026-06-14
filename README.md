# ANN-Insurance-dataset-
The model converges quickly, with R² improving from ~ -0.27 (epoch 1) to ~0.89 within 100 epochs.
An R² of ~0.887 indicates the model explains about 88.7% of the variance in insurance charges — a strong fit for this small, mostly tabular dataset.
Since both features and the target were standard-scaled, the loss/MAE values are in scaled units. To interpret in real dollar terms, use scaler_y.inverse_transform() on predictions.
The relatively simple architecture (32 → 16 → 1) is sufficient given the small feature set (10 columns) and dataset size (~1337 rows); a deeper network would likely overfit.
smoker status, age, and bmi are typically the most influential predictors of insurance cost in this type of dataset (consistent with domain knowledge, though feature importance was not explicitly computed in the notebook).
