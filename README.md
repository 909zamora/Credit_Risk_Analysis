# Credit_Risk_Analysis

### Overview of Analysis
The purpose of this analysis was to see what model does the better job at predicting credit risk using different attributes of customers like interest rate, last payment date, installments, homeownership, rent / mortgage, etc. At the end of the analysis we were able to decide on what model was the best fit to predict something like a high credit risk. Since there are few high risk for every low risk entries, it is harder to call the high risk accounts with precision. 


### Results
Oversampling & Random Oversampling & the combination of both using SMOTEEN were all really good at predicting the low_risk but that was a given since the data had a lot more low_risk profiles than the high_risk ones. Their accuracy scores when compared to the actual data were 65.5% for RandomOversampling / 63.4% for SMOTE Oversampling / 51.3% as shown in the images https://github.com/909zamora/Credit_Risk_Analysis/blob/main/SMOTEOversampling.JPG  https://github.com/909zamora/Credit_Risk_Analysis/blob/main/RandomOversamplingResults.JPG
https://github.com/909zamora/Credit_Risk_Analysis/blob/main/SMOTEENResults.JPG

However, this was not good or reliable because their precision was all .01 meaning that they do not do a good job of actually calling the high credit risk.
### Summary
However, the RandomForest Classifier had a precision rate of 71% meaning that it was correct on high credit risk 71%, this is a huge improvement and does a great job at identifying bad credit. https://github.com/909zamora/Credit_Risk_Analysis/blob/main/RandomForestResults.JPG The Ada Boost classifier had a precision of .07 but since that is significantly low compared to .71, we can confirm that the best model is the RandomForestClassifier. Precision is more important than sensitivity here because precsion gives you the % of True Positive / True Positives + False Positives, in other words it will tell you if it is actually a high risk account or person at a pretty accurate rate if we are judging by a 70% fail pass. It's f1 score was also .47, meaning that it was not low compared to the other and has a good harmonic mean of sensitivity and precision. 

