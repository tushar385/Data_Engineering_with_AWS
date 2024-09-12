# Data_Engineering_with_AWS

--aws configure

-- LIST BUCKET
--aws s3 ls

--CREATE BUCKET
--aws s3 mb s3://sfn-pique	

--DELETE BUCKET
--aws s3 rb s3://sfn-pique	

-- LIST OF Bucket
--aws s3 ls s3://sfn-polaris/snowflake_raw_dump_2023_06_06/test/
--aws s3 cp s3://sfn-polaris/snowflake_raw_dump_2023_06_06/test1/data ./data2 --profile mesa

--TO COPY DATA FROM LOCAL TO S3
--aws s3 cp /home/ubuntu/Desktop/domain_count_per_org.csv s3://sfn-dialpad/ticket_2023_07_18/domain_count_per_org --acl private --sse --metadata-directive  REPLACE --content-type "text/csv" --content-disposition "attachment; filename=<s3_filename>"

--TO COPY DATA FROM S3 TO LOCAL
--aws s3 cp s3://sfn-polaris/snowflake_raw_dump_2023_06_06/test/abc.csv /home/ubuntu/Desktop/abc.csv

--TO move DATA FROM LOCAL TO S3
--aws s3 MV /home/ubuntu/Desktop/domain_count_per_org.csv s3://sfn-dialpad/ticket_2023_07_18/domain_count_per_org 

--To delete data
--aws s3 rm s3://sfn-dialpad/ticket_2023_07_18/abc.txt
--aws s3 rm s3://sfn-dialpad/ticket_2023_07_18 --recursive

--to copy data from 1 aws to another
--aws s3 sync s3://sfn-mesa-specific/mesa_snowflake/data_2020_thru_mar_2022/ s3://sfn-mesa/raw_snowflake_sfdc_tables/ --profile old_aws-acc
