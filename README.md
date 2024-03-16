# Retail Data Pipeline

## Table of Contents

* [Overview](#overview)
* [Dataset Description](#dataset-description)
* [Technologies](#technologies)
* [Pipeline](#pipeline)
* [Data Modeling](#data-modeling)
* [Getting Started](#getting-started)
* [Reference](#reference)

## Overview
This project serves as a comprehensive guide to building an end-to-end data engineering pipeline. The pipeline is built on Apache Airflow and dbt, and is deployed on Astronomer. The data is stored in Google Cloud Storage and BigQuery. The pipeline is built to be modular and scalable, and can be easily adapted to other use cases.

The dataset used in this project is the [Online Retail Data Set](https://www.kaggle.com/datasets/tunguz/online-retail) from Kaggle. This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

### Dataset Description

| Column | Description |
| --- | --- |
| InvoiceNo | Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation. |
| StockCode | Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product. |
| Description | Product (item) name. Nominal. |
| Quantity | The quantities of each product (item) per transaction. Numeric. |
| InvoiceDate | Invoice Date and time. Numeric, the day and time when each transaction was generated. |
| UnitPrice | Unit price. Numeric, Product price per unit in sterling. |
| CustomerID | Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer. |
| Country | Country name. Nominal, the name of the country where each customer resides. |

## Technologies

* Apache Airflow
* dbt
* Google Cloud Storage, BigQuery
* Soda
* Metabase
* Python
* Docker, Docker Compose

## Pipeline

## Data Modeling


## Getting Started

1. Clone the repo
2. Create a project on Google Cloud Platform, then create a service account and download the key file
3. Add the key file to the `include/gcp` folder
4. Run 
```bash
astro dev start

To start the airflow server. The airflow UI will be available at https://localhost:8080

##Reference
https://robust-dinosaur-2ef.notion.site/PUBLIC-Retail-Project-af398809b643495e851042fa293ffe5b
https://astro-sdk-python.readthedocs.io/en/stable/guides/operators.html
https://registry.astronomer.io/providers/apache-airflow-providers-google/versions/10.12.0/modules/LocalFilesystemToGCSOperator