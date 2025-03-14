# Lab 05: Governance Rule

### Estimated Duration: 40 minutes

Governance rules can identify resources that require remediation according to specific recommendations or severities. Microsoft Defender for Cloud continuously assesses your hybrid and multi-cloud workloads and provides you with recommendations to harden your assets and enhance your security posture.
Central security teams often experience challenges when driving the personnel within their organizations to implement recommendations. 
The rule assigns an owner and due date to ensure the recommendations are handled. Many governance rules can apply to the same recommendations, so the rule with a lower priority value is the one that assigns the owner and due date. Governance rules will help:

- **Security teams**: Set accountability for recommendations, track their progress, and drive resource owners to action with notification capabilities.

- **Workload owners**: Focus on the specific recommendations that require their attention. They'll also be able to delegate recommendations to others or set expectations for when the recommendations will be implemented.

## Lab Objectives

In this lab, you will complete the following tasks:

- Task 1: Assign Governance Rule

### Task 1: Assign Governance Rule

1. From the **Defender for Cloud** menu, click on **Environment Settings (1)** page and click on **Governance rules (2)**.

   ![](../images/defender1.7.png)

1. Click on **+ Create governance rule**.

   ![](../images/m1-img20.png)

1. Enter **Rule name** as `asclab-rule` **(1)**, select **Scope** at subscription level **(2)** and **Priority** `100` **(3)**. Click **Next (4)**.

   ![](../images/m1-img21.png)
    
1. Under **conditions** provide the below details and click **Create (5)**
	
   - **By severity**: `High` **(1)**
   - **Owner**: `By email address` **(2)**
   - **Email address**: <inject key="AzureAdUserEmail"></inject> **(3)**
   - **Remediation timeframe**: `90 days` **(4)**

     ![](../images/m1-img22_new.png)

1. On the **Rule created successfully** pop-up select the check box next to **Apply rule to the 29 existing recommendations that are unassigned** and click on **OK**.

   ![](../images/a1.6.png)

   >**Note:** You might see a different pop-up where the existing recommendations count may vary.

1. Click on **Governance report** to view the status of tasks **Complete, Ontime and Unassign**.

   ![](../images/m1-img23.png)
    
   ![](../images/m1-img24.png)

## Validation

   > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
   > - Hit the Validate button for the corresponding task. You can proceed to the next task if you receive a success message.
   > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
   > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.

   <validation step="5f242815-a4bb-4a74-a4c1-b360304165fb" />

## Summary

In this lab, you have assigned Governance Rule.

### You have successfully completed the lab.
