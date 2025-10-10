---
title: "View AWS Account Identifiers"
date: "2025-10-05"
weight: 1
chapter: false
pre: " <b> 1.1 </b> "
---

#### Finding Account ID when signed in as Root User

You can find the AWS account ID using either the **AWS Management Console** or the **AWS Command Line Interface (AWS CLI)**. In the console, the location of the account ID depends on whether you're signed in as the Root User or an IAM User. The account ID remains the same regardless of how you sign in.

##### Minimum Permissions

To perform the following steps, you must have at least the following IAM permissions:

- When you sign in as the Root User, you don't need any IAM permissions.
- In the navigation bar on the upper right, choose your account name or number and then choose **Security credentials**.

> **Tip:** If you don't see the **Security credentials** option, you might be signed in as a federated user with an IAM role, instead of as an IAM user. In this case, look for the entry **Account** and the account ID number next to it.

Under the **Account details** section, the account number appears next to **AWS account ID**.

#### Finding AWS Account ID as an IAM User

##### Minimum Permissions

To perform the following steps, you must have at least the following IAM permission:

- `aws-portal:ViewAccount`

1. In the navigation bar on the upper right, choose your user name and then choose **Security credentials**.

   > **Tip:** If you don't see the **Security credentials** option, you might be signed in as a federated user with an IAM role, instead of as an IAM user. In this case, look for the entry **Account** and the account ID number next to it.

2. At the top of the page, under **Account details**, the account number appears next to **AWS account ID**.


#### Find the Canonical User ID for your AWS Account

You can find the canonical user ID for your AWS account using the AWS Management Console or the AWS CLI. The canonical user ID for an AWS account is unique to that account. You can retrieve the canonical user ID for your AWS account as the Root User, a federated user, or an IAM User.

#### Find the Canonical ID as Root User or IAM User

To find the canonical user ID for your account when signed in to the console as the Root User or IAM User:

##### Minimum Permissions

To perform the following steps, you must have at least the following IAM permissions:

- When you run the command as the Root User, you don't need any IAM permissions.
- When you sign in as an IAM User, you must have:
  - `aws-portal:ViewAccount`

1. Sign in to the AWS Management Console as the Root User or IAM User.
2. In the navigation bar on the upper right, choose your account name or number, and then choose **Security credentials**.

   > **Tip:** If you don't see the **Security credentials** option, you might be signed in as a federated user with an IAM role, instead of as an IAM user. In this case, look for the entry **Account** and the account ID number next to it.

3. Under the **Account details** section, the canonical user ID appears next to **Canonical user ID**. You can use your canonical user ID to configure Amazon S3 access control lists (ACLs).

#### Find the Canonical ID as a Federated User with IAM Role

To find the canonical ID for your account when signed in to the console as a federated user with an IAM Role:

##### Minimum Permissions

You must have permission to list and view Amazon S3 buckets.

1. Sign in to the AWS Management Console as a federated user with an IAM Role.
2. In the Amazon S3 console, choose a bucket name to view details about that bucket.
3. Choose the **Permissions** tab.
4. In the **Access control list** section, under **Bucket owner**, the canonical ID for your AWS account will appear.
