---
title: "Hardware MFA Device"
date: "2025-10-05"
weight: 3
chapter: false
pre: " <b> 2.3 </b> "
---

**Content**

- [Enable Other Hardware MFA Device through Console](#enable-other-hardware-mfa-device-through-console)

#### Enable Other Hardware MFA Device through Console

1. Sign in to the AWS Console.
2. In the upper right corner, you will see your account name, select it and choose **My Security Credentials** then expand Multi-factor authentication (MFA).

![Image](/images/1-account-setup/MySecurity_v1.png?width=15pc)

3. To manage hardware MFA devices, you must have permissions from the following permission set. In the left sidebar, select **Policies** then select **Create policy**, select **JSON** tab and paste the following:


```js
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowManageOwnUserMFA",
            "Effect": "Allow",
            "Action": [
                "iam:DeactivateMFADevice",
                "iam:EnableMFADevice",
                "iam:GetUser",
                "iam:ListMFADevices",
                "iam:ResyncMFADevice"
            ],
            "Resource": "arn:aws:iam::*:user/${aws:username}"
        },
        {
            "Sid": "DenyAllExceptListedIfNoMFA",
            "Effect": "Deny",
            "NotAction": [
                "iam:EnableMFADevice",
                "iam:GetUser",
                "iam:ListMFADevices",
                "iam:ResyncMFADevice"
            ],
            "Resource": "arn:aws:iam::*:user/${aws:username}",
            "Condition": {
                "BoolIfExists": {
                    "aws:MultiFactorAuthPresent": "false"
                }
            }
        }
    ]
}
```
![MFA](/images/3/0001.png?featherlight=false&width=90pc)

4. Select **Next: Tags**. This is the **Tags** screen, a tool used to differentiate AWS resources.
5. Select **Next: Review**. This is the screen that allows you to review the permission set you are creating.
6. Enter the permission set name (e.g., MFAHardDevice) and select **Create policy**.

![MFA](/images/3/0002.png?featherlight=false&width=90pc)

![MFA](/images/3/0003.png?featherlight=false&width=90pc)

7. In the left sidebar, select **Dashboard** and then select **Enable MFA**.

![MFA](/images/3/0004.png?featherlight=false&width=90pc)

8. Expand Multi-factor authentication (MFA) then select **Active MFA**.

9. In **Manage MFA Device**, select **Other Hardware MFA Device** then press **Continue**.
10. Enter the **Serial Number** found on the back of the device.

![Image](/images/1-account-setup/HardwareMFA.png?featherlight=false&width=90pc)

11. Enter MFA code 1, then wait 30 seconds and enter MFA code 2.
12. Select **Assign MFA**.