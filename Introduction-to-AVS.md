# Introduction:
In this Hands-on Lab, you will delve into Azure VMware Solution (AVS), starting with an introduction to its architecture and a comparison with on-prem VMware deployments. Through hands-on labs, attendees will connect Azure VNET to AVS, configure DHCP, set up networking features like Managed SNAT and DNS forwarder, deploy VMware VMs in AVS, and explore advanced topics such as setting up HCX and implementing monitoring using Azure Monitor, Azure Arc, and Log Analytics. Post-workshop, self-paced exercises cover additional topics like monitoring AVS VMs with Azure Monitoring, securing with Defender for Cloud, and implementing SIEM with Sentinel.

## Architecture diagram:

   ![](./Labs/Images/diagram-avs1.png)

The Azure VMware Solution (AVS) architecture enables organizations to run and manage VMware workloads seamlessly within the Azure cloud environment. Here's an overview of the key components and how they interact:

### Azure Subscription:
AVS operates within an Azure subscription, providing a dedicated environment for running VMware workloads.

### Resource Groups:
AVS resources are organized within Azure resource groups, allowing for logical grouping and management.

### AVS Private Cloud:
The core of AVS is the private cloud, which consists of VMware vSphere clusters running on Azure infrastructure.
Each private cloud is associated with an Azure region.

### vSphere Cluster:
Within the private cloud, one or more vSphere clusters are deployed. These clusters include ESXi hosts and vCenter Server.

### ESXi Hosts:
Physical servers within the Azure data center running the ESXi hypervisor. Virtual machines (VMs) are deployed on these hosts.

### vCenter Server:
Manages the vSphere clusters and provides a centralized platform for VM management, provisioning, and monitoring.

### NSX-T Networking:
AVS uses VMware NSX-T for networking and security within the private cloud.
NSX-T enables features such as micro-segmentation, load balancing, and network automation.

### vSAN Storage:
Virtual Storage Area Network (vSAN) provides distributed storage across the ESXi hosts, ensuring high availability and performance.

### Azure Virtual Network Integration with ExpressRoute:
Azure VMWare Solution (AVS) private cloud integrates with Azure Virtual Network (VNET), allowing communication between Azure services and VMware workloads. AVS provide various methods to establish connect with other networks like Azure vNet Connect, ExpressRoute, ExpressRoute Global Reach, AVS Interconnect, in this lab we will be using ExpressRoute method. 

### Azure Entra ID Integration:
Integrates with Entra ID for identity and access management, enabling seamless user authentication. In this lab you will be able to access the AVS resource with your Azure Entra ID credentials provided in this lab.

### Azure Portal and APIs:
AVS is managed through the Azure portal, providing a unified interface for configuration, monitoring, and management.
Azure Resource Manager (ARM) APIs can also be used for automation and scripting.

### JumpBox VM:
You will be deploying the JumpBox, Virtual Network and Virtual Network gateway using an ARM template, these resources will be used to establish the connectivity with AVS and then from JumpBox you will be able to access the AVS vCenter Server and NSX-T Manager.

### HCX (Hybrid Cloud Extension):
HCX facilitates workload migration and mobility between on-premises data centers and the AVS private cloud.

### Azure Services Integration:
AVS allows seamless integration with various Azure services, enabling organizations to leverage Azure functionalities alongside their VMware workloads.
Overall, AVS provides a consistent and familiar VMware environment while leveraging the scalability, flexibility, and additional services available in the Azure cloud ecosystem. This integration simplifies the migration and management of VMware workloads in the cloud.
