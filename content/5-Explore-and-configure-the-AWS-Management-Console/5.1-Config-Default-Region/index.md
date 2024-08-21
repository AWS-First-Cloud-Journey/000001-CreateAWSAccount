+++
title = "Set Up Default Region"
date = 2024
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++

#### Set up Default Region

In this step, we will select a specific AWS Region to manage resources! With **Region** being a collection of AWS resources located in the same geographic area.

In the example in the image below, we are in Region Virginia (us-east-1)

![AWS Support](/images/5-console/5.1/1.1.png?width=90pc)

However, our customers are usually end users in Vietnam, so the nearest Region will be Singapore (ap-southeast-1) to reduce latency

#### Perform Region conversion

- Click on the triangle symbol in Region Virginia (us-east-1)

![AWS Support](/images/5-console/5.1/2.2.png?width=90pc)

- Select Region Singapore (ap-southeast-1)

![AWS Support](/images/5-console/5.1/3.3.png?width=90pc)

- The result displayed on the navigation bar is Region Singapore (ap-southeast-1)

![AWS Support](/images/5-console/5.1/4.png?width=90pc)

In addition, to ensure that we are always present in the correct Region that matches the organization's requirements every time we log in to the AWS console, setting up a default Region is essential.

#### Set Default Region

- Select the gear icon on the navigation bar

![AWS Support](/images/5-console/5.1/5.png?width=90pc)

- Select **More user settings**

![AWS Support](/images/5-console/5.1/6.png?width=90pc)

- Under **Localization and default Region** select **Edit**

![AWS Support](/images/5-console/5.1/7.png?width=90pc)

- Under **Default Region** select the triangle icon

![AWS Support](/images/5-console/5.1/8.png?width=90pc)

- Select **Asia Pacific (Singapore) ap-southeast-1**, select **Save settings**

![AWS Support](/images/5-console/5.1/9.png?width=90pc)

- Result:

![AWS Support](/images/5-console/5.1/10.png?width=90pc)

**Note:** setting up the default Region is very important, to avoid deploying services on other AWS Regions that are not in accordance with the original orientation

Congratulations, You have completed the lab