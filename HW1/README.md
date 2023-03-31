# Regression - PM2.5 concentration prediction

## Description

This code is about regression. According to **train.csv**, I used regression to find the relationship between the concentration of PM2.5 and other factors in the air.

In **test.csv**, every 8 rows is a group, which is the data during consecutive 8 hours at some place. My code can predict the concentration of PM2.5 of the next hour (the 9-th hour) with RMSE 3.20052, which is ranked 4 among 86 students.

## Files

* **train.csv** : training datset
* **test.csv** : testing dataset
* **submit.ipynb** : The code I train, test, and evaluate
* **my_sol.csv** : the prediction to the testing dataset
* **report.pdf** : My report
* **b09902005_hw1_bonus.pptx** : The slides of my bonus report
* **b09902005_hw1_bonus.mp4** : The video of my bonus report

## Usage

Run **submit.ipynb** on Google Colab. It will automatically download **train.csv** and **test.csv**, and figure out the regression function then use it to make prediction in **my_sol.csv**.

## What I've done    

### Preprocessing

I standardized all the feats (columns) into their Z-score and removed extreme values (those with Z-score > 3 or Z-score < 3).

Then, if the correlation coefficient between a feat and PM2.5 is too close to 0, I ignore those feats to prevent from over-fitting. (In fact, this indeed better the performance.)

### Training & Testing
I performed 1st-order performance regression on the training data.

After standardizing the testing data, I use the 1st-order polynomial to estimate the concentration of PM2.5.

## Performance

In private leaderboard, my RMSE (root-mean-square error) is 3.20052.

(Thus my MAE (mean absolute error) is smaller than 1.8)

which is ranked 4-th among 86 students.
