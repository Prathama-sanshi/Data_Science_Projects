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
  The answer is definately NO!!!....I will give you a concrete resons why this is not true in next few points.
  Choosing a right metics is very important for machine learing algorithms, because if we choose a bad merics then at the time of deployment 
  we may not get desired results and may encounter sharp anomalies.
   Before computing the accuracy, we need to understand what each term in confusion matrix has to say 
  about a given datset.
</p>
   <ul>
  <li>True Positive (TP): The patient is diseased and the model predicts "positive"</li>
  <li>False Positive (FP): The patient is healthy but the model predicts "positive"</li>
  <li>True Negative (TN): The patient is healthy and the model predicts "negative"</li>
  <li>False Negative (FN): The patient is diseased and the model predicts "negative"</li>
  </ul>

  <ol> 
    <p>Here accuracy talks about how many times the model has correctly classified a patient given in our dataset with 
    respective to the total number of patients.
      </p>
Accuracy= ( TP + TN ) / ( TP + FP + TN + FN )
<p>
  The given dataset is imbalanced having almost 75% of positive and remaining being negative.
    Hence if we were to use accuracy as a metrics, our model will be biased to the most frequent outcome, in this case it is positive, 
    therefore it is very delicate to use accuracy as a primary  metrics.</p>
      <p>
        We will take an example of our dataset which is an example of imbalaced data set. It has 147 positive class(75%) and 48 negative classes(25%). The total data points being 147+48 =195.
        Lets just say that a given algorithm predicts almost 75%(147 patients) of positive class as positive and predicted all negative class incorrectly, then 
        we would have an accuracy= (147+0)/195  with is again 75%. It is very inappropriate to say that an algorithm is 75 percent accurate despit predicting all negative class incorrectly.All in all we have to find a better metrics which brings us to precision and recall.
      </p>
    <ol>
  
  <li>Precision= TP / ( TP + FP )
  <p>
    Out of the total actual positive predicted results how many were actually positive.It is also called as positive prediction value.  
  </p>
</li> 
 
   <li>Recall= TP / ( TP + FN )
  <p>
   Out of total actual positive values how many positive values did the model predict correctly.This is also known as true positive rate(TPR) / sensitivity.</li>  </p>
  </ol>
 


    





  


  




