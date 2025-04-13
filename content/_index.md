+++
title = "Setting up an AWS account"
date = 2021
weight = 1
chapter = false
+++

# Creating Your First AWS Account

#### Overview
In this first lab, you will create your new **AWS** account and use Multi-Factor Authentication (**MFA**) to enhance your account security. Next, you will create an **Administrator Group** and **Admin User** to manage access to resources in your account instead of using the root user. Finally, we will guide you through account authentication with **AWS Support** in case you encounter authentication issues.

#### AWS Account
**An AWS account** is the fundamental container for all the AWS resources you can create as an AWS customer. By default, each AWS account includes a _root user_. The _root user_ has full access within your AWS account, and root user permissions cannot be restricted. When you first create your AWS account, you will access it as the _root user_.

{{% notice note%}}
As a best practice, avoid using the AWS account _root user_ for any task where it's not necessary. Instead, create a new IAM user for each person requiring administrator access. Subsequently, users in the administrators user group should set up the user groups, users, and so on, for the AWS account. All future interactions should be through the AWS account's users and their own keys instead of the root user. However, to perform certain account and service management tasks, you must log in using the root user credentials.
{{% /notice%}}

#### Multi-Factor Authentication (MFA)
**MFA** adds an extra layer of security by requiring users to provide unique authentication from an AWS-supported MFA mechanism in addition to their regular sign-in credentials when accessing AWS websites or services.

#### IAM User Group
An **IAM User Group** is a collection of IAM users. User groups allow you to specify permissions for multiple users, simplifying the management of those users' permissions. Any user in that user group automatically inherits the permissions assigned to the user group.

#### IAM User
An **IAM User** is an entity you create in AWS to represent the person or application that interacts with AWS. A user in AWS consists of a name and credentials. Note that an IAM user with administrator permissions is not the same as the AWS account root user.

#### AWS Support
AWS Basic Support offers all AWS customers access to our Resource Center, Service Health Dashboard, Product FAQs, Discussion Forums, and Support for Health Checks – at no additional charge. Customers seeking a deeper level of support can subscribe to AWS Support at the Developer, Business, or Enterprise level.

Customers who choose AWS Support receive one-on-one, fast-response support from AWS engineers. The service assists customers in using AWS's products and features. With pay-by-the-month pricing and unlimited support cases, customers are freed from long-term commitments. Customers with operational issues or technical questions can contact a team of support engineers and receive predictable response times and personalized support.

#### AWS Management Console
The **AWS Management Console** provides a simple web interface for AWS users.

#### Main Content

1. [Creating a New AWS Account](1-create-new-aws-account/)
2. [Setting Up MFA for the AWS Account Root User](2-MFA-Setup-For-AWS-User-(root))
3. [Creating Administrator Accounts and Groups](3-create-admin-user-and-group/)
4. [Getting Support for Account Authentication](4-verify-new-account/)
5. [Explore and Configure the AWS Management Console](5-explore-and-configure-the-aws-management-console/)
