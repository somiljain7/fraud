  # RESAMPLING
  
DATA RESAMPLING-train our models much better to recognize fraud cases when there are only very few cases of fraud.
# Oversampling 
sckit learn's imblearn library


      from imblearn.over_sampling importy RandomOverSampler

      method = RandomOverSampler()

      X_resampled, y_resampled = method.fit_sample(X,y)

#SYNTHETIC MINORITY OVERSAMPLING TECHNIQUE FOR OVERADJUSTING SAMPLES
