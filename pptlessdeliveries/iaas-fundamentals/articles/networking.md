###### Go back to [IaaS Fundamentals](iaas-fundamentals.md#delivery-guide)

# Networking

## Azure Networking

> **SHOW** [Azure networking](https://docs.microsoft.com/en-us/azure/networking/networking-overview)

> *Navigation*: https://azure.com > Documentation > Products > Networking > [Networking Overview](https://docs.microsoft.com/en-us/azure/networking/networking-overview)

Explore the following topics:
* [Azure networking concepts](https://docs.microsoft.com/en-us/azure/networking/networking-overview)


## Virtual Network

> **SHOW** [Azure Virtual Network](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)

> *Navigation*: https://azure.com > Documentation > Products > Networking > Networking Overview > Concepts > [Virtual Network](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)

Explore the following topics:
* [What is a Virtual Network](https://docs.microsoft.com/en-us/azure/networking/networking-overview)
* [Components of a Virtual Network](https://docs.microsoft.com/en-us/azure/networking/networking-overview)
  * Address spaces (IP prefixes): The range of IP addresses available in your virtual network 
  * Subnets: Named ranges of addresses assignable to virtual machines
  * DNS servers: References to DNS servers that will be assigned to virtual machines or cloud service instances in the virtual network

* [Virtual Network capabilities](https://docs.microsoft.com/en-us/azure/networking/networking-overview)
  * Network isolation and segmentation
  * Internet communication
  * Secure communication between Azure resources
  * Connectivity between virtual networks
  * Connectivity to an on-premises network
  * Traffic filtering
  * Network traffic routing 


## Walkthrough: Deploy a Virtual Network

> **GUIDE** [Create a virtual network with multiple subnets](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-create-vnet-arm-pportal#portal)

* Explain that the VNet is the foundation for all private connectivity within Azure. Similarly to on-premises, we have address spaces, subnets, and since we don’t allow DHCP, we define our DHCP Option for DNS via Azure.


## Network connectivity

> **SHOW** [Virtual networks and virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview)

> *Navigation*: https://azure.com > Documentation > Products > Compute > Windows Virtual Machines > Concepts > [Networking](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview)

Explore the following topics:
* [Network interface (NIC)](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview#network-interfaces)
    
    Notes: 
    * Stress that setting IP addresses inside of the Guest OS is completely unsupported.  The proper way is to set a reserved DHCP address in the Azure Portal, PowerShell, or CLI.

* [IP addresses](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview#ip-addresses)
    * Types of IP Addresses: Private or Public
    * Allocation methods: Dynamic or Static

    Notes: 
    * Azure does not let you port your public IP address blocks to Azure; you must leverage the IP addresses that are allocated to you by the underlying fabric.
    * If you deallocate your Resource Manager VM and the public IP association is Dynamic, you will lose your public IP; your IP address will not change while the resource is allocated, both for VMs, VPN Gateways, and Application Gateways.  
    * In addition, just mention that VPN gateway and Application Gateway only support Dynamic IPs
    * Static public IP addresses are commonly used in the following scenarios:
        * End-users need to update firewall rules to communicate with your Azure resources.
        * DNS name resolution, where a change in IP address would require updating A records.
        * Your Azure resources communicate with other apps or services that use an IP address-based security model.

More resources:
* [Manage Network interfaces (NICs)](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-network-interface)
* [IP address types and allocation methods in Azure](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-ip-addresses-overview-arm)



## Walkthrough: Configuring VM Connectivity

Purpose: The purpose of this exercise is to visually demonstrate to the customer how to complete day to day operations on leveraging static and public IP addresses on a VM.  When setting DNS servers, think of the scenario around a DMZ not leveraging the same DNS servers as their internal machines not public facing.

* Create a virtual machine, ensuring they are deploying it to their newly created VNet (Do not use a Public IP during creation)

> **GUIDE** [Create a Windows virtual machine with the Azure portal](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal)


* Once deployed, show the customer how to enable a Public IP on a NIC and set a static Private IP address on the VM

> **GUIDE** [Add, change, or remove IP addresses for an Azure network interface](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-network-interface-addresses)

* Set the DNS Servers for the NIC	

> **GUIDE** [Change DNS servers](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-network-interface#change-dns-servers)



## Privacy & Security

User Defined Routes (UDR)

Network Security Group (NSG)

## Load Balancing

Azure Load Balancing Options
https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-introduction#load-balancer-differences


## Hybrid connectivity

Connectivity Options to Azure
https://docs.microsoft.com/en-us/azure/guidance/guidance-connecting-your-on-premises-network-to-azure


## Virtual Appliances

What are network virtual appliances?

https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview#ip-forwarding

Native high availability


###### Go back to [IaaS Fundamentals](iaas-fundamentals.md#delivery-guide)