# Car Price Prediction
~Author :- Pratham Sanshi 🤗
## Introduction 
<p>
  Predicting car prices is a crucial task in the automotive industry, helping buyers and sellers make informed decisions in a rapidly changing market. Whether you're a car enthusiast, a dealership owner, or a data science enthusiast, this project aims to provide you with the tools and insights to predict car prices accurately.
</p>
<p>
  In this repository, I present a comprehensive car price prediction solution that leverages machine learning techniques to estimate the fair market value of a wide range of vehicles. This project is designed to be user-friendly and adaptable, making it suitable for both beginners looking to explore the world of data science and experienced professionals seeking a robust car pricing model.
</p>
<p>
  Feel free to explore the code, datasets, and documentation in this repository to gain a better understanding of how car price prediction can be achieved using machine learning.
</p>
<hr>

## Data Set Details:
<ol>
  <li>Data Format: The following data set is in .csv format. </li>
  <li>Number of Records : 10,670 records.</li>
  <li>Features/Columns : There are 9 columns. They are model, year, transmission, mileage, fueltype, tax, mpg, enginesize and price</li>
  <li>Data Cleaning The process involves usage of sklearn package and graph is plotted  utilizing matplotlib and seaborn. 
  <ul>
    <li>model -> Label encoding</li>
    <li>Fueltype ->  Label encoding</li>
    <li>transmission -> OneHotencoding</li>
    <li>input features -> Standardization</li>
  </ul>
    
  </li>
</ol>
<hr>

## Preprocessing details:
<ol>
  <li>Label Encoding : Label encoding is a technique used in machine learning and data preprocessing to convert categorical data into numerical format. It assigns a unique numerical label to each distinct category, transforming the categorical data into numerical representation.</li>
  <li>OneHotEncoding : One-hot encoding is a technique used in machine learning and data preprocessing to convert categorical data into a binary (0 or 1) format, making it suitable for machine learning algorithms.The original categorical column is replaced with  binary columns. So, instead of having a single column with string values, you now have multiple binary columns representing each category.Unlike label encoding, one-hot encoding does not introduce any artificial order among categories.</li>
  <li>Standardization : Standardization helps bring all features to a common scale, making it easier for machine learning algorithms to work effectively, especially when the features have different scales or units.
    <p>
   $Standardization(z) =  \frac{Original_Value(x)-Mean of feature} { Standard Deviation of the feature}$
      </p>
    </li>
</ol>

## Results
### Multiple Linear Regression
|Algorithm  | Accuracy |
| ------------- | ------------- |
| Multiple Linear Regression |  0.7915 |
|  Multiple Linear Regression + Cross Validation  |0.7582  |
|  Multiple Linear Regression + mean of Loout cv|0.7583  |
|  Multiple Linear Regression + PCA| 0.7916 |
|  Multiple Linear Regression +LDA|0.7915 |


### Polynomial Regression
|Algorithm  | Accuracy |
| ------------- | ------------- |
| Polynomial Regression | 0.9167 |
|  Polynomial Regression + Cross Validation  |0.8961  |
| Polynomial Regression + mean of Loout cv|0.7632 |


### Decision tree regressor

|Algorithm  | Accuracy |
| ------------- | ------------- |
| Decision tree regressor |  0.9122 |
|  Decision tree regressor + Cross Validation  |0.9143  |
|  Decision tree regressor + mean of Loout cv|0.9179  |
|  Decision tree regressor + PCA| 0.9218 |
|  Decision tree regressor + Cross Validation + PCA  |0.9195  |
|  Decision tree regressor + mean of Loout cv +  PCA|0.9139  |
| Decision tree regressor +LDA|0.8945 |
|  Decision tree regressor + Cross Validation + LDA  |0.9427  |
|  Decision tree regressor + mean of Loout cv +  LDA|0.9450  |


### Random Forest
|Algorithm  | Accuracy |
| ------------- | ------------- |
| Random Forest |  0.9601 |
| Random Forest + Cross Validation  |0.9358  |
|  Random Forest + mean of Loout cv|0.9471  |
|  Random Forest + PCA|0.9471 |
|  Random Forest +LDA|0.9581|

### KNN
|Algorithm  | Accuracy |
| ------------- | ------------- |
| KNN |  0.9496 |
| KNN + Cross Validation  |0.9157 |
|  KNN+ mean of Loout cv|0.9220  |
|  Random Forest + PCA| 0.9495 |
|  Random Forest +LDA|0.9496|




