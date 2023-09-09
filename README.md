# Parkinsons_Disease_Analysis
~Author : Pratham Sanshi
## 1.Introduction
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

## 2.Project Details
<p>
  In this project, I undertook the task of predicting Parkinson's disease utilizing data science techniques.
  This project involved the utilization of various algorithms for the analysis in <b>jupyter notebook</b> and <b>sklearn packages</b> for building model and calculating resultant matrix. 
</p>
<p>
  The parkinsons's dataset has 24 freatures and 195 rows which makes it a small sized and imbalanced dataset.The output is either true/positive or false/negative , which makes it binary classification problem.
</p>

### 2.1 Is accuracy is right performance metrics for choosing a best algorithm?
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
  
### 2.2 Precision or Recall? Which is good metrics? 
  <p>
    The gole in parkinson's disease identification is to reduce a false negative(FN) value and ideally it should be zero. The algorithm cannot afford to say that a patient 
    is healthy despit having actual disease. But it can afford a very slight errors in saying that a person has tested positive despite not having a disease. Hence we have 
    to increase the value of recall which can be done by reducing false negative.
  </p>
  <p>
    Now that we know that we have to reduce false negative in our case hence we used one more term called Fbeta.
  </p>
  
 <p>
   $F_{Beta}=$
     $\frac{( 1 + beta )*( Precision  *  Recall ) }{ beta^2 * Precision + Recall }$
   <p>
If false positive and false negative are both important then we select beta value to one.
  if Beta=1 then this is called $F_1$ score. </p>
<p>In our senario the false negative is very important that means we have to select beta value to be 2
   if Beta=2 then it is called $F_2$ score.
   Then,</p>
   <p>
   $F_2 =\frac{2*( Precision  *  Recall ) }{ 4 * Precision + Recall }$ (here $F_2$ is harmonic mean of precision and recall)
     </p>
     <p>Therefore, we conclude that the best performance matrics is $F_2$ score that will account precision and recall therby reducing false negative.</p>
<hr>

  ## 3.Algorithms Used:
  <ol>
<li>Logestic Regression</li>
<li>Logestic Regression + Stratified Cross Validation</li>
<li>Logestic Regression + PCA</li>
<li>Logestic Regression + LDA</li>
<li>Support Vector Machine + rbf(kernel)</li>
<li>Support Vector Machine + poly(kernel with degree=5)</li>
<li>Support Vector Machine + rbf(kernel)</li>
<li>Support Vector Machine + poly(kernel) + Stratified Cross Validation</li>
<li>Support Vector Machine + poly(kernel) + PCA</li>
<li>Support Vector Machine + poly(kernel) + LDA</li>
<li>Decision Tree +gini(kernel)</li>
<li>Decision Tree +entropy(kernel)</li>
<li>Decision Tree +entropy(kernel) + Stratified Cross Validation</li>
<li>Decision Tree +entropy(kernel) + Adaboost</li>
<li>Decision Tree +entropy(kernel) + PCA</li>
<li>Decision Tree +entropy(kernel) + LDA</li>
<li>Random Forest</li>
<li>Random Forest + Adaboost</li>
<li>Random Forest + Stratified Cross Validation</li>
<li>Random Forest + PCA</li>
<li>Random Forest + LDA</li>
<li>KNN</li>
<li>KNN + Stratified Cross Validation</li>
<li>KNN + PCA</li>
<li>KNN + LDA</li>
<li>NB</li>
<li>NB + Adaboost</li>
<li>NB + Stratified Cross Validation</li>
  </ol>
  <hr>
  
## 4.Keywords
<ol>
  <li>
    Stratified cross-validation: Stratified cross-validation is a variation of k-fold cross-validation, a common technique used in machine learning to assess the performance of a predictive model. Stratified cross-validation is particularly useful when dealing with classification problems where the distribution of classes in the dataset is imbalanced.
</li>
  
  <li>
    Kernels: Kernels are a powerful tool in machine learning because they enable the modeling of complex relationships in data without explicitly defining the transformation to a high-dimensional space. They are particularly useful when dealing with non-linear and complex decision boundaries. The choice of the appropriate kernel function depends on the problem and the characteristics of the data you're working with.In our case i have used multiple kernels to probe how results vary.
  </li>
  
  <li>
    Adaboost: AdaBoost is particularly effective when dealing with complex datasets and when weak learners are carefully chosen and combined. It's known for its ability to focus on the data points that are difficult to classify, gradually improving the overall model's performance. 
  </li>
  
  <li>
    PCA: PCA is primarily used for unsupervised dimensionality reduction. Its main goal is to reduce the number of features (dimensions) in a dataset while retaining as much of the original variance as possible.I have used this to show how result affects when used with supervised learing setup.
  </li>
  
  <li>
    LDA: LDA is primarily used for supervised dimensionality reduction and classification. Its goal is to find linear combinations of features that maximize the separation between different classes or groups in the data.
  </li>
  
</ol>

<hr>

## 5.Conclusion

    





  


  




