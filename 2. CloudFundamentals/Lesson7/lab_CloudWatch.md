# Cloud Watch
In this hands-on exercise, you will create a Cloud Watch event to notify via an SNS topic when an EC2 instance is created.

## Prerequisites:
- AWS account
- SNS Topic created in previous lab

Topics Covered:
By the end of this lab, you will be able to:
- Create Cloud Watch event to react to the creation of an Amazon EC2 instance
- Send SNS notification via Cloud Watch when an event occurs

Steps:
1. Create CloudWatch Rule
    - On the AWS Management Console page, type cloud watch in the Find Services box and then select CloudWatch. The CloudWatch Dashboard appears.
    - On the left-hand menu, under Events, select Rules.
    - Click Create rule.
    - For Service Name, select EC2.
    - For the Event Type, select EC2 Instance State-change Notification.
    - Select the Specific state(s) radio button. Select running from the drop-down box. Note: This configures the rule to trigger whenever an Amazon EC2 instance changes to the running state, which happens when an instance is launched or started.
    - On the right-hand side of the screen, in the Target section, add a target by clicking on Add target.
    - In the drop-down, change Lambda function to SNS topic.
    - For the Topic, select the topic you created in the SNS hands-on exercise. Important: If the Topic doesn’t appear, the Access policy – optional section doesn’t have the correct permissions to allow other services to access the Topic.
    - Scroll down and click the Configure details.
Enter a name in the Name field. Ensure the state is Enabled. Click Create rule.
2. Test CloudWatch Rule
    - Navigate to the EC2 console page, by clicking on Services in the upper left-hand menu. Type EC2 in the text box and click on EC2 found in the search results.
    - On the EC2 Dashboard page, click on Instances in the left-hand navigation.
    - Click Launch Instance.
    - Select the Amazon Linux 2 AMI (HVM), SSD Volume Type Amazon Machine Image (AMI). Important: You are free to choose a different AMI, but to avoid excessive charges, pick one that says, Free Tier Eligible.
    - For the Instance Type, select the free-tier instance type of t2.micro.
    - Click Review and Launch.
    - Click Launch.
    - Generate and download a new key pair and then launch the instance.
    - Click Launch Instances.
    - Click on View Instances.
    - Once the Instance state changes to Running, check your email client for an email alert from the SNS Topic.
3. Cleanup & Disable EC2 Instance and Cloud Watch Rule
    - To avoid recurring charges for leaving an instance running, let’s disable the EC2 instance.
    - From the EC2 Dashboard, select the instance just created, click Actions, then Instance State, and then select Terminate.
    - To avoid recurring charges for leaving the Cloud Watch rule running, let’s disable it.
    - From the SNS Dashboard, select Rules from under the Events section.
    - Select the Rule you just created, by clicking the radio button next to the Rule.
    - Click on the Actions button, and select Delete.