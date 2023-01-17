# Task 2: Download the HCX OVA to On-Premises vCenter

## Exercise 1: Download HCX OVA for Deployment of HCX on-premises
The next step after installing HCX on your AVS Private Cloud, is to download HCX onto our On-Premises VMware environment, this will allow us to setup the connectivity to AVS and allow us to migrate. The HCX appliance is provided by VMware and has to be requested from within the AVS HCX Manager.

1. On the Azure VMware Solution page, click on **VMware credentials (1)** under Manage tab and then copy the **Username** and **Password** under **vCenter Server Credentials** **(2)** and save it in notepad for later use.

   ![](./Images/3.2.jpg)
  
2. Next under **Manage** section, click **+ Add-ons (1)**. Select **Migration using HCX (2)** and copy the **HCX Cloud Manager IP URL (3)**, open a new browser tab and paste it. 

   ![](./Images/Mod2Task2Pic1.png)

3. You may see a warning Your connection isn't private, then click on Advanced button and proceed with Continue to 10.10.0.2 (unsafe).

    ![](./Images/Mod2Task2Pic2.png)
    
    ![](./Images/Mod2Task2Pic3.png)
    
 4.  Enter the cloudadmin credentials obtained in **Step 1** and **LOG IN**.  

     ![](./Images/Mod2Task2Pic4.png)
