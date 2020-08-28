# Security in the Cloud
Why do we need security for applications?

As adoption for cloud services has increased, so has the need for security in the cloud.

Companies must secure a persons data especially if it is PII (personally identifiable information)
- SSN
- Passport Information
- Bank account information

Along with protecting the data, we must also protect the applications that access the data. Cloud security can protect the data, application, and the infrasturcture applications run on.

# AWS Shield
AWS Shield is a managed DDoS (or Distributed Denial of Service) protection service that safeguards web applications running on AWS.

DDoS Attach
- an attempt to make a website or application unavailable by overwhelming it with traffic from multiple services.
- the goal is to crash the server which would no longer serve requests making it unavailable.

AWS Shield is a service that you get "out of the box", it is always running (automatically) and is a part of the free standard tier. If you want to use some of the more advanced features, you'll have to utilize the paid tier.

# Tips
- AWS Shield can be found under the Security, Identity, & Compliance section on the AWS Management Console.
- AWS Shield Standard is always-on, using techniques to detect malicious traffic.
- AWS Shield Advanced provides enhanced detection.

[AWS Shield Overview](https://aws.amazon.com/shield/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc)

# AWS WAF
AWS WAF (or AWS Web Application Firewall) provides a firewall that protects your web applications.

Firewall
- A firewall is a networks security mechanism that monitors and controls incoming and outgoing network traffic based on preset security rules.
- a firewall stands in front of your application as a way to guard who can access it. the rules that are set up inside the firewall allow certian traffic or block it. Used to protect your application from unintended access

WAF can stop common web attacks by reviewing the data being sent to your application and stopping well-known attacks.

# Tips
- WAF is found under the Security, Identity, & Compliance section on the AWS Management Console.
- WAF can protect web sites not hosted in AWS through Cloud Front.
- You can configure CloudFront to present a custom error page when requests are blocked.

[AWS Web Application Firewall](https://aws.amazon.com/waf/)


# Identity & Access Management
Identity & Access Management (IAM) is an AWS service that allows us to configure who can access our AWS account, services, or even applications running in our account. IAM is a global service and is automatically available across ALL regions.

# Security Concepts
- User
- IAM Group
- IAM Role
- Policy

[AWS IAM Overview](https://aws.amazon.com/iam/)
[What is IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)