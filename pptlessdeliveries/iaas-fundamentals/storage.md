###### Go back to [IaaS Fundamentals](iaas-fundamentals.md#delivery-guide)

# Azure Storage

## What is Azure Storage?

> **SHOW** [Azure Storage](https://docs.microsoft.com/en-us/azure/storage/)

> *Navigation*: https://azure.com > Products > Products > [Storage](https://docs.microsoft.com/en-us/azure/storage/)

Explore the following topics:
* What is Azure Storage? 
    * Microsoft Azure Storage is a Microsoft-managed cloud service that provides storage that is highly available, secure, durable, scalable, and redundant. Azure Storage consists of Blob storage, File Storage, and Queue storage. Learn how to leverage Azure Storage in your applications with our quickstarts and tutorials.
    * Source: https://docs.microsoft.com/en-us/azure/storage/common/storage-introduction
* Briefly explain what are Files, Disks, Blobs, Queues, Tables and Archive.


More resources:

* [Introduction to Microsoft Azure Storage](https://docs.microsoft.com/en-us/azure/storage/common/storage-introduction)
* [Introducing the Azure Storage services](https://docs.microsoft.com/en-us/azure/storage/common/storage-introduction#introducing-the-azure-storage-services)


## Types of storage accounts

> **SHOW** [Types of storage accounts](https://docs.microsoft.com/en-us/azure/storage/common/storage-introduction#types-of-storage-accounts)

> *Navigation*: https://azure.com > Documentation > Products > Storage > Storage > Overview > [Types of storage accounts](https://docs.microsoft.com/en-us/azure/storage/common/storage-introduction#types-of-storage-accounts)

Explore the following topics:
* Various kinds of storage accounts:
  * General-purpose Standard	
  * General-purpose Premium	
  * Blob storage, hot and cool access tiers


## Scenarios

> **SHOW** [Deciding when to use Azure Blobs, Azure Files, or Azure Disks](https://docs.microsoft.com/en-us/azure/storage/common/storage-decide-blobs-files-disks)

> *Navigation*: https://azure.com > Documentation > Products > Storage > Storage > Overview > [Choose Blobs, Files or Disks](https://docs.microsoft.com/en-us/azure/storage/common/storage-decide-blobs-files-disks)

Explore the following topics:
* Comparison between scenarios for Files, Blobs, and Disks.


## Walkthrough: Create a Storage Account

> **GUIDE** [Create a storage account](https://docs.microsoft.com/en-us/azure/storage/storage-create-storage-account#create-a-storage-account)

* **Storage account name**: (prefix)stg01 [e.g. ftapocstg01]

> **GUIDE** [Manage your storage account](https://docs.microsoft.com/en-us/azure/storage/storage-create-storage-account#manage-your-storage-account)

* After storage account is created explore menus/options on the storage account blade



## Disks

### Disks for Azure VMs

> **SHOW** [About disks storage for Azure Windows VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds)

> *Navigation*: https://azure.com > Documentation > Products > Storage > Storage > Disks > [Disk storage](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds)

Explore the following topics:
* [Disks used by VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds#disks-used-by-vms)
  * Operating system disk
  * Temporary disk
  * Data disk
* [About VHDs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds#about-vhds)
* [Types of disks](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds#types-of-disks) 
  * Performance tiers: Standard or Premium Storage
  * Types of disks: unmanaged or managed - focus on Managed Disks


### Managed Disks

> **SHOW** [Azure Managed Disks Overview](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview)

> *Navigation*: https://azure.com > Documentation > Products > Storage > Storage > [Disks](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview)

Explore the following topics:
* [Benefits of managed disks](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview#benefits-of-managed-disks)
* [Pricing and Billing](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview#pricing-and-billing)
* [Managed Disk Snapshots](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview#managed-disk-snapshots)
* [Images](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview#images)
* [Images versus snapshots](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview#images-versus-snapshots)
* [Managed Disks and Encryption](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview#managed-disks-and-encryption)


## Walkthrough: Create a VM with Managed Disks

> **GUIDE** [Create a Windows virtual machine with the Azure portal](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal)

* Follow guidelines to create a VM
* On the **Basics** tab choose **HDD** for VM disk type
* On the **Settings** tab show options between creating VMs with **Managed disks** and tradicional storage account


## Walkthrough: Convert Managed Disk from standard to premium, and vice versa

> **SHOW** [Convert Azure managed disks storage from standard to premium, and vice versa](https://github.com/laraaleite/laleitetestrep/blob/master/iaas-fundamentals-cx/storage.md#convert-azure-managed-disks-storage-from-standard-to-premium-and-vice-versa)

> **GUIDE** [Convert Azure managed disks storage from standard to premium, and vice versa](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/convert-disk-storage)

* After VM is created show how to upgrade from Standard (HDD) disk to Premium (SSD) disk.
* Stop the VM
* Update to Premium capable VM size
* Update storage type to Premium
* Reboot



## Files

> **SHOW** [Introduction to Azure Files](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-introduction)

> *Navigation*: https://azure.com > Documentation > Products > Storage > Storage > Files > [Introduction](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-introduction)


Explore the following topics:
* [What are Azure Files](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-introduction)
* [Why Azure Files is useful](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-introduction#why-azure-files-is-useful)
* [Key benefits](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-introduction#key-benefits)


> **SHOW** [Azure File Sync scenario](https://github.com/laraaleite/laleitetestrep/blob/master/iaas-fundamentals-cx/storage.md#files)


More resources:
* [FAQ](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-faq)



## Walkthrough: Create a File Share

> **GUIDE** [Create a storage account](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account#create-a-storage-account)

> **GUIDE** [Create a file share](https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-portal#create-file-share)

> **GUIDE** [Upload and download files](https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-portal#upload-and-download-files)

> **GUIDE** [Connect to file share](https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-portal#connect-to-file-share)



###### Go back to [IaaS Fundamentals](iaas-fundamentals.md#delivery-guide)