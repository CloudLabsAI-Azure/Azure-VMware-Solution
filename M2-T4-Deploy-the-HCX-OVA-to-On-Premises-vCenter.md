# Task 4: Deploy the HCX OVA to On-Premises vCenter

## Deploy HCX OVA

In this step, we will deploy the HCX VM with the configuration from the On-Premises VMware Lab Environment section.

# Exercise 1: Deploy HCX from Content Library

1. Once the import is completed from the previous task, click on **Menu** and select **Inventory**. 

    ![](Images/Mod2Task4Pic1.png)
    
2. Right click on **SDDC-Datacenter** and select **New Virtual Machine**.

    ![](Images/Mod2Task4Pic2.png)
   
3. Select **Deploy from template** for **1 Select a creation type** and click on **Next**.

    ![](Images/Mod2Task4Pic3.png)
    
4. Next on **2 Select a template** select **VMware-HCX-Connector**, and click on **Next**.    

    ![](Images/Mod2Task4Pic4.png)
    
5. Enter **HCX-Connector** as the **Virtual machine name** in **3 Select a name and folder** and click **Next**.  

     ![](Images/Mod2Task4Pic5.png) 
     
6. On the **4 Select a compute resource** select **Cluster-1** and click on **Next**.

     ![](Images/Mod2Task4Pic6.png)
     
7. Click **Next** on **5 Review details**, In **6 License Agreement** accept the agreement and click **Next**.

8. Next for **7 Select storage** select the available storage and click **Next**.

    ![](Images/Mod2Task4Pic8.png)
  
9. For **8 Select networks** set the **Destination Network** as **Web-Segment** and click **Next**.
  
     ![](Images/Mod2Task4Pic9.png)

10.  Next on **9 Customize template** provide and following details and click **Next**.

       |Property| Value| 
       |---|---|
       |CLI “admin” User Password/root Password| MSFTavs1!|
       |Hostname| hcx-connector|
       |Network 1 IPv4 Address| 10.10.4.100|
       |Network 1 IPv4 Prefix Length| 24|
       |Default IPv4 Gateway| 10.10.4.1|
       |DNS Server list| 1.1.1.1|
       |Enable SSH| Enabled|
 
  ![](Images/Mod2Task4Pic10.1.png)
     
  ![](Images/Mod2Task4Pic10.2.png)
     
  ![](Images/Mod2Task4Pic10.3.png)
    
  ![](Images/Mod2Task4Pic10.4.png)
   
11. On **10 Ready to complete** click on **FINISH** to complete the setup of new virtual machine.

   ![](Images/Mod2Task4Pic11.png)
   
12. Once done, navigate to newly created **HCX-Connector VM** and **Power on**. The boot process may take 10-15 minutes to complete.   

   ![](Images/Mod2Task4Pic12.png)
