<h1 align='center'>BigQuery</h1>

### GCP VS AWS VS AZURE

[refer](http://blogs.vmware.com/cloudhealth/files/2018/07/Aws-vs-Azure.png)

# All services gcp constituted

### Compute Services
- Compute Engine
  - IAAS
  - Provide configurable VMs
  - Highly Configureable
  - Pay per second

- App Engine
  - Paas
  - focus code all backend handle by google
  - zero to extreme scalabilty
  
- Google Kubernetes Engine(GKE)
  - Container as a service(CaaS)
  - Cluster running self sufficient container
  - Self fully manager clustered

- Cloud Function
  - Function as a service(FaaS)
  - Event driven serverless compute platform
  - Write code and google cloud handle operational infrastructure.
  
### Storage & Databases

- Cloud compute storage
  - Store any kind of data
  - Durable, relaiable obkect storage.
 
- Cloud Sql
  - fully managed rdbms for hosting mysql, pgsql and sql server.

- Cloud BigTable
  - To work with NoSql data
  - Easy to integrate with hadoop and spark.

- Cloud DataStore
  - NoSql schema less database for storing non-relational data.
  - Alternate to bigtable when ACID trascations are required.
 
- Cloud Spanner
  - Database service for cloud
  - relational + non-relational db
  - provide 99.999% availabilty.

### Big Data Services

- BigQuery
  - Datawarehouse use to store and query big data using sql
  - Create customs schema load data perform operation etc.
  
- Cloud Dataflow
  - A fully managed data processing service for batch and stream Big data processing 
  - Based on Apache Bearn's unified programming model

- Cloud Dataproc
  - Apache Spark and Apache hadoop management

- Cloud Pub/Sub
  - Fully managed real-time messaging service.
  
- Cloud Datalab
  - Data exploration, analysis and visualization.

- Cloud Dataprep
  - Exploring, cleaning and preparing both structured and unstructured data.

- Cloud Composer
  - Monitor workflows and data processing pipelines.
 
- Cloud Data Fusion
  - Fully managed cloud-native data integration at any scale, ETL service of GCP.

### AI & ML Services

- Cloud AI building block
  - Cloud video intelligence API
  - Cloud sppech to text
  - Cloud Vision API(Image labelling, Face and Landmark detection, OCR)
  - Cloud Natural Language API(Sentiment analysis, content classification)
  - Cloud Translation(Translate text to various languages)
  - Dialog flow

- AutoML

- BigQuery ML
  - Enable user to execute ML models by using normal sql query.
- AI platform
  - Data scientist & data engineering work

### Big Data Ecosystem [Refer](https://miro.medium.com/max/1400/0*HQTP_FpEDiIth6DE)

### Data warehouse

Data coming from multiple sources need some location to store. So, Datawarehouse some in role.

### Data mining 

To get why ans we use data mining for example why sales is down etc.

### BigQuery

Bigquery is a fully managed, serverless, highly scalable, and cost-effective cloud datawarehouse designed for business agility. In bigquery we have top level container which is dataset which contain multiple table in it.

- Bigquery support both batch and streaming of data.
- 100k rows per sec to store
- In a batch mode it can store TB of data
- Support AI and ML
- Fully managed
- Pay per use
- Scalable.
- Automated data transfer
- Access Control IAM(Identity and access management) 

### Architecture ![refer](https://storage.googleapis.com/gweb-cloudblog-publish/images/BQ_Explained_2.max-900x900.jpg)

- Engine - **Dremel**, which is compbination of columnar and tree architecture.
- File System - **Clossus**(Columnar storage), Google distributed file system.

- Query setting help to work with batch data(Bigquey Engine) and Cloud Dataflow(Streaming data).

### Auto Schema Detection

- BigQuery select random file in source -> scans upto 100 rows as sample -> examine each field's and attempts to assign data type based on sample values.
- Csv and Json onlt.
- date schema auto detection must be in yyyy-mm-dd format
- BigQery consider header row by default by comparing data in the column.
