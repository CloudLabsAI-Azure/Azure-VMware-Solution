# Task 9: Create network profiles

## HCX Network Profiles
A Network Profile is an abstraction of a Distributed Port Group, Standard Port Group, or NSX Logical Switch, and the Layer 3 properties of that network. A Network Profile is a sub-component of a complete Compute Profile.

Customer’s environments may vary and may not have separate networks.

In this Task you will create a Network Profile for each network intended to be used with HCX services. More information can be found in VMware’s Official Documentation, Creating a Network Profile.

- **Management Network** - The HCX Interconnect Appliance uses this network to communicate with management systems like the HCX Manager, vCenter Server, ESXi Management, NSX Manager, DNS, NTP.
- v**Motion Network** - The HCX Interconnect Appliance uses this network for the traffic exclusive to vMotion protocol operations.
- **vSphere Replication Network** - The HCX Interconnect Appliance uses this network for the traffic exclusive to vSphere Replication.
- **Uplink Network** - The HCX Interconnect appliance uses this network for WAN communications, like TX/RX of transport packets.

These networks have been defined for you, please see below section.

In a real customer environment, these will have been planned and identified previously, see here for the [planning phase](https://docs.microsoft.com/en-us/azure/azure-vmware/plan-private-cloud-deployment#define-vmware-hcx-network-segments)

# Exercise 1: Create Network Profiles
