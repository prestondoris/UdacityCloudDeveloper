# Servers in the Cloud

Servers in the cloud allow you to build:
- Failure resilient applications
- Grow and shrinking capacity
- Only pay for what you use
- Are not locked into long term contracts


## Elastic Cloud Compute
Elastic Cloud Compute or EC2 is a foundational piece of AWS' cloud computing platform and is a service that provides servers for rent in the cloud.
- Servers for Rent
- Manage and deploy applications
- Servers are called instances
  - Instances are actual physical servers in an AZ (not considered serverless)
- EC2 is elastic, so it can grow and shrink based on the needs of the application

## Pricing Options
There are several pricing options for EC2.
- On Demand - Pay as you go, no contract.
- Dedicated Hosts - You have your own dedicated hardware and don't share it with others.
- Spot - You place a bid on an instance price. If there is extra capacity that falls below your bid, an EC2 instance is provisioned. If the price goes above your bid while the instance is running, the instance is terminated.
- Reserved Instances - You earn huge discounts if you pay up front and sign a 1-year or 3-year contract.
0425

## Tips
- EC2 is found under the Compute section of the AWS Management Console.
- Spot instances can save you up to 90% off the on-demand pricing.
- There are several instance types that provide varying combinations of CPU, memory, storage, and networking capacity.


# EC2 Dashboard
Running Instances will show all of the running instances that you have running.

Within the description of the instance, there is an instance type which determines your instance's CPU capacity, memory, and storage (m1.small, c1.xlarge)

Block Devices are like additional hard drives attached to the instance for additional storage.



# Elastic Block Store (EBS)
Elastic Block Store (EBS) is a storage solution for EC2 instances and is a physical hard drive that is attached to the EC2 instance to increase storage. It must be attached to your server and mounted before you start storing data on it. Some instance types already have volumes attached.

Benefits
- Two types
  - In memory store(or instance store)
  - EBS
- Using EBS over instance store is that you are able to persist data after EC2 is terminated.
  - Any data store on that volume is still accessible.
- Each volume is automatically replicated in its AZ

Tips
EBS is found on the EC2 Dashboard.
There are several EBS volume types that fall under the categories of Solid State Drives (SSD) and Hard Disk Drives (HDD).


[Amazon Elastic Block Storage](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html)

# Why do we need security in the cloud
Allows you to have complete control over your virtual networking environment. Once you have configured your virtual network, with public or private facing subnets ([What is a subnet](https://www.cloudflare.com/learning/network-layer/what-is-a-subnet/)) You can then launch or place your servers in the selected network to secure access.


# Virtual Private Cloud (VPC)
Virtual Private Cloud or VPC allows you to create your own private network in the cloud. You can launch services, like EC2, inside of that private network, and EC2 inherits security. This is done as a security measure. We control the network configuration and security and expose what we do or do not want exposed to the internet using public or private Subnets. A VPC spans all the Availability Zones in the region.


VPC allows you to control your virtual networking environment, which includes:
- IP address ranges
- subnets
- route tables
- network gateways

### Tips
- VPC is found under Networking & Content Delivery section of the AWS Management Console.
- The default limit is 5 VPCs per Region. You can request an increase for these limits.
- Your AWS resources are automatically provisioned in a default VPC.
- There are no additional charges for creating and using the VPC.
- You can store data in Amazon S3 and restrict access so that it’s only accessible from instances in your VPC.

[Virtual Private Cloud](https://en.wikipedia.org/wiki/Virtual_private_cloud)
[Amazon Virtual Private Cloud](https://aws.amazon.com/vpc/)
[Amazon VPC Documentation](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)


# Compute Power
Provides the ability to run application code in the cloud without having to provision or manage servers. Allows for automatic scaling, high availability, fault tolerance, and frees up the developer to write code for new features.

Compute Power provides:
- No servers
- Continuously scale
- Run code on demand
- Pay when code runs

# Lambda
AWS Lambda provides you with computing power in the cloud by allowing you to execute code without standing up or managing servers. Think of Lambda as a chunk of code that runs in the cloud and is meant to do one specific task. Lambda should only worry about one specific task, because there is currently a time limit of 15 mintues. An application developed using Lambda's is considered to be serverless because your not concerned with the server your code is running on.

Benefits
- only pay when your code is run
  - not charged when your code is not running.
- author code locally and upload it, or write in Lambda console.
- Lambda is event driven so you can run your code based on certain events happening like a file upload or a record being inserted into the DB.

## Tips
- Lambda is found under the Compute section on the AWS Management Console.
- Lambdas have a time limit of 15 minutes.
- The code you run on AWS Lambda is called a “Lambda function.”
- Lambda code can be triggered by other AWS services.
- AWS Lambda supports Java, Go, PowerShell, Node.js, C#/.NET, Python, and Ruby. There is a Runtime API that allows you to use other programming languages to author your functions.
- Lambda code can be authored via the console.

[AWS Lambda](https://aws.amazon.com/lambda/)

# Elastic Beanstalk
Elastic Beanstalks is an orchestration service that allows you to deploy a web application at the touch of a button by spinning up (or provisioning) all of the services that you need to run your application.

# Tips
- Elastic Beanstalk is found under the Compute section of the AWS Management Console.
- Elastic Beanstalk can be used to deployed web applications developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker.
- You can run your applications in a VPC.

[AWS Elastic Veabstalk](https://aws.amazon.com/elasticbeanstalk/)