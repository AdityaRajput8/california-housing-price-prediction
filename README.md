California Housing Price Prediction
Description
This project predicts housing prices in California using the California Census data from 1990. It employs a machine learning model, specifically a Random Forest Regressor, to estimate the median house value for given districts based on various features.

The project includes a complete pipeline for data preprocessing (handling missing values, scaling numerical features, and encoding categorical features) and model training. The main script can train the model and save it for making predictions on new data.

Key Features
Data Preprocessing: Uses scikit-learn's Pipeline and ColumnTransformer for robust data cleaning and preparation.

Model Training: Implements a RandomForestRegressor to learn from the data.

Inference Script: The main script can be used for both training a new model and loading an existing one to make predictions.

Dataset
The dataset used is the California Housing dataset, which is based on data from the 1990 California census. The data contains one row per census block group.

File: data/housing.csv

Project Structure
california-housing-prediction/
├── data/
│   ├── housing.csv         # Raw training data
│   └── input.csv           # Sample data for prediction
├── .gitignore              # Files to be ignored by Git
├── main.py                 # Main script for training and inference
├── requirements.txt        # Project dependencies
└── README.md               # This file

How to Use
The main.py script is designed to handle both training and prediction.

Training the Model
To train the model, ensure the housing.csv file is in the data/ folder and run the script. The script will automatically start training if it doesn't find a saved model.pkl file.

python main.py

This will create model.pkl and pipeline.pkl in the root directory.

Making Predictions
To make predictions, ensure model.pkl and pipeline.pkl are present. The script will then use the data in data/input.csv and save the results to output.csv.

python main.py
