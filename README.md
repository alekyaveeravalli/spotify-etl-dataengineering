# spotify-etl-dataengineering

Hi everyone, I am excited to share my AWS data engineering project.

Spotify Data Pipeline Project Using Python

AWS Services Used : S3, Lambda, Glue, Cloudwatch, Athena.

Data Extraction: 
AWS Lambda: Extracted data  from Spotify API using a Python script running on an AWS Lambda(spotify_api_data_extract)
Amazon S3: uploaded data to an S3 bucket(spotify-etl-project-alekya)under the raw layer(spotify_raw_data/to_processed/)
Amazon CloudWatch: On an hourly basis, triggered the lambda function using Amazon CloudWatch.

Transformation:
AWS Lambda: Created another lambda function(spotify_api_data_transform) for the transformations and loaded them to album, artists and songs folder.

Data Load:
AWS Glue Crawler: Created Glue Crawler to infer schemas whenever there is new data in S3 Bucket.
Amazon Athena: Used to query and analyze the spotify  dataset.
