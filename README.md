# Australian-Used-Car-Price-Prediction
This repositiory contains my work on Assignment 1 for my Masters degree at UTS as a data science student. I was provided with the raw dataset and worked my way from EDA to finalising the model and checking RMSE on the test data. This assignment was limited to Linear Regression, ElasticNet and KNN, the ones that were taught in class. 

I held experiments to check which out of the 3 predicts the fair market price of used cars in Australia with least RMSE for the given datset to help buyers on platforms like Gumtree and Facebook Marketplace determine if a listing is overpriced, fairly priced or a good deal.

## Business Problem

Buyers in the Australian used car market have no reliable way to verify whether a listed price is fair. This tool takes a car's specifications as input and returns a predicted fair market price.

## Dataset

Australian used car listings split into training (pre-2017 manufactured vehicles), validation (2019-2020) and testing (2022-2023) sets. Data was provided as part of UTS course assessment and cannot be shared publicly.

## Approach

Three experiments were conducted using the same 6 engineered features across all models for fair comparison:

| Model | Validation RMSE |
|---|---|
| Baseline (mean predictor) | $37,291.73 |
| Linear Regression | $27,162.40 |
| ElasticNet | $27,872.71 |
| KNN (n=7, p=2) | $23,676.16 |

KNN outperformed all models and was selected as the final model.

## Features Used

- kilometres_driven
- manufacturing_year  
- engine_cylinders
- brand_bodytype_encoded (smoothed mean encoding)
- body_drive_encoded (smoothed mean encoding)
- transmission_type_Manual

## Key Findings

- KNN achieved the best validation RMSE of $23,676 — a $13,616 improvement over baseline
- Model is most reliable in the $15k–$30k range (RMSE $4,361)
- All models struggle above $50k due to insufficient luxury car training data
- Model is NOT recommended for production deployment until retrained on post-2020 data

## Project Structure

- `notebooks/` — 6 Jupyter notebooks (EDA to experiments)
- `report/` — Final project report  
- `data/` — Data folder (data not included)
- `requirements.txt` — Python dependencies
- `README.md` — Project documentation
  
## Tech Stack

Python, pandas, scikit-learn, numpy, matplotlib, seaborn, altair

## ⚠️ Academic Integrity

This project was completed as part of UTS 36106 Machine Learning Algorithms and Applications assessment. The code and report are shared for portfolio purposes only.
Please do not copy or submit any part of this work as your own. Academic misconduct is taken seriously at UTS and all universities.

## Author

**Sushruta Gangadhar Patil**  
Master of Data Science and Innovation  
University of Technology Sydney  
