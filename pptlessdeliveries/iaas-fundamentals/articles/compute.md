
# Compute

## Azure compute options

> **SHOW** [Overview of Azure compute options](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-overview)

> **NAVIGATION** https://azure.com > Documentation > Architecture > Azure Application Architecture Guide > Technology choices > [Compute options overview](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-overview)

> **SPEAKER NOTES**

* There are various compute options available in Azure.
* Briefly explain different options on **IaaS**, **PaaS** or **FaaS**.
* Provide **examples of IaaS compute options**. Some examples:
    * **Virtual Machines**: 
        * Are best used for application migrated to the cloud with no changes or lift and shift, as we call them. 
        Giving that you pay for the resources you actually use, you can save a lot, by scaling out your application to support peak times or growth.
    * **VMSS** (**Virtual Machine Scale Sets**): 
        * You can use to deploy and manage a set of identical VMs that you’ll manage as a single resource.
        * With all VMs configured the same, scale sets support true autoscale, and no pre-provisioning of VMs is required.  
        * So it's easier to build large-scale services that target big compute, big data, and containerized workloads.
    * **Marketplace**:
        * The Azure marketplace offers the flexibility in using the platforms, components and frameworks of your choice.
* Refer that in this session we are going to focus on virtual machines.


> **ADDITIONAL RESOURCES**

* [Virtual Machines Documentation](https://docs.microsoft.com/en-us/azure/virtual-machines/)
* [Virtual Machines Documentation - Windows](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/overview)
* [Virtual Machines Documentation - Linux](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/overview)
* [Virtual Machine Scale Sets Documentation](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/)



## Azure single virtual machine architecture

### Option Windows 

> **SHOW** [Azure single Virtual Machine architecture - Windows](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/virtual-machines-windows/single-vm)

> **NAVIGATION** https://azure.com > Documentation > Architecture > Reference Architectures > Windows VM workloads > [Single VM](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/virtual-machines-windows/single-vm)


### Option Linux 

> **SHOW** [Azure single Virtual Machine architecture - Linux](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/virtual-machines-linux/single-vm)

> **NAVIGATION** https://azure.com > Documentation > Architecture > Reference Architectures > Linux VM workloads > [Single VM](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/virtual-machines-windows/single-vm)

> **SPEAKER NOTES**

* Earlier, we looked at a single VM architecture from a storage perspective, lets look at a VM from a compute Perspective.
* When we think of compute, we think of cores, ram, and disks. 
* We already talked about OS and Data disks that are stored as Managed Disks in Azure Storage and the temp disks stored on the host.
* Now we are going to talk about the VM component.



## Azure Virtual Machine considerations

> **SHOW** [What do I need to think about before creating a VM?](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/overview#what-do-i-need-to-think-about-before-creating-a-vm)

> **NAVIGATION** https://azure.com > Documentation > Windows Virtual Machines > Overview > About Virtual Machines > [What do I need to think about before creating a VM?](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/overview#what-do-i-need-to-think-about-before-creating-a-vm)

> **SPEAKER NOTES**

* Explain important aspects to think about when creating VMs:
    * Naming
    * Location
    * VM size
    * VM Limits
    * Operating system disks and images
    * Extensions
    * Related resources



## Compute families

> **SHOW** [Sizes for Windows virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes)

> **NAVIGATION** https://azure.com > Documentation > Windows Virtual Machines > Concepts > [VM types and sizes](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes)

> **SPEAKER NOTES**

* Explain the variety of options in Compute sizes that you can select to closely match your workloads:
    * [General Purpose](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes-general)
    * [Compute optimized](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes-compute)
    * [Memory optimized](https://docs.microsoft.com/en-us/azure/virtual-machines/virtual-machines-windows-sizes-memory)
    * [Storage optimized](https://docs.microsoft.com/en-us/azure/virtual-machines/virtual-machines-windows-sizes-storage)
    * [GPU](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes-gpu)
    * [High performance compute](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes-hpc)
* Each size option has different variety of cores, RAM, disk space HDD or SDD to choose from – additionally, depending on what instance you select will also determine the size of the temporary/local disk.
* Some size options can handle Premium storage.  You may notice machines that have a lettered followed by S, denoting eligible use for SSD.
* Not all VM sizes available in all regions. 
* Explain how to compare performance across different options with [Azure Compute Units (ACU)](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/acu)



## Virtual Machines Availability

> **SHOW** [Availability sets](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/regions-and-availability#availability-sets)

> **NAVIGATION** https://azure.com > Documentation > Windows Virtual Machines > Concepts > Regions and availability > [Availability sets](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/regions-and-availability#availability-sets)

> **SPEAKER NOTES**

* Explain concepts of Availability Sets, Fault Domains and Update Domains.
* Explain concepts of Managed Disk fault domains.
* Explain concept of Availability zones. Note that is still in preview.


> **ADDITIONAL RESOURCES**

* [VM Availability on FTA GitHub](https://github.com/Azure/fta-wip/blob/master/pptlessdeliveries/iaas-fundamentals/articles/iaas-fundamentals-reference-resources.md#virtual-machines-availability) (with diagrams)


## Virtual machine scale sets

> **SHOW** [What are virtual machine scale sets in Azure?](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-overview)

> **NAVIGATION** https://azure.com > Documentation > Windows Virtual Machines > Concepts > Regions and availability > [Availability sets](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/regions-and-availability#availability-sets)

> **SPEAKER NOTES**

* Explain concept of VMSS.
* Explain benefits of VMSS:
    * **Auto-scale** - simply change the instance count and Scale Sets will increase or decrease the number of VMs while preserving HA.
    * **Performance** - deploying hundreds of VMs results in a single call to the fabric, allowing inherent performance optimizations.
    * **Customization** - built on Azure IaaS, Scale Sets support all Windows and Linux VMs including custom images and extensions.
    * **Ease of management** - building on the simple declarative modelling introduced with Azure Resource Manager, Scale Sets are the simplest way to manage sets of identical VMs. Focus on compute at scale without managing scaling of storage accounts and NICs.


> **ADDITIONAL RESOURCES**

* [VMSS on FTA GitHub](https://github.com/Azure/fta-wip/blob/master/pptlessdeliveries/iaas-fundamentals/articles/iaas-fundamentals-reference-resources.md#virtual-machine-scale-sets-vmss) (with diagrams)





## Walkthrough: Create a Virtual MachineAzure Portal

Create POC VMs 
and show management options



> **SHOW** []()

> **NAVIGATION** https://azure.com > Documentation > 

> **SPEAKER NOTES**

> **ADDITIONAL RESOURCES**












