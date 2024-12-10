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

2. On the **Overview** page, Scroll down and find for **Upgrade to new Defender CSPM plan** and select **Click here to upgrade**

   ![Microsoft Defender for Cloud](../images/task1.1.png)

1. You will be redirected to the **Getting started** page , now select the **Workspace name (1)**. Click on **Upgrade (2)**.

   ![Microsoft Defender for Cloud](../images/task1.2.png)

   >**Note:** You may need to wait for a few minutes for the upgrade to complete.

### Task 2: Get the status of the Defender coverage on the subscription and the workspace

1. Navigate back to Microsoft Defender for Cloud blade, and click on **Environment settings (1)** under **Management**. Expand **Azure (2)** to show the **Tenant Root Group** then expand **Tenant Root Group (3)** to show **Subscription**, and then expand **Subscription (4)** to show the **Workspace**. Notice the Defender coverage is **11/13 plans (5)** for the subscription and **2/2 plans (5)** for the workspace, meaning that you are now fully protected using Microsoft Defender for Cloud.

   ![Environment settings](../images/dfc2.png)

2. From the Environment settings, click on **Subscription**, and notice how the Microsoft Defender for Cloud plans are enabled.

   ![Environment settings](../images/dfc3.png)

3. Ensure that plans for **Servers** and **Databases (1)** are turned **On**. To check for **SQL servers on machines**, in databases, click on **Select types (2)** and make sure **Azure SQL Databases (3)** and **SQL servers on machines (4)** are toggled **On**.

   ![Environment settings](../images/defender1.1.png)

### Task 3: Configure Data Collection Settings Using Azure Monitor Agent (AMA) (Read Only)

1. Open **Azure Portal** and search for **Monitor(1)** and then click on it from the search results **(2)**.

   ![Microsoft Defender for Cloud](../images/task1-rd2.png)

1. On the Monitor menu in the Azure portal under **Settings (1)**, select **Data Collection Rules (2)**  > **Create(3)** to open the DCR creation page.

   ![Microsoft Defender for Cloud](../images/task1.3.png)

1. The Basic page includes basic information about the DCR, fill the following fields with the values and click on **Resources (6)** Tab.

   - **Rule Name:** Name for the DCR. The name should be something descriptive that helps you identify the rule **(1)**
   - **Subscription:** Select the Subscription from the drop-down **(2)**
   - **Resource group:** Select the Resource group named **lab-vm (3)** 
   - **Region:** Enter **West US (4)**
   - **Platform Type:** click on **All (5)**
  
   ![Microsoft Defender for Cloud](../images/task1-rd1.png)

1. The Resources page allows you to add VMs to be associated with the DCR. Select **+ Add resources** to select resources.

   ![Microsoft Defender for Cloud](../images/task1.4.png)

1. Under Subscription, expand Resource Groups and select the Virtual Machines that needs to be associated with Data Collection Rules and click on **Apply.** 

   ![Microsoft Defender for Cloud](../images/task1.61.png)

1. On the **Collect and deliver page (1)** click on **Add data source (2)** which allows you to add and configure data sources for the DCR and a destination for each.

   ![Microsoft Defender for Cloud](../images/task1.7.png)

1. On the **Data Source** Pane, Select a Data source type as **Windows Event Logs (1)** , choose **Basic (2)**, and then check all the fields **(3)** under Application, security , System and click on **Destination (4)**.

   ![Microsoft Defender for Cloud](../images/task1.8.png)

1. On the **Destination** Pane, Add one or more destinations for each data source. select **Azure Monitor Logs (1)** for destination type , choose the **Subscription (2)** from the drop-down, select your **Workspace (3)** from the destination details and then click on **Save (4)**

   ![Microsoft Defender for Cloud](../images/task1.9.png)

1. Review the settings on the **Review + Create** page to ensure that all configurations for the Data Collection Rule (DCR), including resources, data sources, and destinations, are accurate. Once confirmed, click **Create** to finalize the setup.

   ![Microsoft Defender for Cloud](../images/task1.10.png)

   >**Note:** Creating the DCR establishes a connection between the specified data sources and destinations. This ensures that the configured VMs automatically send the selected data (e.g., Windows Event Logs) to the specified Azure Monitor Logs workspace, facilitating centralized monitoring and analysis.

 ## Summary

In this lab, you have enabled Microsoft Defender for Cloud, received the status of the Defender coverage on the subscription and the workspace and configured the data collection settings in Microsoft Defender for Cloud.
 
 ### You have successfully completed the lab
