# Parkinsons_Disease_Analysis
~Author : Pratham Sanshi
## Introduction
<p>
  Parkinson's disease (PD) is a complex and progressive neurological disorder that affects millions of people worldwide, 
  causing significant challenges to their quality of life. Characterized by a range of motor and non-motor symptoms, PD primarily 
  stems from the degeneration of dopaminergic neurons in the substantia nigra region of the brain. Early diagnosis and effective management 
  of Parkinson's disease are 
  crucial for optimizing patient outcomes and improving their overall well-being.
</p>
<p>
  In recent years, the field of data science has emerged as a powerful tool in the study and management of Parkinson's disease. 
  Leveraging advanced data analytics techniques, machine learning algorithms, and the availability of extensive patient data, data 
  scientists are playing a pivotal role in enhancing our understanding of PD, enabling earlier detection, 
  and developing more personalized treatment strategies.
</p>
<hr>

## Project Details
<p>
  In this project, I undertook the task of predicting Parkinson's disease utilizing data science techniques.
  This project involved the utilization of various algorithms for the analysis in <b>jupyter notebook</b> and <b>sklearn packages</b> for building model and calculating resultant matrix. 
</p>
<p>
  The parkinsons's dataset has 24 freatures and 195 rows which makes it a small sized and imbalanced dataset.The output is either true/positive or false/negative , which makes it binary classification problem.
</p>

### Is accuracy is right performancd metrics for choosing a best algorithm?
<p>
  The answer is definately NO!!!....I will explain you why this is not true in next few sentences.
  Choosing a right metics is very important for machine learing algorithms, because if we choose a bad merics then at the time of deployment 
  we may not get desired results and may encounter sharp anomalies.
  Before computing the accuracy, we need to understand what each term in confusion matrix has to say 
  about a given datset.
  <ul>
<li>True Positive (TP): The patient is diseased and the model predicts "positive"</li>
<li>False Positive (FP): The patient is healthy but the model predicts "positive"</li>
<li>True Negative (TN): The patient is healthy and the model predicts "negative"</li>
<li>False Negative (FN): The patient is diseased and the model predicts "negative"</li>
</ul>

Acurracy= ( TP + TN ) / ( TP + FP + TN + FN )
Here accuracy talks about how many times the model has correctly classified a patient given in our dataset with respective to the total number of patients.Also we have an imbalanced dataset (positive patients = 75 % and negative patients = 25%). Hence if we were to use accuracy out model will be biased to the dominating outcome , in this case it is positive, hence it is very delicate to use accuracy as a primary   metrics.

  
</p>



