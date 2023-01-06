# Configure NSX-T to establish connectivity within AVS

## NSX-T on AVS
After deploying Azure VMware Solution, you can configure an NSX-T network segment from NSX-T Manager or the Azure portal. Once configured, the segments are visible in Azure VMware Solution, NSX-T Manager, and vCenter.

NSX-T comes pre-provisioned by default with an NSX-T Tier-0 gateway in Active/Active mode and a default NSX-T Tier-1 gateway in Active/Standby mode. These gateways let you connect the segments (logical switches) and provide East-West and North-South connectivity. Machines will not have IP addresses until statically or dynamically assigned from a DHCP server or DHCP relay.

  - In this Section, you will learn how to:

  - Create additional NSX-T Tier-1 gateways.

  - Add network segments using either NSX-T Manager or the Azure portal

  - Configure DHCP and DNS

  - Deploy Test VMs in the configured segments

  - Validate connectivity

# Exercise 1: Add DHCP Profile in AVS Private Cloud
A DHCP profile specifies a DHCP server type and configuration. You can use the default profile or create others as needed. A DHCP profile can be used to configure DHCP servers or DHCP relay servers anywhere in your SDDC network.

|AVS NSX-T Details|	  |
|-------|-------|
|DHCP Server IP	| 10.10.5.1/30|
|Segment Name| WEB-NET-GROUP-XY|
|Segment Gateway| 10.XY.51.1/24|
|DHCP Range| 10.XY.51.4-10.XY.51.254|

1. Open the **VMware NSX-T** login page on the web browser using the **Web client URL**.

2. On the **Azure portal**, navigate to **AVS Private cloud** and select **VMware credentials (1)** under **Manage** tab. From **NSX-T Manager credentials (2)** copy the **Username (3)** and **Password (4)**.

3. Back on the **VMware NSX-T** login page paste the **Username (1)** and **Password (2)**. Click on **LOG IN (3)**.

4. Once successfully logged in click on **POLICY** on the top right. On the **User Interface Mode Toggle** pop-up, check the **Don't show this again** box and click on **GOT IT!**.

5. In the **NSX-T Console**, click **Networking**. Select **DHCP** under management and click on **ADD DHCP PROFILE**.

6. On the DHCP profile page provide the following details and **Save (4)**.
  
   - **Profile Name:** `Web-DHCP` **(1)**
   - **Profile Type:** `DHCP Server` **(2)**
   - **Server IP Address:** `10.10.5.1/30` **(3)**


7. The **DHCP profile** has been added successfully.


# Exercise 2: Create an NSX-T T1 Logical Router

NSX-T has the concept of Logical Routers (LR). These Logical Routers can perform both distributed or centralized functions. In AVS, NSX-T is deployed and configured with a default T0 Logical Router and a default T1 Logical Router. The T0 LR in AVS cannot be manipulated by AVS customers, however the T1 LR can be configured however an AVS customer chooses. AVS customers also have the option to add additional T1 LRs as they see fit.

1. In the **NSX-T Console**, click **Networking (1)**. Select **Tier-1 Gateways (2)** under connectivity then click **Eclipse button (3)** and select **Edit (4)**.

2. On **Tier-1 Gateways** page, click on **Set DHCP Configuration**. 

3. In **Set DHCP Configuration** pane select **Type** as **DHCP Server (1)** and **DHCP Server Profile** as **Web-DHCP (2)** then click **Save (3)**
