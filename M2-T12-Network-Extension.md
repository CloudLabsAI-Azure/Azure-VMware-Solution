# Task 12: Network Extension

# HCX Network Extension

You can extend networks between and HCX-activated on-premises environment and Azure VMware Solution (AVS) with HCX Network Extension.

With VMware HCX Network Extension (HCX-NE), you can extend a VM’s network to a VMware HCX remote site like AVS. VMs that are migrated, or created on the extended network at the remote site, behave as if they exist on the same L2 network segement a VMs in the source (on-premises) environment. With Network Extension from HCX, the default gateway for an extended network is only connected at the source site. Traffic from VMs in remote sites must be routed to a different L3 network will flow through the source site gateway.

With VMware HCX Network Extension you can:

  - Retain the IP and MAC addresses of the VMs and honor existing network policies.
  - Extend VLAN-tagged networks from a VMware vSphere Distributed Switch.
  - Extend NSX segments.

For more information please visit VMware’s documentation for [Extending Networks with VMware HCX](https://docs.vmware.com/en/VMware-HCX/4.3/hcx-user-guide/GUID-DD9C3316-D01C-4088-B3EA-84ADB9FED573.html).

Once the Service Mesh appliances have been deployed, the next important step is to extend the on-premises network(s) to AVS, so that any migrated VM’s will be able to retain their existing IP address.

# Exercise 1: Create a Network Extension
