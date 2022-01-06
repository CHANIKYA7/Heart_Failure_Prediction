# Heart_Failure_Prediction
Analysis the data and model creation of Heart failure Dataset
## Objectives :
 * Checking the Null values.
 * Identifying the Outliers.
 * Cleaning the Dataset.
 * Exploratory Data Analysis.
 * Data Visualization for better understanding.
 * Feature Engineering.
 * Stanadrad scaling.
 * Building model and Evaluation.
 * Comparison of all models.
 * Collecting Domain Knowledge.
  
## Data Format : CSV

## Languages Used : Python

## IDE's : Jupyter
## Modules
* Numpy
* Pandas
* Matplotlib.pyplot
* Seaborn
* Standard_Scaler (for scaling the data) from Sklearn
* train_test_split(for splitting the data train and test) from sklearn
* Model Creation & Fitting the Modules
* Accuracy,f1_score,recall_score,precision_score,confusion_matrix

## Description of Dataset:

You already know the world is facing with such a risk pace and so do the diseases, and to cure the diseases, doctors have to devote their precious time and experience that they had. But what is more concerning is the increasing number of patients than ever before, which results in more doctors and manual work. Instead of doing that, wouldn't it be awesome if we have a model which can predict whether a patient is going to have or has a particular disease or not ? That’s what we are talking about here.
	 The aim of this model is to predict whether a patient is going to have a heart failure or not based on certain input features. After that, we’re going to evaluate and find out how well our model is working.
	The dataset includes different parameters which are helpful to cut down the chase and helps us to know the target variable. These are the following parameters included:
        Dataset has been procured from kaggle, dataset consists of 13 attributes and 1 target variable. Dataset has 5 continous and 8 discrete values. Further description about the dataset is in the Description.txt file

* 'age': 			Continuous variable
* 'anaemia': 			Categorical variable
* 'creatinine_phosphokinase': 	Continuous variable
* 'diabetes': 			Categorical variable
* 'ejection_fraction': 		Continuous variable
* 'high_blood_pressure': 	Categorical variable
* 'platelets': 			Continuous variable
* 'serum_creatinine': 		Continuous variable
* 'serum_sodium': 		Continuous variable
* 'sex': 			Categorical variable
* 'smoking': 			Categorical variable
* 'time': 			Continuous variable
* 'DEATH_EVENT': 		Categorical variable
### Importing the Dataset
By Using  the Pandas  we import the dataset
### Statistical Descripton of dataset
.head() - prints top 5 rows of dataset, 
.tail() - prints last 5 rows of dataset,
.shape() - prints (number of rows, number of columns),
.info() - prints the datatypes of columns and memory usage,
.columns() - prints the column names of a dataset,
.describe(include ="all") - quartile values like 25,50,75% mean,standard deviation,count, min and max values
## EDA

### Checking the Null values
.isnull() - which prints the whether the value null or not. if the value is Null then it prints True otherwise False
.isnull().sum() - which gives the count of null values column wise
(.isnull().sum()/.shape[0])*100 - which gives the percentage of Null values

The Dataset have "NO" Null values.

### Checking the Duplicated values
.duplicated.sum() - gives the no.of duplicated values present in a dataset

The Dataset have "NO" duplicated values
### Checking the Outliers
Outliers increase the variability in your data, which decreases statistical power.
![image](https://user-images.githubusercontent.com/88540739/148004322-4f8f637d-04b9-40aa-b1e4-4c7250af52df.png)

It's not possible to see outliers like null values and duplicated values. So, we plot the Boxplot using Seaborn/Matplotlib.pyplot from the chart or graph we can easily see whether they are really a outliers or not. Sometimes we consider the outliers because in the theoretical  view it's not possible in the practical view it was consider.
In these dataset also have some outliers but we consider that,they are not really outliers. So, we didn't interrputed.
### Visualization
By using the seaborn we ploted the countplot of sex column, which gives the count of no.of male and no.of female present in a dataset.
![download](https://user-images.githubusercontent.com/88540739/148005359-b2bd7a07-7e86-4576-a20e-54b1e4ef09a6.png)

By using the seaborn we ploted the countplot of Death_Event column, which gives the count of no.of male are died and no.of female are died in a dataset.
![download](https://user-images.githubusercontent.com/88540739/148005560-ea3ed508-3995-4e1f-9384-254af06ab8d3.png)

hf["DEATH_EVENT"].value_counts() which gives count of values 
0    203
1     96
Name: DEATH_EVENT, dtype: int64

Ploted the Distplot of age column, from this in the age of 55 to 63 are registerd more heart_failure cases.
![download](https://user-images.githubusercontent.com/88540739/148006029-972f7dfd-67eb-40e8-b8dc-6a3912003e4e.png)

In the dataset age and Death_event coulumn will not given clearly, so we 1 is assigned for Male and 0 is assigned for Female. After that we ploted the Pie chart 







