---
title: "Virtual MFA Device"
date: "2025-10-05"
weight: 1
chapter: false
pre: " <b> 2.1 </b> "
---

#### Introduction

AWS account security is one of the most important factors to protect your cloud resources. Multi-Factor Authentication (MFA) provides an additional layer of security beyond regular login credentials. This document guides you through setting up a virtual MFA device for your AWS account.

#### Overview of MFA in AWS

MFA requires users to provide two or more authentication factors when signing in:
- Login credentials (username and password)
- Authentication code from a registered MFA device

#### Requirements

> **Note**: To enable MFA, you need to sign in to AWS using the root account.

#### Types of MFA Devices Supported by AWS

AWS supports various types of MFA devices:
- Authenticator apps
- FIDO security keys
- Hardware token devices

#### Setting Up Virtual MFA Device

##### Step 1: Sign in to AWS Management Console

1. Go to [AWS Console](https://aws.amazon.com/console/)
2. Sign in with your account credentials

##### Step 2: Access Security Settings

1. In the upper right corner of the screen, click on your account name
2. Select **My Security Credentials** from the dropdown menu

![Access security settings](/images/2/0001.png?featherlight=false&width=90pc)

##### Step 3: Set Up MFA

1. On the Security Credentials page, expand the **Multi-factor authentication (MFA)** section
2. Click **Assign MFA**

![Set up MFA](/images/2/0002.png?featherlight=false&width=90pc)

##### Step 4: Select MFA Device Type

1. In the **Select MFA device** interface:
   - Enter a name for your MFA device
   - Select **Authenticator app** as the MFA device type
   - Click **Next**

![Select MFA device type](/images/2/0003.png?featherlight=false&width=90pc)

##### Step 5: Install Authenticator App

1. Install an authenticator app on your mobile device or browser
   - List of [AWS-compatible MFA apps](https://aws.amazon.com/iam/features/mfa/?audit=2019q1)

![Install authenticator app guide](/images/2/0004.png?featherlight=false&width=90pc)

##### Step 6: Install Authenticator on Chrome (Optional)

If you want to use an authenticator app on Chrome browser:

1. Go to [Authenticator on Chrome Web Store](https://chrome.google.com/webstore/detail/authenticator/bhghoamapcdpbohphigoooaddinpkbai)
2. Click **Add to Chrome** to install

![Install Authenticator on Chrome](/images/2/0005.png?featherlight=false&width=90pc)

##### Step 7: Scan QR Code

1. Use the installed authenticator app to scan the QR code displayed on the AWS screen

![Scan QR code](/images/2/0007.png?featherlight=false&width=90pc)

##### Step 8: Confirm Setup

1. After scanning the QR code, the authenticator app will start generating codes
2. Enter two consecutive authentication codes in the corresponding fields on AWS
3. Click **Add MFA**

![Enter authentication codes](/images/2/0008.png?featherlight=false&width=90pc)

##### Step 9: Complete Setup

1. Confirm the request to add the MFA device

![Complete setup](/images/2/0009.png?featherlight=false&width=90pc)

##### Step 10: Confirm Success

1. After completion, you will see a confirmation message that MFA setup was successful

![MFA setup successful](/images/2/00010.png?featherlight=false&width=90pc)

#### Using MFA

From the next login onwards, after entering your login credentials, you will be prompted to enter an authentication code from your registered MFA device.

#### Troubleshooting

- **Lost MFA device**: Contact AWS Support for assistance in recovering access
- **Authentication code not working**: Ensure your device has accurate time synchronization

#### Reference Documentation

- [AWS IAM MFA Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa.html)
- [AWS Security Best Practices](https://aws.amazon.com/architecture/security-identity-compliance/)