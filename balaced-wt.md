
2 simple options to tweak your model for heavyily impbalanced fraud data

balanced weight
model = RandomForestClassifier(class_weight='balanced')

balanced_subsample model 
model = 

RandomForestClassifier(class_weight='balanced_subsample')
only difference btw balanced_subsample and balanced :
weights are calculated again at each iteration of growing a tree in the random forest.



balanced can be applied to other classifiers 
whereas balanced_subsample is for only random forest classifier

HYPERPARAMETER TUNING FOR FRAUD DETECTION

GridsearchCV evaluates all combination of parameters we define in the parameter grid

