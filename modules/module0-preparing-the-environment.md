# Lab 01: Preparing the Environment

### Estimated Duration: 10 minutes

## Lab Scenario

You are a cloud security administrator tasked with securing your organization's Azure environment. This lab provides a hands-on experience in enhancing cloud security using Microsoft Defender for Cloud. You will enable Microsoft Defender for Cloud, assess the status of Defender coverage across their subscription and workspace, and configure data collection settings to optimize security monitoring. This lab ensures that you can effectively manage and secure your cloud environments.

## Lab objectives
In this lab, you will complete the following tasks:

- Task 1: Enabling Microsoft Defender for Cloud (Read-Only)
- Task 2: Get the status of the Defender coverage on the subscription and the workspace
- Task 3: Configure the data collection settings in Microsoft Defender for Cloud (Read Only)

### Task 1: Enabling Microsoft Defender for Cloud (Read-Only)

1. Open **Azure Portal** and search for **Microsoft Defender for Cloud (1)** and then click on it from the search results **(2)**.

   ![Microsoft Defender for Cloud](../images/M0-T1-S1.2.png)   

2. Click on the **Getting started (1)** page from the left pane, from the **Upgrade (2)** tab, select the **Workspace name (3)**. Click on **Upgrade (4)**.

   >**Note:** You may need to wait for a few minutes for the upgrade to complete.

   ![Template deployment completed](../images/dfc1.png)

### Task 2: Get the status of the Defender coverage on the subscription and the workspace

1. Navigate back to Microsoft Defender for Cloud blade, and click on **Environment settings (1)**. Expand **Azure (2)** to show the **Tenant Root Group** then expand **Tenant Root Group (3)** to show **Subscription**, and then expand **Subscription (4)** to show the **Workspace**. Notice the Defender coverage is **11/13 plans (5)** for the subscription and **2/2 plans (5)** for the workspace, meaning that you are now fully protected using Microsoft Defender for Cloud.

   ![Environment settings](../images/dfc2.png)

2. From the Environment settings, click on **Subscription**, and notice how the Microsoft Defender for Cloud plans are enabled.

   ![Environment settings](../images/dfc3.png)

3. Ensure that plans for **Servers** and **Databases (1)** are turned **On**. To check for **SQL servers on machines**, in databases, click on **Select types (2)** and make sure **Azure SQL Databases (3)** and **SQL servers on machines (4)** are toggled **On**.

   ![Environment settings](../images/defender1.1.png)

### Task 3: Configure the data collection settings in Microsoft Defender for Cloud (Read Only)

1. Go back to the **Environment settings** in the sidebar and drill down into your **Subscription**.

   ![Environment settings](../images/dfc3.png)

2. Navigate to **Settings and monitoring (1)**.

   ![Auto-provisioning](../images/M0-T3-S2.2.png)

3. On the **Settings and monitoring - Extensions** page, set **Log Analytics agent (1)** to **On (2)** (if it's not already set to On). Then 
 click on **Edit configuration (3)** under the configuration column.

   ![Auto-provisioning](../images/M0-T3-S3.png)

5. On the workspace configuration section, in the **Custom workspace** option, verify your workspace **asclab-xxxxx (1)** is present. Click on **Apply (2)** and **Continue**.

   ![Enable Microsoft Defender for Cloud on the workspace level](../images/defender1.3.png)

8. Click on **Save**.

   ![Enable Microsoft Defender for Cloud on the workspace level](../images/M0-T3-S5.1.png)

 ## Summary

In this lab, you have enabled Microsoft Defender for Cloud, received the status of the Defender coverage on the subscription and the workspace and configured the data collection settings in Microsoft Defender for Cloud.
 
 ### You have successfully completed the lab
