+++
title = "Configure Default Region"
date = 2024
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++

#### Set up Default Region

In this step, we will select a specific AWS Region to manage resources! A **Region** is a collection of AWS resources located in the same geographic area.

In the example shown in the image below, we are currently in the Virginia Region (us-east-1)

![AWS Support](/images/5-console/5.1/1.1.png?width=90pc)

However, since our customers are typically end users in Vietnam, the nearest Region would be Singapore (ap-southeast-1) to reduce latency

#### Perform Region Switch

- Click on the triangle symbol next to Region Virginia (us-east-1)

![AWS Support](/images/5-console/5.1/2.2.png?width=90pc)

- Select Region Singapore (ap-southeast-1)

![AWS Support](/images/5-console/5.1/3.3.png?width=90pc)

- The result shows on the navigation bar that we are now in Region Singapore (ap-southeast-1)

![AWS Support](/images/5-console/5.1/4.png?width=90pc)

Additionally, to ensure that we are always in the correct Region that matches the organization's requirements every time we log in to the AWS console, setting up a default Region is essential.

#### Configure Default Region

- Click on the gear icon on the navigation bar

![AWS Support](/images/5-console/5.1/5.png?width=90pc)

- Select **More user settings**

![AWS Support](/images/5-console/5.1/6.png?width=90pc)

- In the **Localization and default Region** section, select **Edit**

![AWS Support](/images/5-console/5.1/7.png?width=90pc)

- In the **Default Region** section, click on the triangle icon

![AWS Support](/images/5-console/5.1/8.png?width=90pc)

- Select **Asia Pacific (Singapore) ap-southeast-1**, then select **Save settings**

![AWS Support](/images/5-console/5.1/9.png?width=90pc)

- Result:

![AWS Support](/images/5-console/5.1/10.png?width=90pc)

**Note:** Setting up the default Region is very important to avoid accidentally deploying services in other AWS Regions that do not align with your initial planning.

Congratulations! You have completed the lab.