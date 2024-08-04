# amazon-connect-

**Build Contact Center with Amazon Connect**

Amazon Connect integrates with other AWS services like AWS Lamda  and Amazon DynamoDB  allow you to create dynamic, personalized experienced for your callers. In this session, you will learn how to create Queues, Routing Profiles and configure Users and integrate AWS Lambda and Amazon DynamoDB services with your contact center.

Elements in this demo will include:

**Amazon Connect** - Create Queues, Routing Profiles, and configure Users

**AWS IAM** - Create an IAM Policy and Role that allows Lambda to integrate with DynamoDB

**Amazon DynamoDB** - Create DynamoDB Table to host Contact IDs that will set Membership Level

**AWS Lambda** - Import function for integration and data exchange between Amazon Connect & DynamoDB

**Amazon Connect** - Update your contact flow with Queues and AWS Lambda functions

**Creating Dynamic personalized experiences in Amazon Connect**

1. Create Amazon connect instance from aws console.
2. Claim a number to test the flow
3. create Queues, Routing profiles and configure users -  **Queues** - Silver, platinum, gold, business  **Routing Profile** -  Membership
4. Create IAM Policy and Role to allow Lambda integrate with DynamoDB
5. Create DynamoDB table with table name =  membershipTable , PartitionKey - PhoneNumber and Sort Ket - membershipLevel to host contact IDs that will set membership Level.
6. Create Lambda function to check membership level of the customer phonenumber from dynamoDB table.
7. Build a contact flow with the different queues and Lambda function.
8. Create new lex bots
9. Configuring Amazon Connect permissions for Lex bots.
10. Configure contact flows with the new lexbots created.
