# Networking
Networks reliably carry loads of data around the globe allowing for the delivery of content and applications with high availability. The network is the foundation of your infrastructure.

## Cloud networking includes:

- network architecture
- network connectivity
    - services that offer reliable and cost effective ways to route n users to internet applications
- application delivery
- global performance
- delivery

# Route 53
Route 53 is the AWS cloud domain name system (DNS) service that has servers distributed around the globe used to translates human-readable names like www.google.com into the numeric IP addresses like 74.125.21.147.

Scales automatically to handle spikes in DNS queries
Register a Domain Name
Routes Internet Traffic to the resources for your domain and checks the health of your resources.

Health checkes are useful because they help to ensure that your web servers are up and running and offer DNS failover to automatically route web visiters to avoid site outages.


## Features
- scales automatically to manage spikes in DNS queries
- allows you to register a domain name (or manage an existing)
- routes internet traffic to the resources for your domain
- checks the health of your resources

## Tips
- Route 53 is found under the Networking & Content Delivery section on the AWS Management Console.
- Route 53 allows you to route users based on the user’s geographic location.

[Amazon Route 53 Overview](https://aws.amazon.com/route53/)

# Elasticity in the Cloud
One of the main benefits of the cloud is that it allows you to stop guessing about capacity when you need to run your applications. Sometimes you buy too much or you don't buy enough to support the running of your applications.

With elasticity, your servers, databases, and application resources can automatically scale up or scale down based on load.

## Resources
Resources can scale up (or vertically). In Amazon EC2, this can easily be achieved by stopping an instance and resizing it to an instance type that has more RAM, CPU, IO, or you can scale out (or horizontally), which increases the number of resources. An example would be adding more servers.


# EC2 Auto Scaling
EC2 Auto Scaling is a service that monitors your EC2 instances and automatically adjusts by adding or removing EC2 instances based on conditions you define in order to maintain application availability and provide peak performance to your users.

EC2 Autoscaling works with AWS notification services like SNS (simple notification service) to alert you with EC2 Auto scaling is launching or terminating your EC2 instances. You can configure your alert message about the instance and reason for the termination or launch of the instance.

There is also an AWS Auto Scaling service that allows you to set up other services to automatically scale (like DynamoDB)

## Features
- Automatically scale in and out based on needs.
- Included automatically with Amazon EC2.
- Automate how your Amazon EC2 instances are managed.

## Tips
- EC2 Auto Scaling is found on the EC2 Dashboard.
- EC2 Auto Scaling adds instances only when needed, optimizing cost savings.
- EC2 predictive scaling removes the need for manual adjustment of auto scaling parameters over time

[Amazon EC2 Autoscaling Overview](https://aws.amazon.com/ec2/autoscaling/)
[What is Amazon EC2 Autoscaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)


# Elastic Load Balancing
Elastic Load Balancing automatically distributes incoming application traffic across multiple servers.

## Elastic Load Balancer is a service that:
- Balances load between two or more servers
- Stands in front of a web server
- Provides redundancy and performance

## Tips
- Elastic Load Balancing can be found on the EC2 Dashbaoard.
- Elastic Load Balancing works with EC2 Instances, containers, IP addresses, and - Lambda functions.
- You can configure Amazon EC2 instances to only accept traffic from a load balancer.

[Amazon Elastic Load Balancing Overview](https://aws.amazon.com/elasticloadbalancing/)