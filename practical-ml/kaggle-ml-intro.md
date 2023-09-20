# Kaggle's Intro to ML
https://www.kaggle.com/learn/intro-to-machine-learning

(and some separate googling)

## Models
A **model** is essentially an algorithm that can identify patterns or make predictions on unseen data.

At its simplest, it can be a decision tree with two options.

- **Fitting** or **training** the model: capturing patterns from the data
- **training data**: the data used to fit the model

Fitted models can be used to make predictions from new data.

- **prediction target (`y` by convention)**: the column to be predicted
- **features**: columns that are inputted into the model (and used to make predictions later)
  - data selected from features = `x` by convention

## Steps to Building & Using a Model

1. **Define**: What type of model will it be?
1. **Fit**: Capture patterns from provided data. The heart of modeling.
1. **Predict**
1. **Evaluate**: Determine how accurate the model's predictions are.

## Validating Models

You'll want to evaluate almost every model you build.

First step: summarize the model quality.

- **Mean Absolute Error (aka MAE)**: the average of the absolute value of each error (error = actual - predicted). "On average, our predictions are off by about X."
- **validation data**: Data unseen by the model used to test the model's accuracy

## Underfitting & Overfitting

Leaves with very few categories will make predictions that are quite close to actual values, but may make very unreliable predictions for new data.

**overfitting**: when a model matches the training data almost perfectly, but does poorly in validation and other new data.

**underfitting**: when a model fails to capture important distinctions and patterns in the data and performs poorly even in training data.

## Random Forests

- a step more specific than decision trees
- random forest uses many trees, and makes a prediction by averaging the predictions of each component tree.