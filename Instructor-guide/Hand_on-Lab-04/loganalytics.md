### Task 1: Create a Log Analytics Workspace

In this task, you will create a Log Analytics workspace for to store the log information and analysing the machines onboarded through Azure Arc.

1. In the Search bar of the Azure portal, type **Log Analytics**, then select **Log Analytics workspaces**.
   
   ![](../media/image8.png)

1. Select **+ Create** from the command bar.
    
   ![](../media/image9.png)

1. Select Resource Group from the drop down(avs-rg).

1. For the Name, enter something unique like **log-analytics-ws-avs**.

1. Select the default Region 

1. Select **Review + Create**.

   ![](../media/image10.png)

1. Once the workspace validation has passed, select **Create**. Wait for the new workspace to be provisioned, this may take a few minutes.

   ![](../media/image11.png)

1. Once the deployment got succeeded, Click on **Go to resource** and click on **Agents** under Settings section.

   ![](../media/image11.png)

1. On **log-analytics-ws-avs | Agents page**, expand **Log Analytics agent instructions** copy the **Workspace ID(1)** and **Primary key(2)** in notepad you needs this values in upcoming steps.

   ![](../media/image11.png)

1. On Azure Portal page, in Search resources, services and docs (G+/) box at the top of the portal, enter **Azure Arc**, and then select **Azure Arc** under services.


