# 🏠 House Price Prediction

A machine learning project that predicts house sale prices using **XGBoost**, tuned with **GridSearchCV**, and served through an interactive **Gradio** web UI. Built and trained on the Kaggle [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) dataset.

## Overview

The notebook trains a regression model on 20 key housing features (quality, living area, garage size, basement area, year built, etc.) to estimate a home's sale price, then wraps the trained model in a Gradio interface so anyone can enter property details and get an instant price estimate.

## Features Used

- Overall Quality & Condition
- Living Area, Garage Area, Basement Area, 1st/2nd Floor Area
- Garage Cars, Full Bathrooms, Total Rooms, Bedrooms
- Year Built, Year Remodeled, Garage Year Built
- Fireplaces, Masonry Veneer Area, Lot Area
- Finished Basement Area, Wood Deck Area, Open Porch Area

## Model

- **Algorithm:** XGBoost Regressor
- **Tuning:** GridSearchCV (3-fold CV) over `n_estimators`, `max_depth`, and `learning_rate`
- **Metric:** Mean Absolute Error (MAE)

## Getting Started

This project is designed to run in **Google Colab**.

1. Open `HousePricePrediction.ipynb` in Google Colab.
2. Get a Kaggle API token: go to your [Kaggle account settings](https://www.kaggle.com/settings) → **Create New Token** → this downloads a `kaggle.json` file.
3. Run the notebook cells in order. When prompted, upload your `kaggle.json` — it's used only to authenticate the dataset download and is never stored in this repo.
4. The notebook downloads the dataset, trains the model, and launches a Gradio demo with a public shareable link (temporary, valid up to 7 days).

## ⚠️ Security Note

Never commit your `kaggle.json` file or paste your Kaggle API key directly into the notebook. Always use the interactive upload prompt (`files.upload()`) so credentials stay local to your Colab session.

## Tech Stack

- Python
- pandas, scikit-learn, XGBoost
- Gradio (UI)
- Kaggle API (dataset access)

## License

This project is open source and available for educational use.
