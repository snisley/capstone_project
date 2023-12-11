# capstone_project

### Summary of Project
The project aimed to assist Home Credit in mitigating the lending risks associated with unbanked and underbanked populations. Typically, individuals in these categories lack traditional credit scores, posing a challenge for Home Credit. To address this, we combined external and internal data sources to inform loan approval decisions. Our team developed a classification model to predict the likelihood of default, guiding decisions on credit allocation.

### Solution
We chose the XGBoost (eXtreme Gradient Boosting) algorithm for its effectiveness in managing complex datasets like ours. XGBoost's was appealing due to its built-in regularization features, crucial for preventing over-fitting in our high-dimensional, imbalanced dataset. The project focused primarily on data cleaning and hyper-parameter tuning. XGBoost performed best across all of our final datasets, but repeatedly better with advanced data cleaning. 

**Data Cleaning**
We started by eliminating highly improbable outliers and features with zero or near-zero variance. Next, we engineered and evaluated new features using the Ranger package's random forest algorithm. For missing data, we applied mean or median imputation, based on the data distribution. Lastly, we assessed the distribution and skewness of imputed features to ensure consistency with the original data.

**Top Features Post Cleaning**
![important_Features_example](https://github.com/snisley/capstone_project/assets/59975473/5296f1f7-5a88-4875-9124-20f7baa2e66d)

**Final Model and Tuning**
The modeling phase involved extensive experimentation with parameter combinations, using both random and grid search methods. Our model achieved an accuracy surpassing the majority class (92%) and a Kaggle score of 76. The result enables Home Credit to more accurately identify and offer loans to customers while reducing loans to those likely to default. 

**Accuracy Results**
![image](https://github.com/snisley/capstone_project/assets/59975473/7a796aea-3a11-4c31-b4f0-388287322278)

**ROC Curve**
![ROC Curve](https://github.com/snisley/capstone_project/assets/59975473/2d79fe84-b4f3-4df6-a4e9-27ea0646b236)

### My Contribution
Each team member conducted independent exploratory data analysis (EDA) and modeling. However, my dataset and model performed the best overall. Thus, the solution for the project, outlined above, was also my contribution. We all completed the project separately, before coming together as a group for the final model. It was only by luck, that my cleaning and modeling was utilized in totality for the final model. 

### The business value of the solution.
The solution offers value to Home Credit by increasing revenue through interest or fees from additional credit lines and reducing losses from defaulting customers.

### Difficulties that my group encountered along the way
The primary hurdles stemmed from the initial data. First, the class imbalance, with 91% of training data representing non-defaulting customers, complicated the EDA. Second, significant data gaps, particularly in high-importance features, made simple imputation unfeasible. We explored advanced imputation methods, such as the MICE package, but faced computational limitations.  Overall, these challenges were overcome, but added quite a few more hours into the process than we originally expected. 

### What I learned in the project
The project taught me that large datasets can complicate modeling. However, I also learned to transform extensive, flawed data into a predictive dataset, effectively training a model that generalized well to both our test splits and the Kaggle dataset. The overall process gave me much more confidence in my ability, given that most datasets I've used in my career, both professionally and academically, were much cleaner and smaller in comparison.

**Link to final presentation and code**
https://github.com/snisley/capstone_project/blob/main/Capstone_Presentation_and_Results.pdf
https://github.com/snisley/capstone_project/blob/main/EDA_ShaneNisley_withModel.Rmd
