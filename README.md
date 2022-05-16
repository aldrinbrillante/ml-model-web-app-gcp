# ml-model-web-app-gcp

Deploying a ML model web app on GCP through a CD pipeline

### Prerequisites

- Scikit Learn
- Pandas
- Numpy
- Flask

## Dataset used:

We will be using the 50_Startup.csv data from kaggle located [here](https://www.kaggle.com/datasets/karthickveerakumar/startup-logistic-regression) where the goal is to train a regression model (f(X)) using the three features (x₁,x₂,x₃) as (R&D Spend, Administration Cost, Marketing Cost), and predict the company ‘Profit’ (Y).

## ML Model Flask-Deployment

This is
a project to elaborate how Machine Learn Models are deployed on production using Flask API

### Project Structure

This project has four major parts :

1.  model.py - This contains code fot our Machine Learning model to predict employee salaries absed on trainign data in '50_Startup.csv' file.
2.  app.py - This contains Flask APIs that receives employee details through GUI or API calls, computes the precited value based on our model and returns it.
3.  request.py - This uses requests module to call APIs already defined in app.py and dispalys the returned value.
4.  templates - This folder contains the HTML template to allow user to enter employee detail and displays the predicted employee salary.

### Running the project

1.  Ensure that you are in the project home directory. Create the machine learning model by running below command -

```
python model.py
```

This would create a serialized version of our model into a file model.pkl

2.  Run app.py using below command to start Flask API

```
python app.py
```

By default, flask will run on http://127.0.0.1:5000/ (localhost)

3.  Navigate to URL http://127.0.0.1:5000/ (localhost)
