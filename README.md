# Predicting Bike Rentals

This project explores hourly bike rental demand using the UCI Bike Sharing
Dataset. It examines how rentals vary by hour, weekday, season, and weather,
then compares regression models for predicting the number of rentals.

## Project contents

- `Regression.ipynb` — data checks, exploratory charts, correlation analysis,
  and model evaluation.
- `bike+sharing+dataset/hour.csv` — rental counts aggregated by hour.
- `bike+sharing+dataset/day.csv` — rental counts aggregated by day.
- `bike+sharing+dataset/Readme.txt` — original dataset documentation.

## Analysis

The notebook uses `hour.csv` and predicts `cnt`, the total number of rentals
per hour. It compares a mean-prediction baseline (`DummyRegressor`), Linear
Regression, and Random Forest. The observations are sorted chronologically;
the first 80% are used for training and the last 20% for testing.

On the current split, the Random Forest performs best:

| Model | MAE (rentals) | RMSE (rentals) |
|---|---:|---:|
| Mean baseline | 174.98 | 232.61 |
| Linear Regression | 138.29 | 183.28 |
| Random Forest | 45.13 | 69.87 |

These are results for this dataset and split; they do not prove that the
observed relationships are causal or guarantee the same performance on new
data.

## Run the notebook

Open `Regression.ipynb` in Jupyter or PyCharm and select the project's Python
environment (`.venv`). The notebook requires pandas, NumPy, Matplotlib, and
scikit-learn.

## Dataset attribution and license

The Bike Sharing Dataset was created by Hadi Fanaee-T and is based on 2011–2012
Capital Bikeshare data in Washington, D.C. Dataset use is permitted under the
Creative Commons Attribution 4.0 International (CC BY 4.0) license. Please
credit the dataset creator.

For publications, cite:

Fanaee-T, H. and Gama, J. (2013). “Event labeling combining ensemble detectors
and background knowledge.” *Progress in Artificial Intelligence*.
https://doi.org/10.1007/s13748-013-0040-3
