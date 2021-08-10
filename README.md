# -Apply-Decision-Trees-on-Donors-Choose-dataset

#### 1. Apply Decision Tree Classifier(DecisionTreeClassifier) on these feature sets
- Set 1: categorical, numerical features + project_title(TFIDF)+ preprocessed_eassay (TFIDF)
- Set 2: categorical, numerical features + project_title(TFIDF W2V)+ preprocessed_eassay (TFIDF W2V)

#### 2. The hyper paramter tuning (best `depth` in range [1, 5, 10, 50], and the best `min_samples_split` in range [5, 10, 100, 500])
- Find the best hyper parameter which will give the maximum AUC value
- Find the best hyper paramter using k-fold cross validation(use gridsearch cv or randomsearch cv)/simple cross validation data(you can write your own for loops refer sample solution)

#### 3. Representation of results
-You need to plot the performance of model both on train data and cross validation data for each hyper parameter.
- Once after you found the best hyper parameter, you need to train your model with it, and find the AUC on test data and plot the ROC curve on both train and test.
- Along with plotting ROC curve, you need to print the confusion matrix with predicted and original labels of test data points

- Once after you plot the confusion matrix with the test data, get all the `false positive data points`
- Plot the WordCloud(https://www.geeksforgeeks.org/generating-word-cloud-python/) with the words of essay text of these `false positive data points`
- Plot the box plot with the `price` of these `false positive data points`
- Plot the pdf with the `teacher_number_of_previously_posted_projects` of these `false positive data points`
#### 4. Task 2: For this task consider set-1 features. Select all the features which are having non-zero feature importance.
- You can get the feature importance using 'feature_importances_` (https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html), discard the all other remaining features and then apply any of the model of you choice i.e. (Dession tree, Logistic Regression, Linear SVM), you need to do hyperparameter tuning corresponding to the model you selected and procedure in step 2 and step 3
- Note: when you want to find the feature importance make sure you don't use max_depth parameter keep it None.

#### 5. You need to summarize the results at the end of the notebook, summarize it in the table format
