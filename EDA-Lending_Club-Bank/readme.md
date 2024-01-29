# Exploratory Data Analysis- Steps
<p>
EDA uses data  visulisation techniques to draw inferences and obtain insights from the data. However, EDA is much more than plotting graphs or visualising data , it is about understanding and studying the given data in detail and take informed decisions.
  Eda also involves the preparation of data sets for analysis by removing irregularities in data.
  
</p>

## Utility of EDA:
<ol>
  <li>Maximise insights into dataset </li>
  <li>Detect outliers and anomalies.</li>
  <li>Test underlying assumptions (eg:sales increases with discounts) </li>
</ol>

### 1.Data Cleaning
<ul>
  <li><b>Identifying the data type</b></li>
  <ol>
    <li>Change the data type of specific column by removing characters</li>
    <li>split or merge the columns by mathematical operations</li>
  </ol>
  <li><b>Fixing the rows and cloumns</b></li>
  <ol>
    <li>Add column name if missing</li>
    <li>Rename column consistently</li>
    <li>Delete unnecessary column </li>
    <li>Split columns for more data</li>
    <li>Merge columns for identifiers</li>
    <li>align misaligned columns</li>
  </ol>
  <li><b>Imputing removing missing values</b></li>
  <ol>
  <li>set values as missing values (eg treat with 'XX' or NULL</li>
  <li>Fill missing values with function value , constant or central tendency</li>
  <li>Remove missing values by deleting rows or columns depending on volume of missing data</li>
  <li>imputing done using logistic regression or ML techniques</li>
  </ol>
  <li><b>Handling outliers</b></li>
  <ol>
    <li>imputation of outliers</li>
    <li>delete outliers</li>
    <li>binning the values</li>
    <li>cap the outliers</li>
  </ol>
  <li><b>Standardising the values</b></li>
    <ol>
     <li>Transform the data in consistent form by scaling or truncating</li>
     <li>Convert all column into single unit format </li>
      <li>Standardise precision</li>
      <li>Standardise case</li>
    </ol>
  
  <li><b>Fixing invalid values</b></li>
  <ol>
    <li>Convert string to num or vice-versa according to dataset</li>
    <li>Amend the values that are beyond logical range</li>
    <li>Validate general or logical rules(eg: phone num should have 10 digits )</li>
  </ol>
  
  <li><b>Filtering the data</b></li>
  <ol>
    <li>Removing the columns that are not necessary in analysis(eg: id)</li>
    <li>Delete duplicate values and aggregate data</li>
    <li>Selecting columns that has potential information in deciding the output</li>
    
  </ol>
</ul>

##### NOTE:
##### 1.The above given steps are carried out in any order and may or may not apply to all datasets.
##### 2.Types of missing values:
<ol>
  <li>MCAR : (Missing Completely At Random)Does not depend on any feature column </li>
  <li>MAR: (Missing At Random) There could be some depending factor</li>
  <li>MNAR:(Missing Not At Random) Missing for very specific reason</li>
</ol>

### 2.Univariate Analysis:
<p>Univariate analysis involves Analysing / Visualising a single variable by handling missing/outliers. </p>
Types of Univariate Analysis:-
<ol>
   
  <li><b>Categorical unordered univariate analysis</b>: 
  This analysis does not have any meadurable terms , such as high-low , more-less or fail-pass etc. Eg: The type ob loan taken by individual (home loan or personal loan or business loan)
  <li><b>Categorical ordered univariate analysis : </b> The variables that follow a natural rank of order. Eg: Age group(<50,>50) , month, education(primary or secondary)</li>
  <li><b>Statistics or Numeric Features</b>: Continuous or discrete values like height ,temperature ,age or weight.</li>
</ol>

### 3.Bivariate Analysis
<p>Here analysis is carried out by observing two variables.</p>
Types of bivariate analysis
<ol>
  <li>Analysis between numeric and categorical variables </li>
  <li>Analysis between two categorical variables</li>
  <li>Analysis between two numeric vairables</li>
</ol>

### 4.Multivariate Analysis:
<p>It involves gathering more then two variables and drawing conclusions.It makes use of pivot tables or correlation matrix</p>
