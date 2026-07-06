# FraudShield BI Module 8 Presentation Script

## Slide 1 - Title
Good day, my name is Atta Febri-Yeboah. My capstone project is FraudShield BI: Quantifying the Impact of False Positives in Credit Card Fraud Detection. The main idea behind this project is that fraud prevention should not only be judged by how much fraud it catches. It also needs to be judged by how much unnecessary disruption it creates for legitimate customers. In this presentation, I will summarize the business problem, the dataset, the methods, the model results, the threshold and cost analysis, and how the Power BI dashboard turns the findings into a decision-support tool.

## Slide 2 - Business Problem
The business problem I studied is the tension between fraud protection and customer experience. A fraud model can look effective if it catches suspicious activity, but if it creates too many false positives, it can also create a hidden cost. Those costs may include manual review, customer service contact, declined purchases, and reduced customer trust. My project calls this the False Positive Tax because it is a cost that may not be visible if the organization only focuses on model accuracy.

## Slide 3 - Research Questions and Hypotheses
The project was guided by three research questions. First, I studied how changing the classification threshold affected false positives, fraud detection, and estimated cost. Second, I examined which transaction characteristics were associated with false positives. Third, I evaluated how a dashboard and scenario analysis could help decision-makers compare fraud prevention with customer friction. The analysis led to rejection of all three null hypotheses because the data showed meaningful changes across thresholds, transaction segments, and cost scenarios.

## Slide 4 - Dataset and Ethics
The dataset came from the Kaggle credit card transactions fraud detection dataset, which was generated using Sparkov and contains simulated transaction records. I used the training file with 1,296,675 records and the testing file with 555,719 records. The fraud rate in the training data was only about 0.579 percent, which confirmed that this was a highly imbalanced classification problem. The supplied train/test files were practical for the capstone, but a production version should also use a validation sample and an untouched holdout sample for threshold selection and final confirmation. Ethically, I did not use employer data, real customer data, or internal fraud procedures. I also excluded direct identifiers such as credit card number, names, transaction number, street address, and merchant name.

## Slide 5 - Exploratory Findings
The exploratory analysis showed that fraud was not evenly distributed. Some transaction categories had much higher fraud rates than others. Online shopping, miscellaneous online transactions, and grocery point-of-sale transactions were among the highest categories. Time of day also mattered. The fraud rate increased sharply around 10:00 p.m. and 11:00 p.m., while most daytime hours were much lower. These patterns helped support the idea that transaction characteristics are important when evaluating fraud and false-positive decisions.

## Slide 6 - Model Comparison
I compared class-weighted logistic regression with histogram-based gradient boosting. Logistic regression was useful as an interpretable baseline, but at the default 0.50 threshold it produced 67,204 false positives and only 2.31 percent precision. Gradient boosting performed much better. It produced only 163 false positives, with 91.14 percent precision, 78.18 percent recall, and an F1-score of 84.17 percent. This was one of the strongest findings in the project.

## Slide 7 - Threshold and False-Positive Impact
Threshold analysis was important because the default 0.50 cutoff is not automatically the best business choice. Lower thresholds catch more fraud but can also raise false positives and review volume. Higher thresholds can reduce alerts but may miss more fraud. The false-positive analysis also showed that the burden was not evenly distributed. Travel transactions had the highest false-positive rate at about 13.02 percent, and the 11 a.m. hour had the highest hourly false-positive rate at 2.83 percent. These results show why threshold decisions should account for customer friction, review capacity, and high-impact segments.

## Slide 8 - Cost Scenario Analysis and Power BI Decision Support
The cost scenario analysis applied low, moderate, and high assumptions to false-positive cost and missed fraud cost. Gradient boosting produced the lowest estimated total cost in every scenario. Under the moderate-cost scenario, the recommendation was gradient boosting at a 0.10 threshold, with an estimated total cost of $93,392.28 and 1,173 false positives. The Power BI dashboard then translated these model outputs into a decision-support report with an executive overview, threshold decision lab, cost and recommendation page, and false-positive deep dive. This helped move the project from a technical model comparison to a business discussion.

## Slide 9 - Conclusion, Validation Notes, and Final Package
In conclusion, this project showed that fraud detection should be evaluated as both a technical and business problem. Accuracy alone is not enough in an imbalanced fraud dataset. Gradient boosting was the stronger model, and threshold selection changed the practical business outcome. For future validation, a production version should use a validation sample and an untouched holdout dataset, test false-positive costs that vary by transaction value, repeat segmentation using the selected gradient boosting threshold, and evaluate fairness with and without sensitive attributes such as gender. The final GitHub package includes the README, validated outputs, charts, final research paper, presentation materials, dashboard files, and dataset instructions.

## Slide 10 - References
This final slide lists the key references used to support the project. The literature and data sources helped frame the study around class imbalance, fraud detection, cost-sensitive evaluation, research design, identity and authentication guidance, and the operational risk of false alerts. These sources support the overall recommendation that fraud models should be governed using both technical performance and business impact.

