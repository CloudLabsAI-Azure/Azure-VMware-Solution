# Task 4: Deploy the HCX OVA to On-Premises vCenter

## Deploy HCX OVA

In this step, we will deploy the HCX VM with the configuration from the On-Premises VMware Lab Environment section.

# Option 1: Deploy OVA from download.

1. Once the import is completed from the previous task, click on **Menu**,  and select **Inventory**. 

    ![](Images/Mod2Task4Pic1.png)

2. Right click on **OnPremDatacenter** and select **Deploy OVF Template**.

     ![](Images/Mod2Task4Op1Pic1.png)

3. On **Select an OVF template** pane select **Local file** and click **UPLOAD FILES**. 

     ![](Images/Mod2Task4Op1Pic2.png)

4. Select the location of the downloaded OVA for HCX and click **Open**.

      ![](Images/Mod2Task4Op1Pic3.png)
       
5. Click **Next**.

      ![](Images/Mod2Task4Op1Pic4.png)

6. On **Select a name and folder**, Enter **VMware-HCX-Connector** for **Virtual machine name** and click **Next**.

      ![](Images/Mod2Task4Op1Pic5.png)      

7. Leave default on **Select a compute resource** and click **Next**.

      ![](Images/Mod2Task4Op1Pic6.png)

8. On **Review details** click **Next**.

      ![](Images/Mod2Task4Op1Pic7.png)

9. Accept the license on **License agreements** and click **Next**.

      ![](Images/Mod2Task4Op1Pic8.png)
        
10. On **Select storage**, for **Select virtual disk format** select  **Thin Provision** from the drop-down then select **TrueNAS** datastore and click **Next**.

       ![](Images/Mod2Task4Op1Pic9.png)

11. Next for **Select networks** set **Management** as the **Destination Network** and click **Next**.

       ![](Images/Mod2Task4Op1Pic10.png)

12. Next on **Customize template** provide and following details and click **Next**.   
    
       |Property| Value| 
       |---|---|
       |CLI “admin” User Password/root Password| MSFTavs1!|
       |Hostname| hcx-connector|
       |Network 1 IPv4 Address| 192.168.0.62|
       |Network 1 IPv4 Prefix Length| 24|
       |Default IPv4 Gateway| 192.168.0.1|
       |DNS Server list| 8.8.8.8|
       |NTP Server List| time.google.com|
       |Enable SSH| Enabled|

      ![](Images/Mod2Task4Op1Pic11.1.png)
      
      ![](Images/Mod2Task4Op1Pic11.2.png)
      
      ![](Images/Mod2Task4Op1Pic11.3.png)

13. On **Ready to complete** click on **FINISH** to complete the setup.

       ![](Images/Mod2Task4Op1Pic12.png)

14. Once done, navigate to newly created **VMware-HCX-Connector** VM and **Power on**. The boot process may take 10-15 minutes to complete.

       ![](Images/Mod2Task4Op1Pic13.png)

# Option 2: Deploy HCX from Content Library

1. Once the import is completed from the previous task, click on **Menu**, and select **Inventory**. 

    ![](Images/Mod2Task4Pic1.png)
    
2. Right click on **SDDC-Datacenter** and select **New Virtual Machine**.

    ![](Images/Mod2Task4Pic2.png)
   
3. Select **Deploy from template** for **Select a creation type** and click on **NEXT**.

    ![](Images/Mod2Task4Pic3.png)
    
4. Next on **Select a template** select **VMware-HCX-Connector** and click on **NEXT**.    

    ![](Images/Mod2Task4Pic4.png)
    
5. Enter **HCX-Connector** as the **Virtual machine name** in **Select a name and folder** and click **NEXT**.  

    ![](Images/Mod2Task4Pic5.png) 
     
6. On the **Select a compute resource** select **Cluster-1** and click on **NEXT**.

    ![](Images/Mod2Task4Pic6.png)
     
7. Click **Next** on **Review details**, in **License Agreement** accept the agreement and click **NEXT**.

8. Next for **Select storage** select the available storage and click **NEXT**.

    ![](Images/Mod2Task4Pic8.png)
  
9. For **Select networks** set the **Destination Network** as **Web-Segment** and click **NEXT**.
  
    ![](Images/Mod2Task4Pic9.png)

10.  Next on **Customize template** provide and following details and click **NEXT**.

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
