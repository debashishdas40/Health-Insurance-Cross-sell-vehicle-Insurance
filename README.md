# Health-Insurance-Cross-sell-vehicle-Insurance
![image](https://user-images.githubusercontent.com/30859632/183071857-ebc792c9-e566-4654-a8df-cbff448ee681.png)




Health Insurance Cross sell vehicle Insurance
Cross-selling to existing clients has been one of the primary methods of generating new revenue for many businesses. Identifying the potential buyers among existing clients can help a company plan its communication strategy accordingly, thereby optimizing its business model and increasing revenue. In this project, our goal was to use the Health Insurance Cross-Sell dataset to understand Vehicle Insurance Cross Sale Responses, apply machine learning techniques to identify Vehicle Insurance buyers among pre-existing policyholders and provide explanations from the best classifying model to understand factors affecting customer responses.

The important observations identified during EDA were:

Most customers that purchased vehicle insurance had existing damages in their vehicles, were not previously insured and owned vehicles aged over a year.
It was also observed that most policyholders of the health insurance company come from three region codes: 28, 8 and 41.
The policy sales channels most preferred to reach out to the clients were channel numbers 152, 26 and 124
The obstacles identified in the EDA phase of the project were:

The highly imbalanced dataset, with only 12.25 per cent of positive responses observed.
Categorical attributes like Region Code and Policy Sales Channel contained over fifty categories.
Vehicle Age attribute categorized a vehicle’s age into three categories in the form of strings.
The numerical features, Annual Premium, contained a notable number of outliers.
These obstacles were overcome in the Feature Engineering phase of the project, when:

Categories that occur less than 5 per cent of the time were binned together and recognized as ‘Rare’.
The age of the client’s vehicle was numerically encoded.
Outliers in Annual Premium were capped at their lower and upper quartiles.
Categorical features were One Hot Encoded in order to be interpreted as categories.
After Feature Engineering, the dataset was scaled and split into training and testing sets. Three sampling techniques, namely: Tomek Links, Synthetic Minority Oversampling Technique (SMOTE) and SMOTE-EditedNearestNeighbors were performed on the training set in order to counter the Imbalanced Dataset.

Eight models, namely Logistic Regression, Gaussian Naive Bayes, Decision Trees, Gradient Boosting, CatBoosting, LightGBM, Bagging and Random Forest were tested and evaluated based on their F2 scores. F2 score was the preferred metric as it gave emphasis in minimizing false negatives and was relevant as it could help identify maximum a number of potential customers.

Upon model deployment, tuning and evaluation, we found that the best performing model was the Gaussian Naive Bayes classifier trained on SMOTE sampled training set with an F2 score of 0.634614, precision of 27.58 per cent and recall of 94.02 per cent. The finalized model’s predictions were dependent on the customer’s previous insurance status and existing damages on the vehicle.

When the dataset was explored earlier in the project, approximately, one in every ten clients had a positive cross-sale response when they were approached for cross-sale (12.25 % success rate). From the confusion matrix, we were able to tell that the model had correctly identified 94.04 per cent of the positive responses with a success rate of 27.58 per cent in predicting positive responders. This means that, approximately, three out of every ten predicted buyers produced a positive response.

Therefore, the model not only helped identify a large part of the potential vehicle insurance buyers but had also increased the success rate of cross-sales, helping the company save a significant amount of time and resources by generating better leads.



# ML Models Used ![image](https://user-images.githubusercontent.com/30859632/183070499-4e4bf4d5-cce2-4a88-b94d-e99200dc0dbb.png)
![image](https://user-images.githubusercontent.com/30859632/183070586-7a99fc4d-f6fe-457e-9c56-40a96facffda.png)


Hyper-Parameter Tuning metod used:
1. GridSearch CV
![image](https://user-images.githubusercontent.com/30859632/183070672-e42a7839-a2d0-46f6-a681-eab5dd0f84f6.png)

# Results obtained after Training the Dataset :![image](https://user-images.githubusercontent.com/30859632/183070768-f904b32f-edd4-4c89-ae34-79715b62cc01.png)

![image](https://user-images.githubusercontent.com/30859632/183070719-9cb810c8-8d8d-4e72-839c-d9c873dbba71.png)

After training the models and comparing the results, it can be said that the XGBoost
Classifier model has performed better than the other models.
![image](https://user-images.githubusercontent.com/30859632/183070809-893adb44-c260-4254-a3af-d537d95f18f3.png)

Feature Importance:![image](https://user-images.githubusercontent.com/30859632/183071090-b6cefc26-8e19-4044-b8a8-2b2198b2154e.png)

![image](https://user-images.githubusercontent.com/30859632/183070869-b5a47bc1-1d2e-4f0c-bcaa-677137120886.png)


Previously Insured and Vehicle Damage are most important  features according to XGB Model.
![image](https://user-images.githubusercontent.com/30859632/183071111-59efc0b1-7ce4-4f42-ad6c-f93be36b47cc.png)

![image](https://user-images.githubusercontent.com/30859632/183071166-cc2dac2a-6355-4ad3-893c-de33ba48a9d2.png)
![image](https://user-images.githubusercontent.com/30859632/183071424-01294208-26b3-414b-a98f-f2eb105a6450.png)

This means our model can improve our response rate for predicting customers who interested in subscribing vehicle insurance
![image](https://user-images.githubusercontent.com/30859632/183071195-af88d895-8c42-4c47-a085-826896f1d822.png)



