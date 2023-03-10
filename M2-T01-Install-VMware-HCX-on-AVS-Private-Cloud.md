# Module 2 - Deploy HCX for VM Migration

Introduction to VMware HCX
VMware HCX™ is an application mobility platform designed for simplifying application migration, workload rebalancing and business continuity across data centers and clouds. HCX supports the following types of migrations:

 * Cold Migration - Offline migration of VMs.
 * Bulk Migration - scheduled bulk VM (vSphere, KVM, Hyper-V) migrations with reboot – low downtime.
 * HCX vMotion - Zero-downtime live migration of VMs – limited scale.
 *Cloud to Cloud Migrations – direct migrations between VMware Cloud SDDCs moving workloads from region to region or between cloud providers.
 * OS Assisted Migration – bulk migration of KVM and Hyper-V workloads to vSphere (HCX Enterprise feature).
 * Replication Assisted vMotion - Bulk live migrations with zero downtime combining HCX vMotion and Bulk migration capabilities (HCX Enterprise feature).

In this module, we will go through the steps to Install HCX, configure and migrate a test VM to Azure VMware Solution (AVS).


## HCX Setup for Azure VMware Solution (AVS) 

 ![](Images/Mod2MainPic1.png)

# Prerequisites
 * Ensure that Module 1 has been completed successfully as this will be required to connect HCX from AVS to the On-Premises Lab.
 * JumpBox from AVS should be able to ping following ip addresses:
    - AVS vCenter: get from the Azure Portal
    - On-prem vCenter: 10.X.Y.2

# Task 1: Install VMware HCX on AVS Private Cloud

## Exercise 1: Enable HCX on AVS Private Cloud

In the following task, we will be installing HCX on your AVS Private Cloud. This is a simple process from the Add-ons section in the Azure Portal. This can also be achieved via Bicep/ARM/PowerShell.

> **NOTE:** This task may or may not have been completed for you in your AVS environment. Only one participant per group can enable HCX in the SDDC so if you’re not the first participant in the group to enable HCX, just use these instructions for reference.

1. Navigate to the [**Azure Portal**](http://portal.azure.com/), search for **Azure VMware Solution (1)** in the search bar and click on **Azure VMware Solution (2)**.

   ![](Images/Mod2Task1Pic1.png)
  
2. Select **AVS-DC (1)** private cloud.
  
   ![](Images/Mod2Task1Pic2.png)
  
3. From your Private Cloud blade, click on **+ Add-ons (1)** under **Manage** section. Then click **Migration using HCX (2)**. Select the checkbox to agree with terms and conditions **(3)**. Click on **Enable and deploy (4)**.
  
   ![](Images/Mod2Task1Pic3.png)
   
4. HCX will start getting deployed in your **AVS Private Cloud** and it will take about 10-20 minutes to complete. Once the deployment is completed click on **Go to resource**.

   ![](Images/Mod2Task1Pic4.png)

#### Summary:
In this task, you have installed VMware HCX by enabling HCX on AVS Private Cloud.

#### References:
- [VMware’s HCX Documentation](https://www.vmware.com/products/hcx.html).
- [Install and activate VMware HCX in Azure VMware Solution](https://learn.microsoft.com/en-us/azure/azure-vmware/install-vmware-hcx)
