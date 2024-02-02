# Lab Overview: Building Your Cloud Journey with Azure VMware Solution

## Overview

Azure VMware Solution (AVS) is a cloud service on Microsoft Azure that allows organizations to run and manage VMware workloads seamlessly in the Azure environment. It offers integrated support, flexibility, and advanced networking, enabling a consistent hybrid cloud experience. AVS facilitates the extension of on-premises VMware environments to Azure without the need for extensive reconfiguration.

## Planning and Design:
 
### Define requirements: 
1. Start by outlining your specific needs, including the number of VMs, desired performance, network segmentation, security considerations, and budget constraints.
2. Choose an AVS SKU: Select the appropriate AVS SKU (AV36, AV36P, AV52, or AV64) based on your resource requirements and desired features.
3. Design the network architecture: Plan your virtual network structure, including subnets for the Jumpbox, Route Server, Gateway, workload segments, and any other required resources.
 
### Azure Subscription and Resource Group
 
**Create an Azure subscription:** Subscription will be already provided<br>
**Create a resource group:** Resource group to manage all the resources related to your AVS private cloud will be also pre-configured.
 
### ExpressRoute
For a secure and high-performance connection to your on-premises network, set up ExpressRoute. The upcoming exercises will guide you through the configuration process.
 
### Azure VMware Solution Creation:
As a prerequisite, we've completed the AVS private cloud deployment, specifying the SKU, resource group, network configuration, and cluster size. We'll now navigate through the configurations done during this initial deployment in the upcoming hands-on labs.
 
### Accessing the AVS Environment:
As part of accessing the AVS Environment, we will configure a jumpbox VM. This involves setting up the jumpbox VM in the designated subnet, allowing secure remote access to the AVS private cloud for initial management tasks. To proceed, we will connect to the jumpbox VM using RDP, establishing a secure entry point for further configuration and management.
 
### Network Configuration:
For the AVS network configuration, we'll set up NSX-T. If utilizing NSX-T for advanced networking and security, employ the vSphere Client to configure logical switches, firewalls, load balancers, and additional network services within the AVS private cloud. Additionally, we'll establish routing between different network segments, utilizing either static routes or dynamic routing protocols like BGP.
 
### Deploying VMs:
 
In the hands-on labs, the deployment of VMs will be executed using the vSphere Client, providing a user-friendly interface to manage VMs within the AVS private cloud while adhering to established processes and procedures. Furthermore, for seamless workload migration from on-premises, tools like VMware HCX will be employed, ensuring a smooth transition to the AVS environment..
 
### Ongoing Management and Monitoring:
 
During our lab sessions, we'll manage VMs and infrastructure using the vSphere Client and other VMware tools. Optionally, integrate Azure Monitor with Azure Arc for Servers for enhanced insights into resource performance. Additionally, utilize Azure Log Analytics for centralized logging and analysis of AVS events.

## Lab guide Content:

You will have access to a lab guide which is a reference material to assist you in getting started with the exploration.

Based on your interests, you can use this lab guide as a reference to learn and test any VMware feature. You are also encouraged to explore additional features of VMware based on your interests and preferences.

- Exercise 1 - Understand the AVS deployment architecture
- Exercise 2 - Connect Azure VNET to AVS using Express Route Connectivity 
- Exercise 3 - Configure DHCP for Azure VMware Solution
- Exercise 4 - Deploy VMware VMs in AVS 
- Exercise 5 - Enable Managed SNAT for Azure VMware Solution workloads 
- Exercise 6 - Configure a DNS forwarder in the Azure portal
- Exercise 7 - Deploy HCX for VM Migration
- Exercise 8 - Download the HCX OVA to JumpBox-VM vCenter
- Exercise 9 - Import the OVA file to the JumpBox-VM vCenter
- Exercise 10 - Setup HCX on AVS
- Exercise 11 - Obtain HCX License Key
- Exercise 12 - Activate VMware HCX
- Exercise 13 - Configure HCX and connect to vCenter
- Exercise 14 - Manage with Azure Arc 
- Exercise 15 - Logging with Log Analytics  
- Exercise 16 - Monitor AVS VMs with Azure Monitoring 
- Exercise 17 - Protect with Defender for Cloud 
- Exercise 18 - SIEM with Sentinel 

### Azure services and related products

- Azure VMware solution
- Azure Virtual Machine
- Virtual Network Gateway
- Microsoft Defender for Cloud
- Log Analytics Workspace
- Sentinel Workspace
- Azure Monitor
- Azure Arc

