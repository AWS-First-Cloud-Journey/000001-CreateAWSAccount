---
title: "Create Admin Group and Admin User"
date: "2025-10-05"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

#### Create Admin Group

1. Sign in to AWS Management Console at [https://aws.amazon.com/](https://aws.amazon.com/)

2. Click on your account name in the upper right corner and select **My Security Credentials**

   ![Access Security Credentials](/images/01/0001.png)

   > **Note:** If you don't see the **My Security Credentials** menu, you can search for and select the **IAM** service to access the IAM console.

   ![Search for IAM service](/images/01/0002.png)

3. In the left navigation pane, select **User Groups** and click **Create Group**

   ![Create User Group](/images/01/0003.png)

4. In the **User group name** section, enter a group name (e.g., *AdminGroup*)

   ![Name User Group](/images/01/0004.png)

5. In the **Attach permissions policies** section, search for and select the **AdministratorAccess** policy. Then select **Create Group**

   ![Assign permissions](/images/01/0005.png)

6. The group has been created successfully

   ![Complete group creation](/images/01/0006.png)

#### Create Admin User

1. In the navigation pane, select **Users** and click **Add users**

   ![Create new User](/images/02/0001.png)

2. Configure user information:
   - Enter **User name** (e.g., *AdminUser*)
   - Select **AWS Management Console access**
   - Select **Programmatic access**
   - Select **Custom password** and enter a password
   - Uncheck **User must create a new password at next sign-in**
   - Click **Next: Permissions**

   ![Configure User](/images/02/0002.png)

3. Select the **Add user to group** tab and choose the **AdminGroup** you created

   ![Add user to group](/images/02/0003.png)

4. Click **Next: Tags** (Tags are optional for organizing and managing resources)

5. Click **Next: Review**

   ![Review information](/images/02/0004.png)

6. Review the information and select **Create user**

   ![Confirm user creation](/images/02/0005.png)

7. Download the .csv file containing the access key (if needed)

   ![Download credentials](/images/02/0006.png)

8. User has been created successfully

   ![Complete user creation](/images/02/0007.png)

9. View detailed user information

   ![User details](/images/02/0008.png)

> **Note:** After creating the user, AWS will display the access key ID and secret access key. This is important information for accessing AWS through AWS CLI and AWS SDK.

#### Sign in with Admin User

1. In the IAM console, select **Users** in the navigation pane
2. Select the IAM user you just created
3. In the **Security credentials** tab, copy the console sign-in link

   ![Copy sign-in link](/images/03/0001.png)

4. Open a new incognito tab and access the sign-in link

   ![Access via incognito tab](/images/03/0002.png)

5. Enter login information:
   - IAM user name
   - Password you created
   - Click **Sign in**

   ![Sign in IAM user](/images/03/0003.png)

6. Successfully signed in with IAM user

   ![Successful sign in](/images/03/0004.png)

#### Reference Documentation

#### IAM User and AWS Sign-in

An IAM user is an entity created within an AWS account that has permissions to interact with AWS resources. IAM users can sign in using:
- Account ID/alias
- User name
- Password

User names can be regular names (*zhang*) or email addresses (*zhang@example.com*), cannot contain spaces but can contain:
- Uppercase and lowercase letters
- Numbers
- Special characters: + = , . @ _ -

#### Create Access Key for Root User

#### Required Permissions

- Must sign in as root user (cannot be performed with IAM user or role)

#### Steps to Perform

1. Sign in to AWS Management Console using the root user's email and password

2. Click on the account name in the upper right corner, select **Security Credentials**

3. In the **Access keys** section, select **Create access key**

   > **Note:** If you don't see this option, you may have reached the access key limit. You need to delete an existing key before creating a new one.

4. On the **Alternatives to root user access keys** page, read the security recommendations. Check the checkbox and select **Create access key**

5. On the **Retrieve access key** page:
   - Access key ID will be displayed
   - Click **Show** to view the Secret access key
   - Copy and save both Access key ID and Secret key in a secure location
   - Or download the rootkey.csv file to save the information

6. Click **Done** to complete

> **Recommendation:** Delete or deactivate access keys when no longer in use to ensure security.

#### Delete Access Key for Root User

#### Required Permissions

- Must sign in as root user (cannot be performed with IAM user or role)

#### Steps to Perform

1. Sign in to AWS Management Console as root user

2. Click on the account name in the upper right corner, select **Security Credentials**

3. In the **Access keys** section, find the key to delete:
   - Click **Delete** in the **Actions** menu to permanently delete
   - Or click **Deactivate** to temporarily disable

4. In the confirmation dialog:
   - Enter the Access key ID to confirm
   - Click **Delete** to complete

> **Note about deactivating keys:**
> - Deactivated keys can be reactivated later
> - No need to change ID and Secret
> - API calls using deactivated keys will be rejected with "access denied" error

**Best Practices:**
- Limit use of root user access keys
- Create IAM users with appropriate permissions instead of using root user
- Always secure access key information
- Delete or deactivate unused keys
- Regularly rotate access keys
- Use AWS CloudTrail to monitor access key activity

#### Multi-Factor Authentication (MFA) Details

When MFA is enabled, users need to:
- Sign in normally with username/password
- Enter authentication code from MFA device

AWS supports these MFA device types:
- Virtual MFA (Google Authenticator, Authy)
- Hardware MFA token
- U2F security key

> **Recommendation:** Enable MFA for both root user and IAM users to enhance security.

Additional References:
- [IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [AWS Security Best Practices](https://aws.amazon.com/security/security-learning/)
- [AWS CloudTrail Documentation](https://docs.aws.amazon.com/cloudtrail/)