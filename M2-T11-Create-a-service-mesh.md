# Task 11: Create a service mesh

## HCX Service Mesh Creation

An HCX Service Mesh is the effective HCX services configuration for a source and destination site. A Service Mesh can be added to a connected Site Pair that has a valid Compute Profile create on both of the sites.

Adding a Service Mesh initiates the deployment of HCX Interconnect virtual appliances on both sites. An interconnect Service Mesh is always created at the source site.

More information can be found inf VMware’s Official Documentation, [Creating a Service Mesh](https://docs.vmware.com/en/VMware-HCX/4.3/hcx-user-guide/GUID-46AED982-8ED2-4CB1-807E-FEFD18FAC0DD.html).

# Exercise 1: Create HCX Service Mesh

  > **Important Note**: Make sure port UDP 4500 is open between your On-Premises VMware HCX Connector ‘uplink’ network profile addresses and the Azure VMware Solution HCX Cloud ‘uplink’ network profile addresses.

1. On the **Interconnect** page, select **Service Mesh** tab and click on **CREATE SERVICE MESH**.

   ![](Images/Mod2Task11Pic1.png)

2. Ensure the right source site (on-premises) and destination site (AVS) are selected. Then click **CONTINUE**. 

    ![](Images/Mod2Task11Pic2.png)

3. For **Select Source Compute Profile** choose **OnPremCompute** , **click CLOSE**. Then for  **Select Remote Compute Profile** select **Remote Compute Profile** which you recently created and click **CLOSE**. Click **CONTINUE**.

    ![](Images/Mod2Task11Pic3.png)

4. On **Select Services to be activated** leave the Default Services and click **CONTINUE**.

    ![](Images/Mod2Task11Pic4.png)
