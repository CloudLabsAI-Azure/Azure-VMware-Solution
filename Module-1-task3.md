# Exercise 1: Create a content Library

1. Search **Azure VMware Solution (1)** and then select **Azure VMware Solution (2)**.

   ![](.././images/3.1.png "Select Azure VMware Solution")

1. Select your **Azure VMware Solution**.
1. On the Azure VMware Solution click on **VMware credentials (1)** under Manage and then copy the **Username** and **Password** under vCenter Server Credentials **(2)** and paste in in notepad for later use.

   ![](.././images/3.2.png)

1. Open a new tab in the Microsoft edge browser, Enter the URL that you copied. 


1. Login to the **VMware vSphere**; Enter the **Username** and **password** that you copied in step 3 and Click on **LOGIN**.


1. From AVS vCenter, Click on the **Menu (1)** bars and then Click on **Content Libraries (2)** under Inventory.


1. Click on the **Create** button to create the **New Content Library**.


1. On the **Name and location** pane; Enter name your Library as **Local-Lib (1)** and Click on **NEXT (2)**.


1. On the **Configure content library** pane; Leave it as default and Click on **NEXT**.


1. On the **Apply security policy** pane; Leave it as default and Click on **NEXT**.


1. On the **Add storage** pane; Select the **Storage (1)** and Click on **NEXT (2)**.


1. On the **Ready to complete** pane; Review your content library settings and Click on **FINISH**.


1. Click on your newly created Library i.e. **Local-Lib**.


1. On the Local-Lib Library, Click on **ACTIONS (1)** and then Click on **Import item (2)**.


1. Under Source tab, Enter URL as **https://gpsusstorage.blob.core.windows.net/ovas-isos/workshop-vm.ova** and Click on **IMPORT (2)**.



1. After Successfully Import Click on **Actions** on the top right and Click on **Continue**.



1. You will see the **workshop-vm** under the OVF & OVA Templates.


1. Select the workshop-vm and right click on **workshop-vm** and then Click on **New VM from This Template...**.


1. 
