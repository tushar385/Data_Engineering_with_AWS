# Data_Engineering_with_AWS

## Configure Aws account
aws configure

## LIST BUCKET
aws s3 ls

## CREATE BUCKET
aws s3 mb s3://pique	

## DELETE BUCKET
aws s3 rb s3://piquee	

## LIST OF Bucket
aws s3 ls s3://pique/snowflake_raw_dump_2023_06_06/test/
aws s3 cp s3://piques/snowflake_raw_dump_2023_06_06/test1/data ./data2 --profile mesa

## TO COPY DATA FROM LOCAL TO S3
aws s3 cp /home/ubuntu/Desktop/domain_count_per_org.csv s3://pique/ticket_2023_07_18/domain_count_per_org --acl private --sse --metadata-directive  REPLACE --content-type "text/csv" --content-disposition "attachment; filename=<s3_filename>"

## TO COPY DATA FROM S3 TO LOCAL
aws s3 cp s3://pique/snowflake_raw_dump_2023_06_06/test/abc.csv /home/ubuntu/Desktop/abc.csv

## TO move DATA FROM LOCAL TO S3
aws s3 MV /home/ubuntu/Desktop/domain_count_per_org.csv s3://pique/ticket_2023_07_18/domain_count_per_org 

## To delete data
aws s3 rm s3://pique/ticket_2023_07_18/abc.txt
aws s3 rm s3://pique/ticket_2023_07_18 --recursive

## To copy data from 1 aws to another
aws s3 sync s3://pique/mesa_snowflake/data_2020_thru_mar_2022/ s3://pique/raw_snowflake_sfdc_tables/ --profile old_aws-acc

## TO move DATA FROM LOCAL TO S3
aws s3 MV /home/ubuntu/Desktop/domain_count_per_org.csv s3://pique/ticket_2023_07_18/domain_count_per_org 

## To delete data
aws s3 rm s3://pique/ticket_2023_07_18/abc.txt
aws s3 rm s3://pique/ticket_2023_07_18 --recursive

## To copy data from 1 aws to another
aws s3 sync s3://pique/mesa_snowflake/data_2020_thru_mar_2022/ s3://pique/raw_snowflake_sfdc_tables/ --profile old_aws-acc

## To configure aws by nano
nano ~/.aws/credentials  
  [default]  
  aws_access_key_id = YOUR_ACCESS_KEY_ID  
  aws_secret_access_key = YOUR_SECRET_ACCESS_KEY

nano ~/.aws/config
  [default]
  region = us-east-1
  output = json

aws sts get-caller-identity
