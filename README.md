# credit_risk
# Challenge Analysis
The goal of this analysis is to perform machine learning on credit applications in order to identify applications that are high risk and those that are low risk. Because the majority of applications are low risk, the classes that we will categorize into are imblanaced. Therefore, tested various over and under sampling technqiues to address these imbalances.

1. Naive Random Oversampling
- In this approach, we oversampled the high risk group in a random manner.
- The precision (specificity) of this model for high risk loans was low at 1%, meaning our algorithm flagged many loans for being high risk that ultimately would not be. The recall (sensitivity) for high risk loans was 70% so the model catches 70% of all the actual high risk loans.
- For low risk loans, we had near 100% precision meaning most of the loans that we predict to be low risk, are low risk. The recall for low risk loans was 60% reflecting that a decent number of low risk loans are mistakenly classified as high risk by the model.
- The balanced accuracy score was 65.2%.

2. SMOTE Oversampling
- In this approach, we oversampled using the SMOTE algorithm.
- The results were similar to the random oversampling method.
- The precision (specificity) of this model for high risk loans was low at 1%, meaning our algorithm flagged many loans for being high risk that ultimately would not be. The recall (sensitivity) for high risk loans was 62% so the model catches 62% of all the actual high risk loans.
- For low risk loans, we had near 100% precision meaning most of the loans that we predict to be low risk, are low risk. The recall for low risk loans was 69% reflecting that a decent number of low risk loans are mistakenly classified as high risk by the model.
- The balanced accuracy score was 65.5%.

3. Undersampling
- In this approach, we undersampled using the Cluster Centroids algorithm.
- The precision (specificity) of this model for high risk loans was low at 1%, meaning our algorithm flagged many loans for being high risk that ultimately would not be. The recall (sensitivity) for high risk loans was 69% so the model catches 69% of all the actual high risk loans.
- For low risk loans, we had near 100% precision meaning most of the loans that we predict to be low risk, are low risk. The recall for low risk loans was low at 39% reflecting that a high number of low risk loans are mistakenly classified as high risk by the model.
- The balanced accuracy score was 53.9%.

4. Combination sampling
- In this approach, we combined over and under sampling.
- The precision (specificity) of this model for high risk loans was low at 1%, meaning our algorithm flagged many loans for being high risk that ultimately would not be. The recall (sensitivity) for high risk loans was 75% so the model catches 75% of all the actual high risk loans.
- For low risk loans, we had near 100% precision meaning most of the loans that we predict to be low risk, are low risk. The recall for low risk loans was 56% reflecting that a decent number of low risk loans are mistakenly classified as high risk by the model.
- The balanced accuracy score was 65.8%.

## Overall Recommendation
Overall, I would not recommend any of these models. The most important thing for this model would be to catch all the high risk loans that could be looked at for further evaluation, but the best of these models for that (combination) was only 75% meaning 1 out of every 4 high risk loans would be missed even in the best case scenario. Further, the imbalanced nature of the sample is why our precision for low risk loans is consistently very high (there are many more of these loans than anything else). Thus, it would be exceptionally hard to identify the relatively few high risk applications from the large number than are classified as low risk by the model. Thus, these model could put the company on the hook for significant risk and ultimately I cannot recommend them. If we do need to use a model, the best performing model by balanced accuracy score is the combination sampling so that is what I would recommend.
