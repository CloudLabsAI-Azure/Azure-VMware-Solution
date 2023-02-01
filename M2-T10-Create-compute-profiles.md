# Task 10: Create compute profiles

## HCX Compute Profile

A compute profile contains the compute, storage, and network settings that HCX uses on this site to deploy the interconnected dedicated virtual appliances when service mesh is added. For more information on compute profile and its creation please refer to [VMware documentation](https://docs.vmware.com/en/VMware-HCX/4.2/hcx-user-guide/GUID-BBAC979E-8899-45AD-9E01-98A132CE146E.html#:~:text=A%20Compute%20Profile%20contains%20the%20compute%2C%20storage%2C%20and,virtual%20appliances%20when%20a%20Service%20Mesh%20is%20added.).

# Exercise 1: Create Compute Profile 

1. In your on-premises HCX installation, click **Interconnect**. Select **Compute Profiles** and click C**REATE COMPUTE PROFILE**.

   ![](Images/Mod2Task10Pic1.png)
   
2. On **Create Compute Profile** pane, enter `OnPremCompute` for **Name your Compute Profile** and click **CONTINUE**.  

    ![](Images/Mod2Task10Pic2.png)
 
3. Review the selected services. By default all the above services are selected. In a real world scenario, if a customer let’s say doesn’t need Network Extension, you would unselect that service here. Leave all defaults for the purpose of this workshop. Click **CONTINUE**. 

    ![](Images/Mod2Task10Pic3.png)
