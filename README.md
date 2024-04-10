# Linkedin Data Engineer Job Postings

Hi there! This is my project for the Data Engineering Zoomcamp 2024 course.

## Problem Description

This dataset provides valuable insights into data engineering job postings, including the required skills and software proficiency sought by employers. The goal of this project is to create a streamlined and efficient process for finding the most in-demand data science skills in the cloud by implementing data engineering concepts.


## About the dataset

A dataset containing data engineering job postings collected from LinkedIn. Includes job titles, company names, job locations, job links, dates of first sighting, search city and country, job levels, job types, job summaries, and required job skills.

The data can downloaded from [kaggle](https://www.kaggle.com/datasets/asaniczka/linkedin-data-engineer-job-postings/data).


## Technologies
- Cloud : GCP
- Infrastructure as code (IaC) : Terraform
- Containerisation : Docker
- Workflow orchestration : Mage-ai
- Data Warehouse : BigQuery
- Batch processing : Spark



## Data Pipeline

The end-to-end data pipeline includes the below steps:

1. Kaggle dataset is downloaded into the Google VM.
2. The downloaded CSV files (raw) are then uploaded to a folder in Google Cloud bucket (parquet) as Data Lake.
3. Next, the data will be stored in BigQuery with format and values same as the GCP bucket files.
4. Last new tables are created from those original tables by using Spark SQL with correct data types as well as partitioned by Month and Clustered for optimised performance. These tables would be Data Warehouse tables.
5. Spin up a dataproc clusters (master and worker) and execute the pyspark jobs for procusts analys purposes
6. Configure Google Looker Studio to power dashboards from BigQuery Data Warehouse tables.

### Workflow

![Workflow](img/flow.png)

## Dashboard

![Dashboard](img/dashboard.png)


## How to run project

1. Clone this repo using the below command:
```bash
git clone https://....
```
2. Build the project.
    2.1 Go to the project folder.
    ```bash
    cd <folder_name>
    ```
    2.2 Add execution access to build file.
    ```bash
    chmod +x build.sh
    ```
    2.3 Start building.
    ```bash
    ./build.sh
    ```

## Contacts
If you encounter any problem running any part of the project contact me at:

    - olgapogodina11@gmail.com

    - tg https://t.me/ol_pg