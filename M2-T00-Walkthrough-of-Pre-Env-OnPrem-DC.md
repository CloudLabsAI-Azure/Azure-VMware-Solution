# Module 2: Walkthrough of Pre-Configured OnPrem Environment

1. On your **JumpBox** go to start, search and open **Remote Desktop Connection** and enter `xxx.xxx.xxx.xxx` IP and click **Connect** to On-prem vCenter VM.

   ![](/Images/avs-1.1.v2.jpg)

2. Enter the following login credential and click **OK**.
    
    - Username: `administrator`
    - Password: `spektra@123`

      ![](/Images/avs-2v2.jpg)

3. Select **Yes** to connect if prompted that the remote computer's identity cannot be verified.

      ![](/Images/avs-3.png)

4. Open Edge browser on remote desktop and goto `192.168.0.60` webpage and click on **LAUNCH VSPHERE CLIENT (HTML5)**.

    ![](/Images/avs-4.png)

5. On the *vSphere client*, click on **OnPremDatacenter** under **Summary** tab, observe the following resources.

    - Hosts
    - Virtual Machines 
    - Clusters
    - Networks
    - Datastores

    ![](/Images/avs-5.png)

6. Click on **Hosts & Clusters**, observe that we have two **Onprem host Vm**, ensure both are in **Connected** State. 

   ![](/Images/avs-6.png)

7. Click on **VMs** to observe the existing virtual machines. Here we see **VPN-01** VM that is being used to connect *Onprem site VPN* to *Azure VPN*.

   ![](/Images/avs-7.png)

    >**Note**: The VM count might vary in your environment.

8. To view the connection between the *Onprem on* to *Azure VPN*, click on start, search and select **Routing and Remote Access**.

    ![](/Images/avs-8.png)

9. In **Routing and Remote Access** expand **VPN-01**, click on **Network Interfaces** and ensure **AzureS2S** has the *Status* as **Enabled** and the *Connection State* is in **Connected**. Close the **Routing and Remote Access** window.

    ![](/Images/avs-9.png)

    >**Important**: **DO NOT** make any changes in the **Routing and Remote Access** window as you will loose access to OnPrem environemnt and not be able to proceed further in the lab. 

10. Back on the **vSphere Client** page, click on **Networks** tab and select **VM Network**.

    ![](/Images/avs-10.png)

11. In the **VM Network** page from the left menu under **DSwitch** observe the pre-created network switches and ensure the following are present:

    - Management
    - Uplink 
    - vMotion
    - Workload-Web

    ![](/Images/avs-11.png)

12. Next click on **OnPremDatacenter** and go to **Datastores** notice **TrueNAS** datastore. This is a common storage for all the VMs which is created and will get created.

    ![](/Images/avs-12.png)
