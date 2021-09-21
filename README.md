# Hospital data analysis using HDFS and Spark

## Project Description
For this Big-data project, We took the Hospital data from Kaggle website, and converted that data into CSV file. 
The dataset contains 14 columns and 137K rows approximately. Then using Ambari We imported the CSV file data into HDFS. 
After that we created one dataframe in spark and with the help of that dataframe we loaded our csv file into spark. 
Then we performed some dataframes methods on it and also create one temporary view for the spark-sql queries. We also stored our output queries into a file in HDFS directory. 
Then we performed partitioning and bucketing in spark, whose partition files are created in HDFS directory.

## Technologies Used
* HDFS - v2.7
* Spark - v2.3
* Hive - v1.2

## Features
* Created Spark_Dataframe and implemented Spark_Dataframes methods.
* Created temporary Table in Spark and applied some Spark_SQL queries on it.
* Did partitioning and bucketing with the help of Spark_SQL.
* Connected Hive To Spark. 

## Getting Started
importing some packages
```
>>> import pyspark                                                                                                                                   
>>> from pyspark.sql import sparksession 
```

Creating Dataframe in spark
```
>>> df2 = spark.read.csv('/project2/test_data.csv',inferSchema=True,header=False).toDF("id","Hcode","HCcode","A_Room","Dep","Wcode","Bed_Grade","pid"
,"PCcode","Admission","Illness","Visit_P","P_age","Deposit") 
```
Creting Temporary Table in Spark
```
>>> df3=df2.createOrReplaceTempView("Health_Care")
```
## Contributors
* Anosh Shaju
* Omkar Gaikwad
* David Stephen Raj
* Ashish Fulwade
* Akshay Paurush Singh Bhadauria

## References
* https://sparkbyexamples.com/spark/different-ways-to-create-a-spark-dataframe/
* https://sparkbyexamples.com/spark/spark-sqlcontext-explained-with-examples/
* https://spark.apache.org/docs/latest/sql-programming-guide.html
* https://spark.apache.org/docs/latest/sql-data-sources-hive-tables.html
 
