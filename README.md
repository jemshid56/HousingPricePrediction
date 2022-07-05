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

## app.py  -- Entry point of the code. It performs Train and Validate. This can be modified for Web applicaiton deployment.


## DVC Stages

DVC has 3 stages
- preparing the data, performing train test split
- Training the model and saving the model
- Validating the model with test split, generating the report and graph

![image](https://user-images.githubusercontent.com/47142192/177393533-df06f843-0309-48f0-9592-2b01b2cfbbb7.png)


## Continuous ML
- Github actions are configured for each push
- Everytime a docker instance is created
- It performs the setup using requirement installation
- Then performs the evaluate step of DVC using ''dvc repro evaluat''

## AWS Configuration
- The project has been configured in AWS Cloud9 IDE
- It successfully ran the code
- Able to perform DVC operations and Git operations from cloud.
- The same can be used in future for web app deployment.


![image](https://user-images.githubusercontent.com/47142192/177395538-a507c2d3-f672-43fe-bdb3-920df5801b38.png)
