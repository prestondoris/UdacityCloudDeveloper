# Storage in the Cloud
Storage and database services in the cloud provide a place for companies to collect, store, and analyze the data they've collected over the years at a massive scale.

Storage Services in the cloud provide
- Durability
  - You will not loose the data that you put in the cloud
  - High durability gives piece of mind that data will be there in the future.
- Availability
  - Address how quickly you can access you data
  - High availability provides fast and reliable access to the data you store in the cloud.
- Scalability
  - Allows apps running in environment to always meet demands seemlessly
  - Automatically adding and removing
  - Maintain steady state
  - Three types of scaling
    - Vertical
      - Scaling up, when you modify the server to meet demands (more memory or capacity)
    - Horizontal
      - Scaling out, add or remove servers to meet demand
    - Diagonal
      - A combination of veritcal and horizontal

## Storage & Database Services
- Amazon Simple Storage Service (Amazon S3)
- Amazon Simple Storage Service (Amazon S3) Glacier
- DynamoDB
- Relational Database Service (RDS)
- Redshift
- ElastiCache
- Neptune
- Amazon DocumentDB

# S3 & S3 Glacier
Amazon Simple Storage Service (or S3) is an object storage system in the cloud. Like a file system in the cloud where you load files in the cloud.

Uploaded files in S3 get a unique url that can then be used to access it.

All objects( files ) are stored in buckets and a bucket can hold millions of objects. S3 buckets live in a region, but bucket names must be globally unique. 

Durability - 99.999999999%
Availability - 99.99%
Use Cases:
- Static Websites
- content delivery
- backup and recovery
- archiving and big data
- application data
- hybrid cloud storage

## Storage Classes
- S3 offers several storage classes, which are different data access levels for your data at certain price points.
- S3 Standard
- S3 Glacier - data archiving (a lot cheaper but data retrieval is much slower)
  - monthly log files that do not need a lot of frequent access
- S3 Glacier Deep Archive
- S3 Intelligent-Tiering
- S3 Standard Infrequent Access
- S3 One Zone-Infrequent Access

## Tips
- S3 is found under the Storage section on the AWS Management Console.
- A single object can be up to 5 terabytes in size.
- You can enable Multi-Factor Authentication (MFA) Delete on an S3 bucket to prevent accidental deletions.
- S3 Acceleration can be used to enable fast, easy, and secure transfers of files over long distances between your data source and your S3 bucket.

[Amazon S3](https://aws.amazon.com/s3/)
[Amazon S3 Glacier](https://aws.amazon.com/glacier/)
[What is Amazon S3 Glacier](https://docs.aws.amazon.com/amazonglacier/latest/dev/introduction.html)


# DynamoDB
DynamoDB is a NoSQL document database service that is fully managed. Unlike traditional databases, NoSQL databases, are schema-less. Schema-less simply means that the database doesn't contain a fixed (or rigid) data structure.

NoSQL are:
- Schemaless
- There is no fixed structure
  - can easily change on the fly based on the data being passed in
- Offers flexibility

Data:
- usually stored in JSON or JSON like text
- key-value pairs

Dynamo DB Tables:
- Each row or record is called a Document
- fully managed service
  - dont worry about servers
  - dont worry about patches or upgrades

Use Cases:
- Lyft
- AirBnB
- Netflix
- Snap

## Tips
- DynamoDB is found under the Database section on the AWS Management Console.
- DynamoDB can handle more than 10 trillion requests per day.
- DynamoDB is serverless as there are no servers to provision, patch, or manage.
- DynamoDB supports key-value and document data models.
- DynamoDB synchronously replicates data across three AZs in an AWS Region.

[Amazon DynamoDB Overview](https://aws.amazon.com/dynamodb/)
[What is Amazon DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html)

# Relational Database Service (RDS)
RDS (or Relational Database Service) is a service that aids in the administration and management of databases. RDS assists with database administrative tasks that include upgrades, patching, installs, backups, monitoring, performance checks, security, etc.

## Database Engine Support
- Oracle
- PostgreSQL
- MySQL
- MariaDB
- SQL Server

## Features
- failover
- backups
- restore
- encryption
- security
- monitoring
- data replication
- scalability


# Redshift
Redshift is a cloud data warehousing service to help companies manage big data or an extremely large volume of data that needs to be analyzed or reported against and quickly scale. Redshift allows you to run fast queries against your data using SQL, ETL, and BI tools. Redshift stores data in a column format to aid in fast querying.

A data warehouse is designed for fast querying and analysis not transaction processing and usually contains historical data from transactional systems. For example if you manage a website that allows users to order products online and you have a RDB that stores order information. The most recent orders will most likely need to be transacted against in day to day operations, but orders from 10 years ago maybe archieved to a data warehouse like Redshift.

## Tips
- Redshift can be found under the Database section on the AWS Management Console.
- Redshift delivers great performance by using machine learning.
- Redshift Spectrum is a feature that enables you to run queries against data in Amazon S3.
- Redshift encrypts and keeps your data secure in transit and at rest.
- Redshift clusters can be isolated using Amazon Virtual Private Cloud (VPC).

[What Is Amazon Redshift](https://docs.aws.amazon.com/redshift/latest/mgmt/welcome.html)
[Amazon Redshift Overview](https://aws.amazon.com/redshift/)

# CDN 
Why do we need content delivery in the cloud?

A content delivery network (CDN) speeds up delivery of your static and dynamic web content such as webpages, CSS, JS, and images.

Typically content is cached for a certain amount of time so when  a user requests information, the cache is checked first to pull from that.

Benefits:
- reduces latency
- decreases load on your server
- provides good end user experience

Latency
- The time is takes to respond to a request
- high latency causes your website to load slowly


# Cloud Front
CloudFront is used as a global content delivery network (CDN). Cloud Front speeds up the delivery of your content through Amazon's worldwide network of mini-data centers called Edge Locations.

CloudFront works with other AWS services, as shown below, as an origin source for your application:

- Amazon S3
- Elastic Load Balancing
- Amazon EC2
- Lambda@Edge
- AWS Shield

## Tips
- CloudFront is found under the Networking & Content Delivery section on the AWS Management Console.
- Amazon countinously adds new Edge Locations.
- CloudFront ensures that end-user requests are served from the closest edge location.
- CloudFront works with non-AWS origin sources.
- You can use GeoIP blocking to serve content (or not serve content) to specific countries.
- Cache control headers determine how frequently CloudFront needs to check the origin for an updated version your file.
- The maximum size of a single file that can be delivered through Amazon CloudFront is 20 GB.

[Amazon CloudFront Overview](https://aws.amazon.com/cloudfront/)
[What is Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)