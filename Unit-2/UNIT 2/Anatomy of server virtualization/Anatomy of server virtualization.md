**Anatomy of server virtualization**

Server virtualization is a technology that allows multiple virtual machines (VMs) to run on a single physical server.

Each VM has its own operating system and applications, and they are all isolated from each other. This means that if one VM crashes, it will not affect the other VMs on the same Server.

**How server virtualization works:**

1. The hypervisor is installed on the physical server.   
1. The hypervisor creates virtual machines (VMs).
1. Each VM is assigned a share of the physical server's resources.   
1. The VMs run their own operating systems and applications.   
1. The hypervisor manages the VMs and allocates resources as needed.


**Types of Server virtualization :** 

**1  Hypervisor –** 

A Hypervisor or VMM(virtual machine monitor) is a layer that exists between the operating system and hardware. It provides the necessary services and features for the smooth running of multiple operating systems. 

It identifies traps, responds to privileged CPU instructions, and handles queuing, dispatching, and returning the hardware requests. A host operating system also runs on top of the hypervisor to administer and manage the virtual machines.

**2. Para Virtualization –** 

It is based on Hypervisor. Much of the emulation and trapping overhead in software implemented virtualization is handled in this model. The guest operating system is modified and recompiled before installation into the virtual machine. 
Due to the modification in the Guest operating system, performance is enhanced as the modified guest operating system communicates directly with the hypervisor and emulation overhead is removed. 

Example: Xen primarily uses Paravirtualization, where a customized Linux environment is used to support the administrative environment known as domain 0. 


**3. Full Virtualization –** 

It is very much similar to Paravirtualization. It can emulate the underlying hardware when necessary. The hypervisor traps the machine operations used by the operating system to perform I/O or modify the system status. After trapping, these operations are emulated in software and the status codes are returned very much consistent with what the real hardware would deliver. This is why an unmodified operating system is able to run on top of the hypervisor. 

Example: VMWare ESX server uses this method. A customized Linux version known as Service Console is used as the administrative operating system. It is not as fast as Paravirtualization. 




**4. Hardware-Assisted Virtualization –** 

It is similar to Full Virtualization and Paravirtualization in terms of operation except that it requires hardware support. Much of the hypervisor overhead due to trapping and emulating I/O operations and status instructions executed within a guest OS is dealt with by relying on the hardware extensions of the x86 architecture. 

Unmodified OS can be run as the hardware support for virtualization would be used to handle hardware access requests, privileged and protected operations, and to communicate with the virtual machine. 

Examples: AMD – V Pacifica and Intel VT Vanderpool provide hardware support for virtualization.

**5. Kernel level Virtualization –** 

Instead of using a hypervisor, it runs a separate version of the Linux kernel and sees the associated virtual machine as a user-space process on the physical host. This makes it easy to run multiple virtual machines on a single host. A device driver is used for communication between the main Linux kernel and the virtual machine. 
Processor support is required for virtualization ( Intel VT or AMD – v). A slightly modified QEMU process is used as the display and execution containers for the virtual machines. In many ways, kernel-level virtualization is a specialized form of server virtualization. 

Examples: User – Mode Linux( UML ) and Kernel Virtual Machine( KVM ) 


**6. System Level or OS Virtualization –** 

Runs multiple but logically distinct environments on a single instance of the operating system kernel. Also called shared kernel approach as all virtual machines share a common kernel of host operating system. Based on the change root concept “chroot”. 
chroot starts during bootup. The kernel uses root filesystems to load drivers and perform other early-stage system initialization tasks. It then switches to another root filesystem using chroot command to mount an on-disk file system as its final root filesystem and continue system initialization and configuration within that file system. 











**Three major layers in Xen Server**

1. **Hardware Layer:** This is the foundation of the XenServer environment. It consists of the physical server components like CPU, memory, network interfaces, and storage devices. XenServer requires specific hardware features, such as Intel VT or AMD-V, to support virtualization.   
1. **Xen Hypervisor:** This is the core of XenServer. It's a thin layer of software that sits directly on top of the hardware and provides the foundation for running virtual machines. The hypervisor is responsible for allocating resources (CPU, memory, etc.) to the virtual machines and ensuring they are isolated from each other.   
1. **Control Domain (Dom0):** This is a privileged virtual machine that runs on top of the hypervisor. It's a modified Linux environment that has direct access to the hardware and runs the XenServer management toolstack (XAPI). Dom0 is responsible for managing the other virtual machines (DomUs), handling I/O operations, and providing a management interface for the XenServer host.   



**Storage Virtualization Overview**

Storage virtualization is a technology that abstracts physical storage resources, creating a virtual layer between the physical storage and the applications that use it. This allows for more efficient and flexible management of storage, regardless of the underlying hardware.

Think of it like this: Imagine you have a bunch of different sized containers (physical storage devices) scattered around. Storage virtualization is like having a system that organizes these containers into a single, unified pool. You can then easily allocate and manage storage from this pool, without worrying about the individual containers.

**Types of Storage Virtualization**

Below are some types of Storage Virtualization.

- **Kernel-level virtualization:** In hardware virtualization, a different version of the Linux Kernel functions. One host may execute several servers thanks to the kernel level.
- **Hypervisor Virtualization: I**nstalled between the operating system and the hardware is a section known as a hypervisor. It enables the effective operation of several operating systems.
- **Hardware-assisted Virtualization:** Hardware-assisted virtualization is similar to complete para-virtualization, however, it needs hardware maintenance.
- **Para-virtualization:** The foundation of para-virtualization is a hypervisor, which handles software emulation and trapping.

**Methods of Storage Virtualization**

- **Network-based storage virtualization:** The most popular type of virtualization used by businesses is network-based storage virtualization. All of the storage devices in an FC or iSCSI SAN are connected to a network device, such as a smart switch or specially designed server, which displays the network's storage as a single virtual pool.
- **Host-based storage virtualization:** Host-based storage virtualization is software-based and most often seen in HCL systems and cloud storage. In this type of virtualization, the host, or a hyper-converged system made up of multiple hosts, presents virtual drives of varying capacity to the guest machines, whether they are VMs in an enterprise environment, physical servers or computers accessing file shares or cloud storage.
- **Array-based storage virtualization:** Storage using arrays The most popular use of virtualization is when a storage array serves as the main storage controller and is equipped with virtualization software. This allows the array to share storage resources with other arrays and present various physical storage types that can be used as storage tiers.

**Benefits of storage virtualization**

**1. Increased Storage Utilization:**

- **Pooling:** Storage virtualization combines multiple physical storage devices into a single virtual pool. This eliminates wasted space on individual devices and allows for more efficient allocation of storage.   
- **Thin Provisioning:** Storage is allocated on demand, rather than pre-allocated. This means you only use the storage you actually need, preventing over-provisioning and maximizing utilization.   

**2. Simplified Storage Management:**

- **Centralized Management:** Storage can be managed from a single console, making it easier to monitor, allocate, and maintain.
- **Non-Disruptive Operations:** Storage can be added, removed, or reconfigured without interrupting applications.   
- **Automation:** Many storage virtualization solutions offer automation features that can streamline tasks like provisioning, tiering, and data migration.   

**3. Improved Scalability and Flexibility:**

- **Easy Expansion:** It's simple to add more storage capacity to the virtual pool as needed, without disrupting operations.   
- **Dynamic Allocation:** Storage can be easily reallocated to different applications or workloads based on changing needs.   
- **Data Mobility:** Data can be moved between different storage devices or tiers without affecting applications.   

**4. Enhanced Data Protection and Availability:**

- **Redundancy:** Storage virtualization often incorporates features like mirroring and replication to protect data from hardware failures.   
- **Snapshots:** Snapshots of virtual storage can be easily created for backup and recovery purposes.   
- **Disaster Recovery:** Storage virtualization can simplify disaster recovery by enabling quick replication of data to a secondary location.   

**5. Reduced Costs:**

- **Lower Hardware Costs:** By optimizing storage utilization, organizations can reduce the need to purchase additional physical storage devices.   
- **Reduced Administrative Overhead:** Simplified management and automation can free up IT staff for other tasks.   
- **Lower Energy Costs:** By consolidating storage resources, organizations can reduce power consumption and cooling costs.   

**6. Increased Agility and Efficiency:**

- **Faster Provisioning:** Storage can be provisioned quickly and easily, enabling faster deployment of new applications and services.
- **Improved Performance:** Storage virtualization can incorporate features like caching and tiering to optimize performance.   
- **Better Resource Allocation:** Storage resources can be allocated more efficiently to meet the needs of different applications.



