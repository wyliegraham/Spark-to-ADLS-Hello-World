# Spark-to-ADLS-Hello-World

some really simple code to validate that you can read a .csv from Azure Data Lake Store g2 from Synapse or Databricks

#set the data lake file location:

file_location = "abfss://"container name"@"storage account name".dfs.core.windows.net/"filename""

#read in the data to dataframe df

df = spark.read.format("csv").option("inferSchema", "true").option("header", "true").option("delimiter",",").load(file_location)

#display the dataframe

display(df)
