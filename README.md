# CIS18-security-assessment-flow
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
3. AWS Lambda
4. AWS RDS
5. AWS Cloudwatch

###### CIS Control 2: Inventory and Control of Software Assets
Inventory of Software:
1. Apache web server software
2. Javascript/React frontend web application
3. Python scripts to execute as Lambda functions

###### CIS Control 3: Data Protection
We first categorize the data.
1. End user's authentication and PII
2. CloudWatch log data
3. App and system confguration data
Data Protection Controls:

***Note: The following will give you pointers. The security controls that get selected would depend on organizational contexts, budget, risk profile and risk appetite.
1. Maps to [OWASP A02:2021 – Cryptographic Failures](https://owasp.org/Top10/A02_2021-Cryptographic_Failures/), [OWASP A03:2021 – Injection](https://owasp.org/Top10/A03_2021-Injection/) and [OWASP A09:2021 – Security Logging and Monitoring Failures](https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures/).
2. Make sure logs are tamper resistant. This maps to [A08:2021 – Software and Data Integrity Failures](https://owasp.org/Top10/A08_2021-Software_and_Data_Integrity_Failures/).

   
###### CIS Control 4: Secure Configuration of Enterprise Assets and Software
***Note: The following will give you pointers. The security controls that get selected would depend on organizational contexts, budget and risk profile and risk appetite.

1. AWS EC2 configurations i.e. IAM credentials, EC2 instance types and sizes. Maps to <a href="https://owasp.org/Top10/A05_2021-Security_Misconfiguration/" target="_blank">OWASP Top 10- A05:2021 – Security Misconfiguration.</a> Please also refer to [AWS EC2 best practices](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-best-practices.html).
2. AWS Lambda security misconfigurations. Maps to [OWASP Serverless Top 10](https://owasp.org/www-project-serverless-top-10/), AWS Lambda security best practices[1](https://docs.aws.amazon.com/lambda/latest/dg/best-practices.html) and [2](https://docs.aws.amazon.com/lambda/latest/dg/lambda-security.html).
3. AWS RDS maps to [Owasp Database Security Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Database_Security_Cheat_Sheet.html) and [AWS best practices](https://aws.amazon.com/blogs/database/applying-best-practices-for-securing-sensitive-data-in-amazon-rds/).
4. Configure AWS WAF rules to protect against OWASP Top 10 and other rules based on the system context.
