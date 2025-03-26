# Bank Marketing Prediction

**Jupyter Notebook with code, experimentation, further insights, and deployment strategies: [here](https://github.com/JunGaoca/bankMarketingPrediction/blob/main/bank-marketing-prediction.ipynb).**

## Business Goal
The goal of this project is to build a predictive model for banking client subscriptions that maximizes accuracy while minimizing the number of contacts in marketing campaigns. This strategy aims to optimize resource allocation, reduce unnecessary outreach, and enhance client engagement.

## Data
The dataset comes from the [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/222/bank+marketing). The data is from a Portuguese banking institution and is a collection of the results of multiple marketing campaigns. The dataset contains 41,188 entries and 20 features.

## Modeling and Performance
In this project, we implemented multiple classifiers to predict the success of future marketing campaigns. The models explored include K-Nearest Neighbors, Logistic Regression, Decision Trees, and Support Vector Machines. Each model was trained and tested using a train/test split, followed by cross-validation and hyperparameter tuning with GridSearchCV to optimize performance. Evaluation metrics included accuracy, precision, recall, F1-score, runtime, and the confusion matrix.

Logistic Regression emerged as the most effective model, achieving the highest recall (0.86631) and F1-score (0.588663). This ensures that the bank captures most potential deposit subscribers while keeping false positives at a manageable level, enabling effective client engagement with balanced precision.

If precision is the priority which means minimizing wasted marketing efforts on non-subscribers, then SVM performs best. However, its long training time makes it impractical for frequent retraining.

## Interesting Findings
- Higher durations push the prediction toward subscription (positive impact). This suggests that longer calls are associated with a higher likelihood of the client subscribing, which aligns with the intuition that more engagement leads to better conversion.

- Lower euribor3m values have a strong impact on predicting subscription (positive impact). This likely reflects that lower euribor rates might make deposits more attractive to clients.

## Actionable Insights
- **Enhance targeting strategy** by prioritizing high-recall models to ensure the bank reaches most potential subscribers, reducing missed opportunities.

- **Optimize campaign timing** by incorporating economic indicators. Factors like euribor3m impact customer decisions, making it crucial to target campaigns when deposit interest rates are favorable.

- **Refine customer segmentation** by utilizing feature importance. Key factors such as call duration and previous campaign success can help tailor marketing efforts to the right audience.


## Conclusions and Next Steps
This project employs the CRISP-DM framework to evaluate and refine four classifers for predicting client subscription to a term deposit. The most effective model is Logistic Regression, offering an optimal balance of F1-score, training efficiency, and interpretability.

#### Next Steps
- Balancing the Dataset: Address class imbalance using SMOTE and explore additional balancing techniques.
- Model Ensembling: Investigate stacking or bagging methods (e.g., Random Forest) to improve the F1-score and reduce prediction variance.