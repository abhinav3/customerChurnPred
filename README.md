# customerChurnPred
Dataset used is from opensourced kaggle telecom customer churn data : https://www.kaggle.com/blastchar/telco-customer-churn

Classification model evaluation metrics :
	Precision, recall, F1 score etc.


Types of errors in classification : 
	Type 1 error : Failed to reject the null hypothesis. False positives..
	Type 2 error : Wrongly Accepts the null hypothesis. False negatives..

f-beta score formula : (1 + beta^2)/(beta^2 * precision + recall)

When precision is more important :
	Use f-beta score with beta=0.5
	eg : Email spam 

When recall is more important :
	Use f-beta score with beta=0.5
	eg : A brand discount campaign to elite customer in e-commerce.

When precision and recall both are important :
	Use f-beta score with beta=1.0
	eg : For finance institutions they should give enough loans to earn enough interest to run it while at the same time not give to bad customers who might not return it.

When imbalanced classes : 
We use Micro-average method, where we sum up the individual true positives, false positives, and false negatives of the system for different sets and the apply them to get the statistics.
Use F1 micro score.
	Formulation is :
	Micro-average of precision= (𝑇𝑃1+𝑇𝑃2)/(𝑇𝑃1+𝑇𝑃2+𝐹𝑃1+𝐹𝑃2)
	Micro-average of recall= (𝑇𝑃1+𝑇𝑃2)/(𝑇𝑃1+𝑇𝑃2+𝐹𝑁1+𝐹𝑁2)

Macro-average Method :
This is straight forward. Just take the average of the precision and recall of the system on different sets. Suitability Macro-average method can be used when you want to know how the system performs overall across the sets of data.
	Macro-average precision=𝑃1+𝑃2/2
	Macro-average recall=𝑅1+𝑅2/2
