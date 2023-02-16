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

5. On the *Vsphere client* click on **OnPremDatacenter** under **Summary** tab, observe the following resources and it's count.

    - Hosts:	2
    - Virtual Machines: 7 
    - Clusters:	1
    - Networks:	6
    - Datastores:	3

  ![](/Images/avs-5.png)

6.    

