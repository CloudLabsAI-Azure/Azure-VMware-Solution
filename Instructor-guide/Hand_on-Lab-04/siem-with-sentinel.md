### Task 1: Create Sentinel Workspace

In this task, you will create Microsoft Sentinel workspace where you will be monitoring and analyzing security events.

1. On Azure Portal page, in **Search resources, services and docs (G+/)** box at the top of the portal, enter **Microsoft Sentinel**, and then select **Microsoft Sentinel** under services.

    ![Picture 1](../media/image_7.png)

1. From the list of workspaces available, select the **log-analytics-ws-avs** workspace and click on **Add**.

1. Once the workspace is added, the Microsoft Sentinel | News & guides page will display., including that the Microsoft Sentinel free trial is activated. Select **OK**  Note the three steps listed on the Get started page.

### Task 2: Ingesting data to Sentinel from Windows security event connector.

1. From the **Microsoft Sentinel** blade, from left menu select **Content hub(1)** under **Content management** section.

1. On the content hub page search for **Windows Security Events(2)** and select, **Install(3)**.

     ![Picture 1](../media/14s1.png)
   
1. Once you receive the notification of successful installation go back to the Data connector page and click on refresh

1. You can see **Security events Via Legacy agent** and **windows security events via AMA**

1. Select **Security events Via Legacy agent(1)** and click on **open connector page(2)**.

    ![Picture 1](../media/14s2.png)
   
1. Under configuration choose **Install agent on non Azure Windows Machine(1)** and select **Download & install agent for non Azure Windows machines(2)**  

1. On the **log-analytics-workspace | Agent Management** page, notice that windows machine is already connected via Log analytics windows agent (legacy).

1. Navigate back to the **Security Events via legacy agent** configuration page, scroll down a bit you can find **Select which events to stream** Click on **All Events**
 
1. Click on **Apply changes** now if you refresh the data connector page you can see the status connected for **Security events Via Legacy agent**.

### Task 3: Ingesting data to Sentinel from Microsoft Defender for cloud

1. From the **Microsoft Sentinel** blade, from left menu select **Content hub(1)** under **Content management** section.

1. On the content hub page search for **Microsoft Defender for cloud** and select, **Install(3)**.

1. Once Installed, you will find below two data connectors listed in the Data Connector page.
      * Tenant-based Microsoft Defender for Cloud (Preview) : It allows you to collect Defender for Cloud alerts over your entire tenant, without having to enable each subscription separately.
      * Subscription-based Microsoft Defender for Cloud (Legacy) :  It allows you to collect Defender for Cloud alerts per subscription.

     ![Picture 1](../media/s41.png)
1. Select **Subscription-based Microsoft Defender for Cloud (Legacy)** data connector.
    
    >**Note**: The connector can be enabled only on subscriptions that have at least one Microsoft Defender plan enabled in Microsoft Defender for Cloud, and only by users with Contributor permissions on the subscription.

1. In the details pane for the connector, select Open connector page.

1. On the configuration page, select the subscription and click on **Connect**
