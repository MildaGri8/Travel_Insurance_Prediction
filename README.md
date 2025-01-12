## Travel Insurance

**Objectives**
- Practice performing EDA.
- Practice applying statistical inference procedures.
- Practice using machine learning models.
- Practice visualizing data.

**IMPORTANT: plotly.express is used for graphs in this work. To see them, Notebook has to be run locally**

**Context**

Kagle data set [Travel Insurance](https://www.kaggle.com/datasets/tejashvi14/travel-insurance-prediction-data/data) is used for analysis. 

*A Tour & Travels Company is offering Travel Insurance Package to their customers. The new Insurance Package also includes Covid cover. The company requires to know which customers would be interested to buy it based on its database history. The Insurance was offered to **some** of the customers in 2019 and the given data has been extracted from the performance / sales of the package during that period. The data is provided for almost 2000 of its previous customers and there is a requirement to build an intelligent model that can predict if the customer will be interested to buy the travel insurance package based on certain parameters.*

### Project Goal
The purpose of this project is to analyze the Travel Insurance dataset and, create Machine Learning model that can predict if customer will be interested in buying Travel Insurance package.

### Summary
- EDA is important in understanding data and observing patterns and potential relationships.
- Metric choice matters a lot. Wrong metric can lead to model generalization on the wrong target. This is especially important with imbalanced datasets. For example model can learn to predict Target group - 0 better, if used metric is accuracy. Having this in mind PR AUC metric was used in this work which balances trade - off between precision and recall.
- Analyzed various models like: Logistic regression, SVM, K-nearest neighbours, Naive Bayes, Decision Tree, Random Forest. 
- From PR AUC and Recall results some models were selected for further analysis and hyperparameter tuning.
- Hyperparameter tuning is important step of modeling, as it can significantly improve results (e.g. Decision Tree in this project). With hyperparameter tuning it is possible to make model either more specific (too specific - risk of overfit) or make better at generalising (too generalized - risk of underfit). 
- Ensemble models tend to provide better results as they can utilize strong sides of each of base model used in ensemble. This is specifically valid when base models are of different types.
- Changing threshold, model can be adjusted to business needs e.g. prioritizing one type of error over the other.

### Suggestions for additional analysis and improvement
- Try models on full train dataset without duplicate removal to see if that can improve performance.
- Use random search for finding best hyperparameters as this may improve results compare to grid search.
- Try models which were not used, to see how they perform after hyperparameter tuning and in the ensemble.
- Try modeling without engineered features.
- Create additional engineered features (e.g. interaction between features) and try models with them.



### Structure
insurance.ipynb: Jupyter Notebook for this project,

TravelInsurancePrediction.csv: data set for this project,

README.md: Provides an overview and instructions for the projects.

requirements.txt: Provides list of packages to be installed what will be needed for anlysis.

```
pip install -r requirements.txt