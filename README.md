# HousingPricePrediction

The predicts the housing price using California Housing dataset. 
ML Model used in LinearRegression. Metrics are MAE and MSE.
The repository is configured with DVC and CML. 
The github actions will be carried out upon code push.


Following is the file structure

## src -- Source code direcory
      prepare_data.py   -- Preparing the California Housing Dataset. Splitting into Train and Test
      train.py          -- Performing the training with baseline Linear Regression model
      evaluate.py       -- Performing validation using the test split (20%)

## report -- Generated Reports
      score.json        -- Report containing the MAE and MSE scores
      prediction.png    -- Scatter plot showing the Prediction vs. Ground Truth

## saved_models -- 
      housing_model.h5  -- Model saved using the pickle utility

## app.py  -- Entry point of the web application
