# How to setup Cloud Pak for Data on Red Hat OpenShift for AWS
In this tutorial, you will learn how to setup CPD on ROSA

## Introduction
State the purpose of your tutorial, your intended audience, and the benefits readers can gain from it. Aim to grab the reader’s interest quickly, using terms they are likely to search on and relate to.

## Prerequisites
List or describe any skills, tools, experience, or specific conditions required to perform the tutorial. Include version levels for any required tools or platforms. Include links to necessary resources whenever possible.

## Estimated time
Provide guidance on how long it will reasonably take to complete the steps under normal circumstances.

## Steps
### Step 1: Create an OpenShift IAM user in AWS

An IAM user ***osdCcsAdmin*** within the AWS account has to be created for OpenShift installer to get access to your AWS infrastructure.

The IAM user needs at least **Programmatic access** access type enabled and this user must have the **AdministratorAccess** policy attached to it.

- Goto [Identity and Access Management (IAM)](https://console.aws.amazon.com/iam/home) on AWS console.
- Under **Access management** click on **Users**.

- Create a new user ***osdCcsAdmin*** by selecting AWS access types as follows:
  - Programmatic access
  - AWS Management Console access

- Create a user group to manage ***osdCcsAdmin*** permissions. Make sure to enable **AdministratorAccess** and create the group.

- Select the recently created user group to proceed.

- Optionally you can add Tags.

- Review the details and create a user as shown.

- On Successfully creating ***osdCcsAdmin*** IAM User **Download csv** as you will require the **Access key ID** and the **Secret access key** in further steps.

- Also make a note of your Account ID as it will be required in further steps.
![aws account id](doc/source/images/awsaccountid.png)

- At this point, you will have successfully created: 
  - IAM user ***osdCcsAdmin*** with required permissions.
  - **AWS access ID**, **AWS account key ID** and **AWS secret access key** credentials.
## Summary
State any closing remarks about the task or goal you described and its importance. Reiterate specific benefits the reader can expect from completing your tutorial. Recommend a next step (with link if possible) where they can continue to expand their skills after completing your tutorial.

## Related links
Include links to other resources that may be of interest to someone who is reading your tutorial.
