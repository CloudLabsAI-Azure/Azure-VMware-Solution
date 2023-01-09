## Task 4: Advanced NSX-T Features within AVS
You can find more information about NSX-T capabilities in VMware’s website under [VMware NSX-T Data Center Documentation](https://docs.vmware.com/en/VMware-NSX-T-Data-Center/index.html).

In this Section, you will learn just a few additional NSX-T Advanced Features. You will learn how to:
  * Create NSX-T tags for VMs
  * Create NSX-T groups based on tags
  * Create Distributed Firewall Rules in NSX-T

### Exercise 1: Assign NSX-T Tags to VMs
**NSX-T Tags** help you label NSX-T Data Center objects so that you can quickly search or filter objects, troubleshoot and trace, and do other related tasks.
You can create tags using both the **NSX-T UI** available within AVS and APIs.

More information on NSX-T Tags can be found here: [VMware NSX-T Data Center Documentation](https://docs.vmware.com/en/VMware-NSX-T-Data-Center/3.2/administration/GUID-358DF469-75C8-48C4-B0E2-279E55C7BB3E.html#:~:text=Tags%20Tags%20help%20you%20to%20label%20NSX-T%20Data,create%20tags%20using%20both%20the%20UI%20and%20APIs.).

1. Open the **NSX-T** UI page which you have already connected in Edge browser, if you have closed the page you can reopen it using `https://10.10.0.3/` in edge browser of JumpBox. 

2. Under **Inventory (2)**, click on the **Virtual Machines (3)** option; Locate your two Virtual Machines you created in the previous task **TestVM-1** and **TestVM-2**.
 
   ![](Images/nsx-t-inventory-vms.jpg)
   
3. Click the **elipsis(...) (1)** next to the **TestVM-1** VM and click **Edit (2)**.

   ![](Images/edit-testvm1.jpg)
   
4. Locate the **Tag** area under VM edit section; add a tag with name `Web` (1) and then click on **Add item(s); Web (2)**. Now, click on the **Save (3)** to make the changes.

   ![](Images/testvm1-save-tag.jpg)
   
5. Let us add the same tag for **TestVM-2**;  Click the **elipsis(...) (1)** next to the **TestVM-2** VM and click **Edit (2)**.

   ![](Images/edit-testvm2.jpg)
   
6. Locate the **Tag** area under VM edit section; add a tag with name `Web` (1) and then click on **Add item(s); Web (2)**. Now, click on the **Save (3)** to make the changes.

   ![](Images/testvm2-save-tag.jpg) 
   
You have successfully added the Tag to the Virtual Machines, now let's us create a group by Tag name.

### Exercise 2: Create NSX-T Groups

Groups include different objects that are added both statically and dynamically, and can be used as the source and destination of a firewall rule.

Groups can be configured to contain a combination of Virtual Machines, IP sets, MAC sets, segment ports, segments, AD user groups, and other groups. Dynamic including of groups can be based on a tag, machine name, OS name, or computer name.

You can find more information on NSX-T Groups on VMware’s NSX-T Data Center docs.
