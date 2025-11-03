
# Predicting Adult Autism

96% accurate positive adult ASD flag using a support vector classifier with 6 questions from the AQ-10 and 5 non-behavioral patient attributes.


## ![AutismSpeaks](https://github.com/user-attachments/assets/ffd56063-76ab-4fc7-bd47-ac9eec9d2857)

Acknowledgements

 - [Allison, C., Auyeung, B., & Baron-Cohen, S. (2012). Toward brief “Red flags” for autism screening: The short autism spectrum quotient and the short quantitative checklist in 1,000 cases and 3,000 controls. Journal of the American Academy of Child & Adolescent 
Psychiatry, 51(2). doi: 10.1016/j.jaac.2011.11.003](https://docs.autismresearchcentre.com/papers/2012_Allisonetal_JAACAP_RedFlags.pdf)
 - [Thabtah, F. (2019). An accessible and efficient autism screening method for behavioural data and predictive analyses. Health informatics J. 2019 Dec;25(4):1739-1755. doi: 10.1177/1460458218796636. Epub 2018 Sep 19.](https://pubmed.ncbi.nlm.nih.gov/30230414/)



## Authors
Christopher Stemm 





## Data Source
Dr. Fadi Fayez Thabtah of the Department of Digital Technology, Manukau Institute of 
Technology in Auckland, New Zealand has provided a dataset of 704 observations of adults 
screened for ASD with 20 features. The data is available for download at the UC Irvine Machine 
Learning Repository [Adult ASD](https://archive.ics.uci.edu/dataset/426/autism+screening+adult). The dataset includes nine patient attributes and ten binary 
responses to the Autism Spectrum Quotient (AQ-10-Adult). The features also include the total 
score of the AQ-10 responses and a binary decision class of yes or no for the possibility of ASD.
## Project Summary
This project demonstrates computational techniques to predict autism spectrum disorder 
in the adult population. The project's main goal was to develop a practical and accurate screening 
algorithm for clinicians to identify probable cases for formal evaluation. An optimized support 
vector classifier (SVC) and XG Boost classifier were trained using responses to six of the ten 
questions on the Adult Spectrum Quotient for adults and five non-behavioral attributes. On a 
hold-out test set of 141 subjects, the SVC predicted autism with an accuracy of 0.96 and a macro 
average F1 of 0.95. Only one false positive out of 104 true negatives was predicted, which is 
important because of the barriers to seeking a formal diagnosis. There are two compounding 
advantages of screening with this model over the AQ-10. The data used for the developed model 
uses a more stringent cutoff score of seven or more on the AQ-10 for a positive Autism flag 
where the AQ-10 uses six or more. Secondly, the SVC model uses only six of the more 
dichotomous questions of the AQ-10. All the questions on interpreting other people’s intentions 
during interactions were eliminated, reducing the chance of respondent misinterpretation. 
Everyone may occasionally have trouble identifying the intentions of manipulative people. The 
SVC model presented in this paper demonstrates a positive Autism classification precision of 
0.97 (overall odds = 0.36) on a test set with less ambiguous questions than the AQ-10. The 
model is a practical and accurate screening for Autism in adults. The technical analysis is 
presented as an appendix to this report. 
A secondary goal was to select a few predictive and transparent features that practitioners 
may use as a segue to a conversation on autism screening. This is where the more transparent XG 
Boost model was immensely helpful. Since XG boost is a decision tree ensemble model, the 
most important features contributing to the prediction are available for analysis. The model 
trained for this project revealed that two questions from the AQ-10, three and six, were the most 
important, which shows that difficulty with multi-tasking and reading faces are two important 
behavioral characteristics of people with ASD. Even without screening or a diagnosis, 
recognizing such traits is important for empathy and support from the neurotypical population.
## Model Inputs
The final inputs for modeling include six questions from the AQ-10 and five non
behavioral attributes as follows: 

• Q1 - I often notice small sounds when others do not. (Yes = 1) 

• Q2 - I usually concentrate more on the whole picture, rather than the small details.       
(No = 1) 

• Q3 - I find it easy to do more than one thing at once. (No = 1) 

• Q4 - If there is an interruption, I can switch back to what I was doing very quickly.      
(No = 1) 

• Q6 - I know how to tell if someone listening to me is getting bored. (No = 1) 

• Q9 - I find it easy to work out what someone is thinking or feeling just by looking at their 
face. (No = 1) 

• Age in years. 

• Patient relationship with who is completing the test. (Self or others). 

• Family member with ASD. (Yes or no) 

• Ethnicity of subject. (White, Asian, Middle Eastern, Black, other)   
  
• Country of residence. (United States, New Zealand, Jordan, United Arab Emirates, 
United Kingdom, Australia, India, other)   

## Model Test Results
Using 20% of the data as a test set, the SVC model predicted the correct test set targets with an overall accuracy of 96%.
The positive ASD classification precision is 97% and only one false positive out of 104 
true negatives was predicted with a recall of 99%. 
