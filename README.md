# SpameBase-Project

Authors: Eric Rodriguez, Aryeh Freud, Anthony Suvorov, Henry Garkanian

Link to presentation video: https://drive.google.com/file/d/1Vz66wgQyByiremiFUdZ3iS4vFG5jIWrB/view?usp=sharing

#Introduction
- Why was the project undertaken?
The project 'Spambase' was undertaken by the team with the goal of building a system to predict the percentage likelihood of an email being spam based on the email subject line and content.

- What was the research question, the tested hypothesis or the purpose of the research?
The main research purpose was to develop a model that could effectively classify emails as spam or non-spam. The team aimed to explore which features are most effective in determining spam emails. 

#Selection of Data
- What is the source of the dataset? Characteristics of data?
The data source is called 'Spambase' from the University of California Irvine Machine Learning Repository. Some characteristics about the dataset include that it contains 4601 instances with 57 features and 1 target variable. The target variable is binary, 1 for spam, 0 for non-spam. It also includes word frequencies, character frequencies, and capital letter run lengths.

- Any munging or feature engineering?
Yes we have a check for missing values in features and target variables. A train-test split was also used to seperate the data into a scaled-down versions using StandardScaler().  

#Methods
- What materials/APIs/tools were used or who was included in answering the research question?
We used Python within a Jupyter/Colab environment. NumPy and Pandas were used for data manipulation, matplotlib and seaborn for visualization, and scikit-learn for modeling and evaluation. We also used the ucimlrepo package to fetch the Spambase dataset from the UCI Machine Learning Repository. The methods included missing value checks, train-test splitting, and scaling using StandardScaler. This was followed by implementing regression and classification models.

#Results
- What answer was found to the research question; what did the study find? Was the tested hypothesis true? Any visualizations?
Our tests showed that KNN and Logistic Regression predicted emails being spam. The KNN model, with a distance weighting at k = 15, achieved a test RMSE of 0.238, while the Logistic Regression reached an accuracy of 92%. The visualizations we provided support the conclusion that even simple models like these can differentiate spam from non-spam emails. This resulted in our hypothesis being validated. 

#Discussion
- What might the answer imply and why does it matter?
The experiments show that KNN and logistic regression can effectively predict the likelihood of an email being spam. This is with KNN (with a distance weighting at k=15) of getting a test RMSE of 0.238 and logistic regression reaching 92% accuracy. This matters because it shows that even simple models can provide spam detection for email users.

- How does it fit in with what other researchers have found?
Our findings are consistent with what other researchers have found using this Spambase dataset, where traditional models have been successful in correctly identifying emails.

- What are the perspectives for future research?
Future research could use deep learning models to further improve spam detection. With more sophisticated spam emails being released, more advanced models will be necessary to detect them.

- Survey about the tools investigated for this assignment.
Our project used scikit-learn, matplotlib, seaborn, and the ucimlrepo package, among others. These tools offered an environment for data exploration, visualization, and building and evaluating effective solutions for spam detection.

#Important Findings

Data Distribution & Features:
 - The dataset contains spam (1) and non-spam (0) emails; we observed a certain distribution of these classes (see the bar plot above).
 - Some word frequency features (e.g., 'word_freq_email', 'word_freq_table') appear to be more indicative of spam emails.

Model Performance:
 - Using Logistic Regression, the accuracy is shown above (>90%).
 - The confusion matrix indicates how many spam emails are correctly labeled (True Positives), how many non-spam emails are correctly identified (True Negatives), and where our model gets confused (False Positives/Negatives).

Overall Conclusion:
 - A machine learning model can reliably predict the probability of an email being spam based on selected word frequency features. This highlights the potential for an automated spam detection system using these simple yet effective features.

#References
- Hopkins, M., Reeber, E., Forman, G., & Suermondt, J. (1999). Spambase [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C53G6X.

