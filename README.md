# Automated-AWS-Cloud-ETL-Solution-for-Music-Streaming-Data
Seamlessly extract, transform, and load Spotify streaming data with a fully automated ETL pipeline, leveraging AWS cloud services for scalable, efficient data processing and analytics readiness.

## Purpose

This ETL pipeline embodies a practical fusion of academic learning and self-directed exploration within the realm of data engineering. It is the culmination of rigorous study in my master’s program, enriched by the tangible experiences from my internships. The project is an active representation of theory applied to a tangible challenge: constructing a comprehensive music database from Spotify's diverse dataset.

In harnessing Spotify's API to extract, transform, and load data, this pipeline crystallizes the abstract concepts of data management into a tangible workflow. It is a deliberate application, a bridge from the conceptual to the concrete, enabling hands-on experience with complex data processes. This initiative is instrumental in cementing my grasp of sophisticated data processing, analytics, and efficient data storage strategies. It's here that my theoretical knowledge and practical skills coalesce, preparing me to tackle the intricate demands of today's data-driven landscape.

## Architecture

![1707949477705](https://github.com/kohliamitoj/Automated-AWS-Cloud-ETL-Solution-for-Music-Streaming-Data/assets/134894076/29ba9b65-fe98-408b-b55f-42856e3a3b0d)

The ETL pipeline is structured as follows:
- **Extract**: Data is extracted from the Spotify API using a Python AWS Lambda function.
- **Transform**: The raw data is transformed using another Lambda function that processes and structures the data.
- **Load**: The transformed data is then loaded into Amazon S3 buckets. From there, it's cataloged using AWS Glue and made available for querying and analysis with Amazon Athena.

## Components
- `spotify_api_data_extract_lambda_function.py`: The Lambda function for extracting data from the Spotify API.
- `spotify_transformation_load_lambda_function.py`: The Lambda function for transforming the extracted data and loading it into S3.
- `Spotify_ETL_Pipeline_Project.ipynb`: A Jupyter notebook that outlines the entire ETL process and can be used for testing and documentation purposes.

## List of Technologies
- AWS Lambda: For the serverless execution of data extraction and transformation routines.
- AWS S3: As the cornerstone for raw and processed data storage.
- AWS Glue: To catalog data assets and automate schema recognition.
- AWS Athena: Enabling SQL-powered analytics on S3-based datasets.
- Python: The scripting lingua franca for data wrangling and interactions with the Spotify API.

## Project Highlights
- Engineered an end-to-end ETL pipeline using AWS services (Lambda, S3, Glue, Athena) and Python for Spotify's music streaming data extraction, transformation, and analysis.
- Automated daily data extraction from the Spotify API using Python, securely managing API credentials and ensuring reliable data capture. Processed raw JSON data with Python, employing Pandas for data transformation tasks such as parsing, deduplication, and timestamp conversion to prepare for analytics.
- Deployed AWS Lambda functions for serverless execution of ETL tasks, significantly reducing infrastructure costs and scalability concerns.
- Managed structured storage of transformed data on AWS S3, creating an efficient and organized system for easy data access and retrieval.
- Integrated AWS Glue to catalog data assets and automate schema recognition, streamlining the management and accessibility of data schemas for analysis.
- Configured CloudWatch events to trigger data processing, ensuring the timely availability of data for reporting and analysis.
- Implemented best practices for in-memory data handling and I/O optimization, resulting in a high-performance data processing environment.
- Facilitated downstream analytics by organizing transformed data into composite CSV files, streamlining data access for business intelligence tools.
- Enabled advanced analytics and ad-hoc querying capabilities by organizing data into structured CSV files for business intelligence tools and using AWS Athena for efficient data exploration.
