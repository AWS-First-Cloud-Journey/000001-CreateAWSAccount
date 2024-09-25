---
title : "Creating Support Cases and Case Management in AWS"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---


#### Creating Support Cases and Case Management in AWS

This guide covers how to create and manage support cases in AWS, including various case types, severity levels, and the process for handling different support requests.

#### Types of Support Cases in AWS

In the AWS Management Console, you can create three types of customer support cases:

1. **Account and Billing Support**
   - Available to all AWS customers for billing and account-related inquiries.

2. **Service Limit Increases**
   - Available to all AWS customers. For more information on default service quotas (limits), see the [AWS service quotas](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) documentation.

3. **Technical Support Cases**
   - Available to customers on Developer, Business, Enterprise On-Ramp, or Enterprise Support plans. Not available for Basic Support plans.

**Notes:**
- To change your support plan, see [Changing AWS Support Plans](https://docs.aws.amazon.com/premiumsupport/latest/user/change-support-plan.html).
- For account closure, refer to [Closing an Account](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/close-account.html).
- For common troubleshooting topics, check the [Troubleshooting resources](https://aws.amazon.com/premiumsupport/knowledge-center/).

#### How to Create a Support Case

1. Sign in to the [AWS Support Center](https://console.aws.amazon.com/support/home#/).
   
   **Tip:** In the AWS Management Console, click the question mark icon ( ? ) and select **Support Center**.

2. Choose **Create case**.

3. Select the case type:
   - **Account and billing**
   - **Technical**
   - For service quota increases, select **Looking for service limit increases?** and follow the instructions.

4. Select the **Service**, **Category**, and **Severity** level.
   
   **Tip:** AWS provides recommended solutions for commonly asked questions.

5. Provide the following details:
   - **Subject:** Title for your case.
   - **Description:** Describe the issue including error messages, troubleshooting steps, and how you're accessing the service (Console, CLI, API).
   - (Optional) **Attach files**: Add error logs, screenshots, etc., up to 3 files (maximum 5 MB each).

6. Choose **Next step: Solve now or contact us**.

7. On the **Contact us** page, select your preferred language and contact method:
   - **Web**: Reply in Support Center.
   - **Chat**: Live chat with a support agent.
   - **Phone**: Receive a call from a support agent (enter country, phone number, and optional extension).

**Notes:**
- Contact options depend on the case type and support plan.
- You can discard a support case draft by selecting **Discard draft**.
- For Business, Enterprise On-Ramp, or Enterprise plans, additional contact options allow you to notify others of status changes.

8. Review your case details and select **Submit**. The case ID and summary will be displayed.

#### Describing Your Issue

Provide as much detail as possible, including relevant AWS resources, timestamps, logs, and environment descriptions to increase the chances of a quick resolution.

#### Severity Levels and Response Times

Choose severity levels based on the impact on your applications. Higher severities are for critical issues with no workarounds.

| Severity                   | Severity Code | First Response Time | Description (Support Plans)                                                                                                                                             |
|----------------------------|---------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| General guidance            | Low           | 24 hours            | General development questions or feature requests (*Developer, Business, Enterprise On-Ramp, Enterprise Support*)                                                        |
| System impaired             | Normal        | 12 hours            | Non-critical functions behaving abnormally (*Developer, Business, Enterprise On-Ramp, Enterprise Support*)                                                               |
| Production system impaired  | High          | 4 hours             | Important application functions are impaired or degraded (*Business, Enterprise On-Ramp, Enterprise Support*)                                                            |
| Production system down      | Urgent        | 1 hour              | Significant business impact, important functions unavailable (*Business, Enterprise On-Ramp, Enterprise Support*)                                                        |
| Business-critical system down | Critical      | 15 minutes          | Critical business functions unavailable (*Enterprise Support*), 30 minutes for *Enterprise On-Ramp Support*                                                             |

**Note:** Severity codes cannot be changed after creating a case. If your situation changes, work with the AWS Support agent.

#### Response Times and Support Hours

AWS aims to respond within the specified timeframes for each severity level. For Business, Enterprise On-Ramp, or Enterprise Support, 24/7 access is available. Developer Support response times are calculated in business hours (typically 8:00 AM - 6:00 PM local time, excluding weekends and holidays).

For details on AWS Support features, see the [AWS Support features](https://aws.amazon.com/premiumsupport/features/) page.

#### Multilingual Support

AWS offers support in various languages for different support levels:

- **Japanese**: 24/7 technical support for Business, Enterprise On-Ramp, and Enterprise plans. Developer support available during Japanese business hours.
- **Chinese**: 24/7 technical support for Business, Enterprise On-Ramp, and Enterprise plans. Developer support available during Chinese business hours.
- **Korean**: 24/7 technical support for Business, Enterprise On-Ramp, and Enterprise plans. Developer support available during Korean business hours.

