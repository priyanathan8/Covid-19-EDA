# Covid-19-EDA

Executive Summary

Background

As new employees of the Public Health Agency of Canada, we were asked to examine a
dataset containing information on COVID-19-related behaviours collected by the
Institute of Global Health Innovation Imperial College London. We were tasked with
preparing the data, carrying out exploratory data analysis and creating an optimal k-NN
model to carry out our analysis of the dataset.

Most salient findings

Through our Exploratory Data Analysis (EDA), we found that while observations were
different for Canada and the USA, the trends in all variables were quite similar. Also,
there were a lot of variables with missing values which we dealt with using a variety of
methods. We also noticed that the data is not representative in terms of age.
After our EDA, we created a KNN classifier. A key part of this was identifying the
relevant predictors to include in the model and to do this, we narrowed down the pool
of predictors using our findings in the EDA section and by examining the correlations
between our variables. Finally, after fitting the model, we compared the importance of
the variables included in our model with the use of DecisionTreeClassifier. The most
important predictor is i12_health_16, “Avoided going to shops”. This makes sense as
avoiding going to shops would be a very good indicator of whether an individual avoids
going out in general.
For the model creation portion of our task, we created a version of the target variable,
“Avoided going out in general” (i12_health_6), which binned its five existing categories
into two categories that represented going out versus not going out. This essentially
turned our target variable into a binary variable. After tuning our model parameters and
carrying out our predictions, we found that the KNN classifier had a higher accuracy
when the binary version of the target variable was used. A binary variable also has
positive feasibility implications for future studies as it is easier to gauge if someone goes
out or not versus gauging how much a person goes out.
The model was tuned by determining the optimal k value and by using the Decision Tree
Classifier feature importance score. We used K-fold cross-validation processes to avoid
overfitting. In the end, we found that the optimal K value was k= 19. When this value of
k was used, the KNN model had the highest accuracy.
