# UFC Classification Project by Luigi Fiori

## Files 

- data_93.csv: Raw Data
- UFC_classification_project.ipynb: Notebook for Analysis
- ufc_project_pdf.pdf: Slide presention
- ufc_data_images: folder containig images used for README

## Introduction

For this project I will be acting as a consultant for a bet site firm and we will be dealing with a classification problem. 

In particular, have been asked to predict who is going to win a potential fight.

Our goal is to create a Machine Learning Model such that we can get some valuable predictions for our company.

We will be working with UFC data containing information about fights from 1993 up till today.

![https://raw.githubusercontent.com/illumi91/dsc-mod-5-project-online-ds-pt-051319/master/images/uf.jpeg](https://raw.githubusercontent.com/illumi91/dsc-mod-5-project-online-ds-pt-051319/master/images/uf.jpeg)

The Database can be found in Keggle and you can download it [here](https://www.kaggle.com/rajeevw/ufcdata).

We'll be following the OSEMN methodology:

1.Obtain

2.Scrub

3.Explore

4.Model

5.Interpret

# Feature engineering

I created several new features taking the difference for the same variable of different fighters, and checked the normality through the histogram and box-plot as shown below:

![ufc](https://raw.githubusercontent.com/illumi91/Predicting-UFC-outcomes/master/ufc_data_images/Capture.PNG)

![ufc](https://github.com/illumi91/Predicting-UFC-outcomes/blob/master/ufc_data_images/box_plot.PNG)

# Model

I applied feaure selection to find the most valuable variables for predicting a fight.

![ufc](https://raw.githubusercontent.com/illumi91/Predicting-UFC-outcomes/master/ufc_data_images/feature_select.PNG)

And implemented several machine learning models for the prediction:

![ufc](https://raw.githubusercontent.com/illumi91/Predicting-UFC-outcomes/master/ufc_data_images/top_mach_learn.PNG)

We can see the confusion matrix for the results:

![ufc](https://raw.githubusercontent.com/illumi91/Predicting-UFC-outcomes/master/ufc_data_images/conf_matr.PNG)

Confusion Matrices show us that Random Forest compared to Logistic Regression is capable of predicting Labels in a more balanced way.
In fact for Logistic Regression we have predicted 252 Red that were actually Blue, while insted for Random Forest is 205.
As we can see our model performed decently overall, in fact it's still significantly better than we would expect from random guessing, which would have ~13% accuracy

Here we can see a plot we the top features for predicting a fight:

![ufc](https://raw.githubusercontent.com/illumi91/Predicting-UFC-outcomes/master/ufc_data_images/top_feat.PNG)

# Now it's your turn predicting a fight!

![ufc](https://raw.githubusercontent.com/illumi91/Predicting-UFC-outcomes/master/ufc_data_images/predict.PNG)

# Conclusion


From our analysis, based on our prediction, we advice our clients when betting to consider in order of importance these factors:

1. Total Number of Losses of the Fighter
2. Age of the Fighter
3. Takedown Capabilities(Related Fighter Background Techniques)
4. Total Number of Rounds Fought


It's important to notice that:
-The prediction is based on the fighter's last 5 fights.
-The model was trained on data from the actual fights between the 2 fighters.