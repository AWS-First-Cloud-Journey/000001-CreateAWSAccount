---
title: "Close Standalone AWS Account"
date: "2025-10-05"
weight: 4
chapter: false
pre: " <b> 1.4 </b> "
---

## Close Standalone AWS Account

### Considerations Before Closing Your AWS Account

Before closing your AWS account, you should consider the following:

#### Your Agreement with AWS

Closing your AWS account serves as notice to us that you want to cancel the AWS customer agreement or other agreement with AWS that governs your AWS account, solely with respect to this specific AWS account. If you reopen your AWS account during the post-closure period (within 90 days after you close the account), you agree that the same agreement terms will govern your access to and use of the service offerings through your reopened AWS account.

#### AWS Management Console Access

Access to the AWS Management Console for a closed AWS account will be restricted. During the post-closure period, you can still sign in to your AWS account to view past billing information and access AWS Support. You cannot access any other AWS services or start any new AWS services in the closed account.

#### Find and Terminate Active Resources

To avoid unexpected charges, before closing your account, we recommend that you review and terminate all resources currently running in the account.

1. Sign in to the AWS Management Console.
2. On the navigation bar, choose Services.
3. On the Services page, search for Resource Groups.
4. In Tag Editor, under Regions, select the regions where you have created resources, or choose All regions.
5. In Resource types, select All supported resource types.
6. Choose Search Resources. If search results appear, then there are still active resources on the account.

> **Note:**
> AWS Resource Groups search results don't show AWS Marketplace subscriptions. To manage subscriptions, see Managing your software.

You should archive your content and delete resources as appropriate. For additional guidance on how to retrieve your content, see the documentation for that service.

For more information, see [How do I check for active resources that I no longer need on my AWS account?](link-to-more-info)

#### Existing Content and Services Still in Use After Closing

After the post-closure period, AWS automatically deletes any remaining content in your AWS account and attempts to terminate any AWS services that are still in use. For more information about the post-closure period, see [Accessing your AWS account after you close it](link-to-more-info).

#### Your Payment Method

We charge you through your designated payment method for any usage fees incurred before you closed your AWS account. We issue any refunds that might be due through the same payment method. If you have active subscriptions (such as Reserved Instances that you pay for monthly), even after your account is closed, you might continue to be charged for the subscription through your designated payment method until the subscription expires or is sold according to the terms governing the subscription. These charges and refunds might occur after you close your account.

Additionally, if you reopen your account, you might be charged for the cost of running AWS services (that you didn't stop before closing your account) during the post-closure period. Closing your AWS account doesn't affect payment methods that you use on Amazon.com or other Amazon websites.

#### On-Demand Charges

During the post-closure period, billing for On-Demand charges stops. However, you will be billed for any usage that has accrued up until the time you closed your account. You'll be charged for that usage at the beginning of the next month. Additionally, if you purchased any subscriptions with ongoing payment obligations, you might continue to be charged for them after your account is closed.

> **Important:**
> You will continue to incur costs if you don't stop or delete your resources.

#### Domains Registered with Amazon Route 53

Domains that are registered with Route 53 are not deleted automatically. When you close your AWS account, you have three options:

1. You can disable automatic renewal, and the domains will be automatically deleted when the registration period expires. For more information, see [Enabling or Disabling Automatic Renewal for a Domain](link-to-more-info).

2. You can transfer the domains to another AWS account. For more information, see [Transferring a Domain to a Different AWS Account](link-to-more-info).

3. You can transfer the domains to another domain registrar. For more information, see [Transferring a Domain from Route 53 to Another Registrar](link-to-more-info).

If you have already closed the account, you can open a case with AWS Support to get help with disabling automatic renewal or transferring your domains. For more information, see [Contacting AWS Support About Domain Registration Issues](link-to-more-info). There is no charge to open a case for domain registration issues.

#### Charges if You Reopen Your AWS Account

If you reopen your AWS account during the post-closure period, you might be charged for the cost of any AWS services that weren't stopped or resources that weren't deleted before you closed your account.

> **Example:**
> You reopen your AWS account 30 days after closure. Your AWS account had only an active t2.micro Amazon EC2 instance at closure. In this example, imagine that the price for a t2.micro Amazon EC2 instance in your AWS Region is $0.01 per hour. In this case, you might be charged for 30 days x 24 hours x $0.01 per hour = $7.20 for your AWS services.

#### Cross-Account Access to the Account You're Closing

After you close your AWS account, any access requests to your closed account's AWS services from other AWS accounts will fail. This occurs even if you have granted the other accounts permission to access your account's AWS services. If you reopen your AWS account, other AWS accounts can again access your account's AWS services and resources if you granted the necessary permissions to the other AWS accounts.

#### Removing Amazon VPC Peering Connection

AWS doesn't delete Amazon Virtual Private Cloud (Amazon VPC) peering connections when you close one of the accounts participating in the VPC peering connection. Any traffic destined for the VPC peering connection originating from other active accounts is dropped because AWS terminates instances and deletes any security groups in the closed account. To remove the VPC peering connection, delete it from your account using the Amazon VPC console, AWS Command Line Interface (AWS CLI), or Amazon EC2 API. For more information, see [Deleting a VPC Peering Connection](link-to-more-info).

#### Troubleshooting Errors When Closing an AWS Account

If you receive an error message while trying to close your AWS account, you can contact your account representative or contact AWS Support to open a billing or account support case for assistance. Common reasons why you might not be able to close your AWS account include:

- Your account is the management account of an organization in AWS Organizations with active member accounts. To close the management account, you must first remove all member accounts from the organization.

- You have unpaid invoices for your account.

- You are not signed in to the account as the AWS account Root User.

- You are an active AWS Marketplace seller.

## How to Close Your AWS Account

### Minimum Permissions

To perform the following steps, you must have at least the following IAM permissions:

- You must sign in as the AWS account Root User, which requires no additional IAM permissions. You cannot perform these steps as an IAM user or role.

### Review Considerations Before Closing Your AWS Account

1. Sign in as the Root User of the account you want to close, using the email address and password associated with the account. Note that signing in as an AWS Identity and Access Management (IAM) user or role will not allow you to close an account.

2. On the navigation bar in the upper-right corner, select your account name (or alias), and then choose **Account**.

3. Scroll to the end of the Account page to the **Close Account** section. Make sure you read and understand the text next to the check boxes. Once you close an AWS account, you will no longer have access to AWS services using that account.

4. Select the check boxes to accept the terms, and then choose **Close Account**.

5. In the confirmation box, choose **Close Account**.

### Accessing Your AWS Account After Closure

After closing your AWS account, you will no longer have access to AWS services using that account. However, during the 90-day period following account closure (called the Post-Closure Period), you can:

- View past billing information for your AWS account.
- Access AWS Support.

During the Post-Closure Period, AWS may retain any content you didn't delete and any active AWS services. To access remaining content or AWS services, you can reopen your account within the Post-Closure Period.

### Reopening Your AWS Account

To reopen your AWS account, contact AWS Support. If you choose to reopen your account, you can access retained content and AWS services that were active before account closure. Note that you might incur charges for running these AWS services during the Post-Closure Period. Use the [AWS Pricing Calculator](https://calculator.aws/) to estimate these costs.

### After the Post-Closure Period

Once the Post-Closure Period ends, AWS will permanently close your AWS account. Any undeleted content will be permanently deleted, and any active AWS services will be stopped. Service attributes necessary for billing and administration purposes may be retained.

Please note that you cannot create a new AWS account using the same alias or email address that was registered to your closed AWS account.