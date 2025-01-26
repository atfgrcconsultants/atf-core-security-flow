# atf-core-security-flow
Most small to medium businesses will generally have a simple website with the following components:

<img src="images/small-business-web.png" alt="Lucidchart Diagram" width="500"/>

We want to get started with the client fast and show them the work to gain confidence. We immediately map the components to <a href="https://www.cisecurity.org/controls/cis-controls-list" target="_blank">CIS 18 critical security controls</a> . This is safe as there are available mappings towards other frameworks.

#### Scenario Setup
Let us consider a more detailed ficitional business setup in order to do a elaborate assessment.

<img src="images/small-business-aws.png" alt="Lucidchart Diagram" width="500"/>

We have the following components:
1. AWS EC2 instances that host Apache web servers.
2. AWS WAF to filter traffic to web servers.
3. AWS Lambda function that takes instructions from web servers.
4. AWS RDS database to store data.
5. AWS Cloudwatch service logging all the above components.

###### CIS Control 1: Inventory and Control of Enterprise Assets
Inventory of Assets:
1. AWS EC2 instances
2. AWS WAF
3. AWS RDS
4. AWS Cloudwatch

###### CIS Control 2: Inventory and Control of Software Assets
Inventory of Software:
1. Apache web server software
2. Javascript/React frontend web application
3. Python scripts to execute as Lambad functions

###### CIS Control 3: Data Protection
We first categorize the data.
1. End user's authentication and PII.
2. CloudWatch log data.
   
###### CIS Control 4: Secure Configuration of Enterprise Assets and Software
1. AWS EC2 configurations i.e. IAM credentials, EC2 instance types and sizes. Maps to <a href="https://owasp.org/Top10/A05_2021-Security_Misconfiguration/" target="_blank">OWASP Top 10- A05:2021 – Security Misconfiguration.</a> Please also refer to [AWS EC2 best practices](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-best-practices.html).
2. 
