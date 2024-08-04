# amazon-connect - Build a bank contact center use case with options of help with the account or schedule an appointment.

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
9. Configuring Amazon Connect permissions for Lex bots and Lambda function
10. Configure contact flows with the new lexbots created.
11. Save and publish contact flow
12. Assign the contact flow to the number claimed in the connect instance.

Place a test call to your claimed phone number to interact with the contact flow. Click the phone icon on the Connect Dashboard to open the Contact Control Panel and answer the calls!

Try these options:

**Call #1:**

Call the number that is assigned to the Intro Flow 1
From the Main Menu – say: “I need help with my account”
From the Account Type Menu – say “I have a personal account”
From the Agent CCP, make sure that the agent state is Available, when the call is presented, select Accept Call – You will hear Platinum
Hang 

**Call #2:**

Call the number that is assigned to the Intro Flow 1
From the Main Menu – say: “I would like to schedule an appointment”
Answer the Schedule Appoint bot questions:
Q: What type of appointment would you like to schedule? 
A: New Account or New Loan

Q: What is your first name?
A: provide name

Q: What is your last name?
A: provide name

Q: What is your phone number?
A: provide 10-digit phone number

Q: What day or date would you like to schedule an appointment for?
A: Provide a date or day of week (next Tuesday or August 20th)

Q: What time would you like to request for your appointment?
A: Provide time in 12 hour clock with AM/PM or 24 hour clock

Receive confirmation of appointment and then asked, “Should I go ahead and book your appointment?”, say YES.
“Is there anything else I can help you with?”, say NO
From the Agent CCP, make sure that the agent state is Available, when the call is presented, select Accept Call – You will hear Platinum
Hang up
