+++
title = "AWS Account Setup"
date = 2024
weight = 1
chapter = false
+++

# AWS Account Setup
This document provides detailed guidance on the AWS account setup process from the beginning, including account creation, security configuration, and administrative access setup. This guide helps you start using AWS safely and effectively.

## Table of Contents
- [Create your first AWS account](#create-your-first-aws-account)
- [Set up MFA for Root account](#set-up-mfa-for-root-account)
- [Create Administrator Group and Administrator User](#create-administrator-group-and-administrator-user)
- [Account verification support](#account-verification-support)
- [Explore AWS Management Console](#explore-aws-management-console)

## Create your first AWS account

### Overview
In this section, you will create a new **AWS account**, set up **MFA** (Multi-factor Authentication) to protect your account. Next, you will create an **Administrator Group** and **Administrator User** to manage AWS resources instead of using the root account. Finally, if you encounter issues during verification, you will be guided to contact **AWS Support**.

### Basic Concepts

#### AWS Account
An **AWS Account** is the means to access and use AWS services. Each account has a default **root user** with unrestricted administrative privileges. When you first sign in, you will use this root user account.

> **Note**: AWS recommends not using the root user for daily tasks. Instead, create IAM Users with appropriate administrative permissions to minimize security risks.

#### MFA (Multi-factor Authentication)
**MFA** is an advanced security feature for AWS accounts. When activated, you will need to enter an OTP (One-time Password) code each time you sign in to your AWS account, creating a second layer of protection beyond your regular password.

#### IAM Group
**IAM Group** is AWS's user management tool that allows you to group multiple IAM Users together. All IAM Users in the same group will inherit the permissions assigned to that group, making permission management easier.

#### IAM User
**IAM User** is a user entity in AWS. Each IAM User has their own login credentials and is granted specific access permissions to AWS resources. IAM Users are suitable for providing **long-term** access for people or applications that need to access AWS.

#### AWS Support
**AWS Support** is AWS's customer support service unit that helps resolve technical issues and provides account verification support.

#### AWS Management Console
**AWS Management Console** is a web interface that allows you to manage and interact with AWS services visually.

## Main Content

### Creating an AWS Account

#### Step 1: Access the AWS registration page
1. Open a web browser and go to [aws.amazon.com](https://aws.amazon.com)
2. Click the **Create an AWS Account** button in the upper right corner of the page

#### Step 2: Fill in account information
1. Enter your email address
2. Create an AWS account name
3. Click **Verify email address** and verify your email

#### Step 3: Create password
1. Create a strong password for your AWS account
2. The password must meet the following requirements:
   - Minimum 8 characters, maximum 128 characters
   - Include at least one uppercase letter (A-Z)
   - Include at least one lowercase letter (a-z)
   - Include at least one number (0-9)
   - Include at least one special character (!@#$%^&*()_+-=[]{}|;':\",./<>?)

#### Step 4: Fill in contact information
1. Choose account type (Personal or Business)
2. Fill in complete personal or business information
3. Read and accept the AWS Customer Agreement

#### Step 5: Fill in payment information
1. Enter valid credit card information
2. Note: AWS will perform a small authorization hold to verify your card

#### Step 6: Verify identity
1. Enter your mobile phone number
2. Choose verification method (SMS or voice call)
3. Enter the verification code sent to your phone

#### Step 7: Choose support plan
1. Select an appropriate AWS support plan (Basic, Developer, Business, or Enterprise)
2. Basic plan is free and suitable for beginners

#### Step 8: Complete the registration process
1. Click the **Complete sign up** button
2. Wait for confirmation email from AWS (may take a few minutes to several hours)
3. After receiving the confirmation email, you can sign in to the AWS Management Console

### Set up MFA for Root Account

#### Step 1: Sign in to AWS Management Console
1. Go to [console.aws.amazon.com](https://console.aws.amazon.com)
2. Sign in with your root account email and password

#### Step 2: Access account management page
1. Click on your account name in the upper right corner
2. Select **My Security Credentials** from the dropdown menu

#### Step 3: Set up MFA
1. Expand the **Multi-factor authentication (MFA)** section
2. Click **Activate MFA**
3. Choose MFA device type:
   - **Virtual MFA device**: Use authenticator apps like Google Authenticator
   - **Hardware TOTP token**: Use dedicated hardware devices
   - **Security key**: Use FIDO security keys

#### Step 4: Configure MFA for virtual device (most common)
1. Install an authenticator app on your phone (Google Authenticator, Authy, Microsoft Authenticator, etc.)
2. Click **Show QR code** and scan the QR code with your authenticator app
3. Enter two consecutive authentication codes from the authenticator app
4. Click **Assign MFA**

#### Step 5: Backup MFA information
1. Save the QR code or secret key provided during setup
2. Store this information securely in case you lose your device

### Create Administrator Group and Administrator User

#### Step 1: Access IAM service
1. Sign in to AWS Management Console with root account
2. Search for "IAM" in the service search bar
3. Select **IAM** (Identity and Access Management) service

#### Step 2: Create Admin Group
1. In the IAM dashboard, click **User groups** in the left menu
2. Click the **Create group** button
3. Enter a name for the group (e.g., "Administrators")
4. Find and select the **AdministratorAccess** policy in the policies list
5. Click **Create group** to complete

#### Step 3: Create Admin User
1. In the IAM dashboard, click **Users** in the left menu
2. Click the **Add users** button
3. Enter username (e.g., "AdminUser")
4. Select **AWS Management Console access** in the Access type section
5. Configure password:
   - Choose **Custom password** and enter a strong password
   - Uncheck "User must create a new password at next sign-in" if you don't want to change the password on first login

#### Step 4: Add User to Admin Group
1. On the "Add user to group" page, select the Administrators group created in the previous step
2. Click **Next: Tags**
3. (Optional) Add tags if needed
4. Click **Next: Review**
5. Review the information and click **Create user**

#### Step 5: Save login information
1. Download or copy the login information (including sign-in URL, username, and password)
2. Store this information securely

#### Step 6: Set up MFA for Admin User
1. Return to the Users list in IAM
2. Select the username you just created
3. Select the **Security credentials** tab
4. In the **Multi-factor authentication (MFA)** section, click **Assign MFA device**
5. Follow the same steps as when setting up MFA for the root account

### Account verification support

#### Common issues when verifying accounts
1. Not receiving confirmation email
2. Credit card not accepted
3. Identity verification failed
4. Unable to sign in after registration

#### Contact AWS Support
1. Go to [aws.amazon.com/support](https://aws.amazon.com/support)
2. Click **Create case**
3. Select **Account and billing support** support type
4. Fill in complete information about your issue
5. Click **Submit** to send the support request

### Explore AWS Management Console

#### Overview of AWS Management Console
1. Top navigation bar:
   - Services menu: Quick access to AWS services
   - Search bar: Search for services, documentation, and resources
   - Region: Select AWS region to work in
   - Account: Manage account settings and sign out
   - Support: Access documentation and support

#### Basic AWS services for beginners
1. **EC2**: Virtual servers
2. **S3**: Object storage
3. **RDS**: Relational databases
4. **Lambda**: Serverless computing
5. **CloudWatch**: Monitoring and logging

#### Personalizing AWS Management Console
1. Create custom homepage:
   - Click **Edit** in the upper right corner of the console homepage
   - Add, remove, or rearrange widgets as needed
   - Click **Save** to save changes

2. Create bookmarks for frequently used services:
   - Click the star next to the service name in the services menu
   - Bookmarked services will appear in the **Recently visited services** section

## Reference Documentation
- [AWS Identity and Access Management](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
- [AWS Security Best Practices](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
- [AWS Support Plans](https://aws.amazon.com/premiumsupport/plans/)
- [Getting Started with AWS](https://aws.amazon.com/getting-started/)