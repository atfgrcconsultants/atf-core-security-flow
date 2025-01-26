# atf-core-security-flow
Most small to medium businesses will generally have a simple website with the following components-

<img src="images/small-business-web.png" alt="Lucidchart Diagram" width="500"/>

We want to get started with the client fast and show them the work to gain confidence. We immediately map the components to <a href="https://www.cisecurity.org/controls/cis-controls-list" target="_blank">CIS 18 critical security controls</a> . This is safe as there are available mappings towards other frameworks.

#### Scenario Setup
Let us consider a more detailed ficitional business setup in order to do a elaborate assessment.

<img src="images/small-business-aws.png" alt="Lucidchart Diagram" width="500"/>

We have the following components-
1. AWS EC2 instances that host Apache web servers.
2. AWS Lambda function that takes instructions from web servers.
3. AWS RDS database to store data.

###### CIS Control 1: Inventory and Control of Enterprise Assets
Inventory of Assets:
1. Web server and firewall.
2. App server.
3. Database server.

###### CIS Control 2: Inventory and Control of Software Assets
Inventory of Software:
1. Apache/Nginx
2. SQL/Nosql
3. Firewall suite
4. web application/inhouse software

P.S.- CIS Control 1 and 2 can be equivalent of scoping in other frameworks such as NIST CSF 2.0's Identify function or ISO 27001. I will show later how if we want do to NIST CSF 2.0 with the same architecture. 

###### CIS Control 3: Data Protection
We first categorize the data.
1. End client and admin authentication data.
2. End client PII.
3. System and server log data.
4. Payment Information.

P.S.- These information can be used to create a baseline of state of data in NIST CSF 2.0.

###### CIS Control 4: Secure Configuration of Enterprise Assets and Software
To be continued ...
