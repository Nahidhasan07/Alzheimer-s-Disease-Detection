# Nahidhasan07-Alzheimer-s-Disease-Detection
We used the OASIS 1 dataset and ten influential machine-learning algorithms to detect AD.
# Code Description
1.Read the two CSV format datasets (oasis_cross-sectional and oasis_longitudinal) and merge them for further pre-processing.	
2. Preprocessed the dataset, like dropping unnecessary features, data labelling and replacing missing values with medium values.
3. Selected top 7 features using DecisionTreeClassifier and function feature_importances.argsort(). Selected top seven features are `CDR', `Age', `Educ', `ASF', `SES', `MMSE', and `eTIV'.
4. Built ten machine learning classifier models and trained those models using preprocessed data. Generate predicted results report using classification\_report().\\
5. For XAI, installed Lime and then randomly selected five data \newline $random\_index = random.randint(0, x\_test\_length - 1)$. \newline Explain the instance's prediction using LogisticRegression, \newline explanation = explainer.explain\_instance(). Display the explanation, explanation.show\_in\_notebook().
