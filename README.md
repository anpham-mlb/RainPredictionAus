## Purpose
Using PySpark, MongoDB and apply machine learning algorithms such as ​DecisionTreeClassifier(), RandomForestClassifier(), and LogisticRegression(), GBTClassifier() methods in spark to calculate the probability of the rain fall tomorrow based on the other related data points (e.g., temperature, wind, humidity).
## Details
### Step 1: Import Spark Session and initialize Spark
Create a SparkConf object that contains information about your application by SparkContext.
### Step 2: Load the dataset and print the schema and total number of entries
Load data as CSV format in sparkSession.
### Step 3: Delete columns from the dataset
Delete unnecessary data from the dataset to improve the efficiency and accuracy of the model.
### Step 4: Print the number of missing data in each column
### Step 5: Fill the missing data with average value and maximum occurrence value
Fill in all the missing data with average value (for numeric column) or maximum frequency value (for non-numeric column).
Firstly, identify the columns which have numeric values (e.g., MinTemp, MaxTemp), calculate the average and fill the null value with the average.
Secondly, identify the columns with non-numeric values (e.g., WindGustDir, WindDir9am) and find the ​most ​frequent item (e.g., wind direction). Now fill the null values with that item for that particular column.
### Step 6: Data transformation
Transform the data so that it will be useful to process by the machine learning algorithm. Before transforming your non-numerical data, do the type casting (to double) of the numerical value columns as they are defined as “String” (see, the schema of the dataset). For the non-numerical value column (i.e., WindGustDir, WindDir9am, WindDir3pm, RainTomorrow) use the StringIndexer method to convert them into numbers.
### Step 7: Create the feature vector and divide the dataset
Create the feature vector from the given columns. Spit the dataset randomly and between 70 percent and 30 percent.
### Step 8: Apply machine learning classification algorithms on the dataset and compare their accuracy. Plot the accuracy as bar graph.
Use DecisionTreeClassifier(), RandomForestClassifier(), and LogisticRegression(), GBTClassifier() methods in spark to calculate the probability of the rain fall tomorrow based on the other related data points (e.g., temperature, wind, humidity). Draw a graph to demonstrate the comparison of their accuracy.
### Step 9: Calculate the confusion matrix and find the precision, recall, and F1 score of each classification algorithm
Finding the accuracy of the model does not always represent the quality of the model for a given dataset.




