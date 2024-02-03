# Planning an AVS Deployment

Planning your Azure VMware Solution deployment is crucial for creating a successful production-ready environment for virtual machines (VMs) and migration. During the planning process, you identify and gather the necessary information for your deployment. Be sure to document the information you collect for easy reference during the deployment. A successful deployment results in a production-ready environment for creating VMs and migration.

You will have to: 
 * Identify the Azure subscription, resource group, region, and resource name
 * Identify the size of hosts and determine the number of clusters and hosts
 * Request a host quota for an eligible Azure plan
 * Identify the /22 CIDR IP segment for private cloud management
 * Identify a single network segment
 * Define the virtual network gateway
 * Define VMware HCX network segments

### Identify the subscription
Identify the subscription you plan to use to deploy Azure VMware Solution. In this lab, you can use an existing one.

### Identify the resource group
Identify the resource group you want to use for your Azure VMware Solution. Generally, a resource group is created specifically for Azure VMware Solution, but you can use an existing resource group (AVS-RG).

### Define the resource name
The resource name is a friendly and descriptive name for your Azure VMware Solution private cloud, for example, **AVS-DC (AVS Private Cloud)**.

### Identify the size hosts
Identify the size hosts that you want to use when deploying Azure VMware Solution.
Azure VMware Solution clusters are based upon hyper-converged infrastructure. The following table shows the CPU, memory, disk and network specifications of the host.

|Size hosts Details|	  |
|-------|-------|
|Host Type	| AV36|
|CPU (Cores/GHz)| Dual Intel Xeon Gold 6140 CPUs (Skylake microarchitecture) with 18 cores/CPU @ 2.3 GHz, Total 36 physical cores (72 logical cores with hyperthreading)|
|RAM (GB)| 576|
|vSAN Cache Tier (TB, raw)| 3.2 (NVMe)|
|vSAN Capacity Tier (TB, raw)| 15.20 (SSD)|
|Network Interface Cards| 4x 25-Gb/s NICs (2 for management & control plane, 2 for customer traffic)|
|Regional availability| East US|

An Azure VMware Solution cluster requires a minimum number of three hosts. You can only use hosts of the same type in a single Azure VMware Solution private cloud. Hosts used to build or scale clusters come from an isolated pool of hosts. Those hosts passed hardware tests and had all data securely deleted before being added to a cluster.

### Define the IP address segment for private cloud management
Azure VMware Solution requires a /22 CIDR network, such as 10.0.0.0/22. This address space is divided into smaller network segments (subnets) for Azure VMware Solution management segments including vCenter Server, VMware HCX, NSX-T Data Center, and vMotion functionality. The following diagram shows Azure VMware Solution management IP address segments.

### Define the virtual network gateway
Azure VMware Solution requires an Azure Virtual Network and an ExpressRoute circuit. Decide whether to use an existing or new ExpressRoute virtual network gateway. If you choose a new virtual network gateway, create it after creating your private cloud. Using an existing ExpressRoute virtual network gateway is acceptable. For planning purposes, note which ExpressRoute virtual network gateway you use.

#### References:
  * [Planning an AVS Deployment](https://learn.microsoft.com/en-us/azure/azure-vmware/plan-private-cloud-deployment)

