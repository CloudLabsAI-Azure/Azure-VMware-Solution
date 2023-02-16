# Lab 1: Walkthrough of Pre Env: OnPrem DC ready with a DRS Enabled Cluster with shared storage and vCenter and RRAS for VPN deployed. 

1. On your **JumpVM** go to start, search and open **Remote Desktop Connection** and enter `103.227.96.82:4440` IP and click **Connect** to On-prem VM.

   ![](/Images/avs-1.1.png)

2. Enter the following login credential and click **OK**.
    
    - Username: `administrator`
    - Password: `spektra@123`

      ![](/Images/avs-2.png)

3. Select **Yes** to connect if prompted that the remote computer's identity cannot be verified.

      ![](/Images/avs-3.png)

4. Open Edge browser on remote desktop and goto `192.168.0.60` webpage and click on **LAUNCH VSPHERE CLIENT (HTML5)**.

    ![](/Images/avs-4.png)

5. On the *Vsphere client*, click on **OnPremDatacenter** under **Summary** tab, observe the following resources.

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

> **Note**: The VM count might vary in your environment.

8. To view the connection between the *Onprem on* to *Azure VPN*, click on start, search and select **Routing and Remote Access**.

  ![](/Images/avs-8.png)

9. In **Routing and Remote Access** expand **VPN-01**, click on **Network Interfaces** and ensure **AzureS2S** that the *Status* is **Enabled** and the *Connection State* is in  **Connected**.

  ![](/Images/avs-9.png)

> **Important**: **DO NOT** make any changes in the **Routing and Remote Access** window as you will not be able to advance in the lab. 


