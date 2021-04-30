Oversampling 
sckit learn's imblearn library

from imblearn.over_sampling importy RandomOverSampler

method = RandomOverSampler()

X_resampled, y_resampled = method.fit_sample(X,y)

SYNTHETIC MINORITY OVERSAMPLING TECHNIQUE FOR OVERADJUSTING SAMPLES


rules base system 

fixed thershold per rule to determine fraud

limited to yes/no outcomes
(binary result)

# Import the packages to get the different performance metrics
from sklearn.metrics import classification_report, confusion_matrix, roc_auc_score

# Obtain the predictions from our random forest model 
predicted = model.predict(X_test)

# Predict probabilities
probs = model.predict_proba(X_test)

# Print the ROC curve, classification report and confusion matrix
print(roc_auc_score(y_test, probs[:,1]))
print(classification_report(y_test, predicted))
print(confusion_matrix(y_test, predicted))


resampling is done traing data not on testing data 

method = SMOTE(kind='borderline1')
X_train,X_test,y_train,y_test=train_test_split(X,y,train_size=0.8,random_state=0)

X_resampled,y_resampled=method.fit_sample(X_train,y_train)

model = logisticRegression()
model.fit(X_resampled,y_resampled)

predicted = model.predict(X_test)
print(classification_report(y_test,predicted)


basic implemetation on random forest 

from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(random_state = 42)
model.fit(X_train,y_train)
predicted = model.predict(X_test)
print(metrics.accuracy_score(y_test,predicted))

precision  = (true positive)/(true positive + false positve)
fraction of actual fraud cases out of all predicted fraud cases

recall = true positive/(true positive + false negative)

fraction of predicte frauds and actual fraud cases

they are inversely proportional to each other.

classification report gives you precision 
recalll
f1 score
support

ROC 
ROC stands for reciver operating characterisitcs curve and is created by plotting
the true positive rate against the false positive rate at various threshold settings.

from sklearn.
# This is the pipeline module we need for this from imblearn
from imblearn.pipeline import Pipeline 

# Define which resampling method and which ML model to use in the pipeline
resampling = SMOTE(kind='borderline2')
model =  LogisticRegression()


# Define the pipeline, tell it to combine SMOTE with the Logistic Regression model
pipeline = Pipeline([('SMOTE', resampling), ('Logistic Regression', model)])

decision tree and random forest classification are most commonly used for fraud detection

tree are transparent and easily interpreted 

Random Forest prevents overfitting most of the time, by creating random subsets of the features and building smaller trees using these subsets. Afterwards, it combines the subtrees of subsamples of features, so it does not tend to overfit to your entire feature set the way "deep" Decisions Trees do.

not in all cases does resampling necessarily lead to better results. When the fraud cases are very spread and scattered over the data, using SMOTE can introduce a bit of bias. Nearest neighbors aren't necessarily also fraud cases, so the synthetic samples might 'confuse' the model slightly



performance metrics

from sklearb.metrics import precision_recall_curve

from sklearn.metrics import average_precison_score

averageprecision = average_precision_score(y_test,predicted)

precision , recall, _ = precision_recall_curve(y_test, predicted)

