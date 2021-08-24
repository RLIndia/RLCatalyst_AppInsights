# RLCatalyst AppInsights

RLCatalyst AppInsights is a product complementing AWS Service Catalog AppRegistry to provide Application Centric views of cloud resources combining infrastructure, applications and services to support a dynamic CMDB for operational excellence and cost governance in ServiceNow.


This capability provides actionable intelligence for Capacity tracking, Health, Compliance, security, health and Cost of all assets in near-real time. With capability of tracking application metrics across multi-accounts to provide Organization aggregated details helps in Total Cost of Application Management (TCAM).


The product is built on ServiceNow ITSM and integrates with AWS Service Catalog AppRegistry and Service Management Connector. The product provides dashboards and drill-down information for topology views with issue detection & resolution using automation runbooks & BOTs. The solution provides capability to add additional functionality and customization of User Interface, functional features and data integration to external third-party systems using RL DataBridge adapters.


**Benefits of RLCatalyst AppInsights :**

•	Cost planning, tracking and optimization across application centric views aligned with business

•	Near real-time asset, health, security and compliance drives operational excellence

•	Detection of idle capacity and Orphaned resources helping plug cost and security leakages

•	Ability to automate, remediations providing ‘single pane of control’ for Cloud Operational Management with ServiceNow


![Architecture](https://user-images.githubusercontent.com/64137641/130602792-8feac980-8571-49c6-a4c4-3941ea860668.png)

# To create API Gateway and Lambda functions required for RLCatalyst AppInsights Solution on AWS

For one click deployment click here  [![Launch Stack](https://user-images.githubusercontent.com/64137641/130605188-bc6546bf-3526-4c62-a35c-30cce25c3275.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateURL=https://rlcatalystappinsights.s3.amazonaws.com/listapp.template)


API Gateway: 

Deployed as a REGIONAL endpoint.

Integrated with Lambda function

Lambda function:

In-line Python Lambda function to retrieve the list of applications, attributes and application related meta-data.

Creates an authorization layer that API Gateway activates for methods that have authorization enabled. API Gateway activates the authorizer when a client calls those methods

IAM:

IAM role for Lambda allowing CloudWatch logs access

IAM role with permissions that allow API Gateway endpoint to successfully invoke lambda function


