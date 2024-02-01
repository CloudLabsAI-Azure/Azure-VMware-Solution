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

   ![](../media/image11.png)

1. Select **Machines** under **Infrastructure** section from the left pane, and select **WinDev2401Eval** machine from the list.
 
   ![](../media/image11.png)

1. On **WinDev2401Eval** machine page, select **Extensions** under settings.

   ![](../media/image11.png)

1. On **Install extension** page, search and select **Log Analytics Agent - Azure Arc (on a deprecation path)** and click on **Next**

   ![](../media/image11.png)

1. On **Configure Log Analytics Agent - Azure Arc (on a deprecation path) extension** page, enter the Workspace ID and Primary key copied for the workspace id and workspace key respectively and click on **Review + create**

   ![](../media/image11.png)

1. Click on **Create**. Wait for the deployment to get succeeded.

1. Once the deployment get succeeded, navigate to the Log Analytics workspce which was created earlier and select **Logs** from the left pane and close the query window pop-up and enter the below query and click on **Run** to verify the log analytics connectivity with the machine.

```
 Heartbeat
  | where OSType =="Windows"
  | distinct computer
```
1. In the **Results** window, the **WinDev2401Eval** entry is listed, indicating the machine is connected to Log Analytics workspace.

