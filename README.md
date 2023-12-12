# S3_GLUE_ETL

This is an end to end ETL pipeline where data is populated in S3 and then AWS crawler is used to access this data. The crawler reads data from S3 path and creates AWS Glue database and AWS glue table. Since the data has been extracted , it is then ready for set of tarnsformations which are made on it.

An ETL Job is created to execute the entire ETL process and it's triggered through code. Finally, once the data has been tarnsformed, it's dumped back to S3 wherein it's used as a data lake.

# STEPS

1. Create S3 bucket and upload data into the S3 bucket using python.

2. AWS Glue cralwer is created and along with that AWS Glue Database and Table is also created.
   
3. The crawler extarcts the data from S3 path and populates the Glue table.
   
4. AWS Glue is now used to perform Transformations on the data and updated data is finally stored in S3.
   
5. Finally the etl job is triggered to perform etl.


EXTRACT => Crawler (Data catalog DB and Data catalog table)

TRANSFORM => AWS Glue ( Python script is used)

LOAD => S3 ( Transformed data is loaded back to output folder in concerned S3 bucket)
