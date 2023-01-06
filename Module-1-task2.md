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
|DHCP Server IP	| 10.XY.50.1/30|
|Segment Name| WEB-NET-GROUP-XY|
|Segment Gateway| 10.XY.51.1/24|
|DHCP Range| 10.XY.51.4-10.XY.51.254|

## Task-1: Add DHCP Profile

1. Open the **VMware NSX-T** login page on the web browser using the **Web client URL**.

2. On the **Azure portal**, navigate to **AVS Private cloud** and select **VMware credentials (1)** under **Manage** tab. From **NSX-T Manager credentials (2)** copy the **Username (3)** and **Password (4)**.

3. Back on the **VMware NSX-T** login page paste the **Username (1)** and **Password (2)**. Click on **LOG IN (3)**.

4.
