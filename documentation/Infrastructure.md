# Infrastructure

## Introduction

The purpose of this application is to deploy this application on AWS. deploy the frontend as a static website on S3, the database in this app is PostgreSQL on RDS, and deploy the dynamic website it represents in Nodejs supported on

## What is AWS?

AWS (Amazon Web Services) is a comprehensive, evolving cloud computing platform provided by Amazon that includes a mixture of infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings.

## AWS Services

There are many AWS services, but the most relevant to this project are:

-  Simple Storage Service (S3)

   ![AWS_S#](https://miro.medium.com/max/240/1*B9CIOrxdROHvtdmouQA1_A.png)

   Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. You can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere.

-  Database Service (RDS)

   ![AWS_RDS](https://miro.medium.com/max/240/1*KqNnfYtaVshGXbuGUCTOQw.png)

   Amazon Relational Database Service (RDS) is a managed SQL database service provided by Amazon Web Services (AWS). Amazon RDS supports an array of database engines to store and organize data. It also helps with relational database management tasks, such as data migration, backup, recovery and patching.

-  Elasticbeanstalk (EB)

   ![AWS_EB](https://www.awsomeblog.com/wp-content/uploads/2015/07/elastic_beanstalk.png)

   AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, . NET, PHP, Node. js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

## AWS Hook of Udagram App

![AwsHook](aws.png)
We'll talk about the AWS Request lifecycle in this app

-  First of all, the user accesses the front-end URL and that website is published on `S3`
-  Then the front end needs to connect to the backend deployed on the `EB` to send or receive data for example
   -  Registration: send data to be stored in the database.
   -  Log: submit the data to check whether this data is correct or not.
   -  Or get the data that will appear for each user
-  Then the backend calls the database stored on `RDS` to get or store user data.
