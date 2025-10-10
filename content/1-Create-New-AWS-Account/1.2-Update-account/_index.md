---
title: "Update Account"
date: "2025-10-05"
weight: 2
chapter: false
pre: " <b> 1.2 </b> "
---

#### Update Account Name, Email Address, or Password for Root User

#### Edit AWS Account Information 

To change your AWS account name, Root User password, or Root User email address, follow the steps below. Your email address and password are used as login credentials as the Root User of your AWS account.

> **Note:** Changes to your AWS account may take up to four hours to apply across all services.

#### Edit Account Name, Root User Password, or Email Address

**Minimum permissions required:**
To perform the following steps, you must have at least the following IAM permissions:

- You must sign in as the Root User of your AWS account. No additional IAM permissions are required. These steps cannot be performed by an IAM user or IAM role.

1. Sign in to the AWS Management Console using your AWS account's email address and password.

2. In the upper right corner of the console, click on your account name or account number, then select **Account**.

3. On the Account page, find **Account settings** and click **Edit**. You will be prompted to re-authenticate for security reasons.

   > **Note:** If the **Edit** option is not displayed, this indicates that you are not signed in as the Root User of your AWS account. Account settings cannot be modified when signed in as an IAM user or IAM role.

4. On the **Update Account Settings** page, select **Edit** next to the field you want to update.

   - For **Name**: On the **Update Your Account Name** page, enter the new account name in the **New account name** field, then click **Save changes**.

     > **Note:** If you encounter issues modifying the AWS account name, check whether there is a Service Control Policy (SCP) in AWS Organizations that restricts access to **aws-portal** or denies the **iam:UpdateAccountName** action.

   - For **Email**: On the **Update Your Email Address** page, provide the required information for **New email address**, **Confirm new email address**, and confirm your current password. Then, click **Save changes**. A verification code will be sent to your new email address from **no-reply@verify.signin.aws**. On the **Verify Your New Email Address** page, enter the verification code you received via email, then click **Save changes**.

     > **Note:** The verification code may take up to 5 minutes to receive. If you don't find the email in your inbox, remember to check your spam and junk folders.

   - For **Password**: On the **Update Your Password** page, fill in the fields for **Current password**, **New password**, and **Confirm new password**. Then, click **Save changes**. For additional guidance and best practices on Root User password management, refer to [Change the password for the AWS account Root User](link-to-documentation).

5. When you have completed all desired changes, select **Done**.

That's it! You've successfully updated your AWS account information.
