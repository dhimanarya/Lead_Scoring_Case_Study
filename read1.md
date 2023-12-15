"X Education, an online course provider, faces challenges with its lead conversion rate, which currently stands at 30%. The company wishes to improve the efficiency of its lead conversion process by identifying the most potential leads, referred to as Hot Leads, by assigning a score to each lead. The target is to increase the lead conversion rate to around 80%, a significant improvement from the current rate. 
Several steps were performed, as outlined below (for details, refer to code comments).
Step 1: Reading and Observing 
•	Corrected the datatype of incorrect datatypes
•	Identified all missing and null values
•	There were columns having select as class. Relabelled then as Missing.
•	Dropped redundant data such as Prospect ID & Lead Number
 
Step 2: Data Cleaning & EDA
•	Variable are split into categorical and Numerical groups based on datatype
•	Variables such as Asymmetrique Activity Index,Asymmetrique Profile Index,Asymmetrique Activity Score, Asymmetrique Profile Score with more than 40% missing are dropped  
•	Identified all 0 variance variables and dropped them
•	Merged various classes with very low counts into a single class for various variables
•	Categorical data is analysed using univariate and Bi variate analysis and imputing is done based on conditions
•	All "Yes" and "No" values are converted into 1s and 0s
•	For numerical variables, outliers identified and their treatment is done
•	Missing value are imputed with median if variables are there and with mean if no outlier is present.
Step 3: Encoding and standardizing
•	All the categorical data is converted into dummy variables.
•	All numerical values are standardised using StandardScaler()
•	Correlation checks and highly corelated are dropped.
Step 4: Modeling
•	Basic model i.e., Minimum viable product (MVP) is trained and Evaluated on training dataset
•	Multiple models are trained using different variables to introduce complexity based on automated technique RFE and VIF.
•	To further reduce variables, manual feature dropping is performed using the model summary.
•	Final model summary
•	 
Step 5: Evaluation and Threshold calculation
•	ROC curve is plotted using the model to know evaluate the performance compared to the MVP. AUC is .91
 
•	Accuracy, recall and precision score are compared with MVP score
•	Threshold value is calculated using the Precision-Recall curve. 
•	Threshold value come as 0.51
Step 6: Evaluation on Test dataset
•	Using threshold prediction are adjusted and the final evaluation is done on the training dataset
•	Accuracy, recall, precision is calculated and evaluated against the score of training set.
•	True positive rate, false negative which are important in this are calculated.
•	Model evaluations are as follows
Training Set	Evaluation Metrics	Test set
.92	Recall Score	.93
.89	Precision Score	.88
.92	Accuracy	.92
.93	Specificity	.92
.08	False Negative rate	.07

Summary 
•	The model provide Score to each lead on a scale  of 0 to 100 higher the number more is the probability of getting into converted. 
•	Any lead with a Lead  score more than 51(threshold) can be considered as Hot Lead.
•	The model has an accuracy of 92% and an average false positive rate of 7.5%.

" 
