# Alzheimer's-Disease-Detection
We used the OASIS 1 dataset and ten influential machine-learning algorithms to detect AD.

# Data Description
For our research, we use OASIS 1, a publically available dataset https://www.oasis-brains.org/#data for Alzheimer’s disease detection. The OASIS dataset is a collection of 162 MRI scans obtained from individuals with varying age groups and cognitive conditions. 163 The dataset comprises both cross-sectional and longitudinal MRI data of older adults. The 164 cross-sectional subset consists of 416 subjects aged 18 to 96, among which 100 subjects were 165 diagnosed with very mild to moderate Alzheimer’s disease (AD). Each subject underwent 166 3 or 4 T1-weighted MRI scans during single scan sessions. Additionally, the longitudinal 167 subset includes 150 subjects aged 60 to 96, with multiple scans conducted at different time 168 intervals, spanning at least a year. This longitudinal dataset encompasses individuals who 169 remained non-demented throughout the study, those who were initially diagnosed with 170 dementia and remained so in subsequent scans, as well as individuals who transitioned 171 from non-demented to demented over time. The dataset consists of 3 class labels - non- 172 demented, demented and converted. The converted are the individuals who were non- 173 demented at the initial stage and later found out to be demented. For our study, we 174 combined these two datasets and considered the converted class as demented.

# Code Description
1.Read the two CSV format datasets (oasis_cross-sectional and oasis_longitudinal) and merge them for further pre-processing.\\
2. Preprocessed the dataset, like dropping unnecessary features, data labelling and replacing missing values with medium values.
3. Selected top 7 features using DecisionTreeClassifier and function feature_importances.argsort(). Selected top seven features are 'CDR', 'Age', 'Educ', 'ASF', 'SES', 'MMSE', and 'eTIV'.
4. Built ten machine learning classifier models and trained those models using preprocessed data. Generate predicted results report using classification\_report().
5. For XAI, installed Lime and then randomly selected five data $random_index = random.randint(0, x_test_length - 1). Explain the instance's prediction using LogisticRegression, explanation = explainer.explain_instance(). Display the explanation, explanation.show_in_notebook().
