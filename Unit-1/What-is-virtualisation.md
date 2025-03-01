# What is  virtualisation 

* By using virtualisation, a resource—like a computer, server, storage device, network, or operating system—can be created virtually instead of    
  using the actual hardware. 
* It improves output, scalability, and resource usage through allowing the operation across multiple virtual environments on a single physical     
  system in an isolated environment.

## Types of virtualisation

* Hardware virtualisation is the process of operating several virtual machines (VMs) on a single physical server using a hypervisor.
* Operating System Virtualisation: this allows several containers (like Docker and LXC) to run on a single OS.
* Storage virtualisation: This creates a single virtual storage system by combining several storage devices.
* Network virtualisation: This process builds virtual networks without relying on physical infrastructure (e.g., VLAN, SDN).
* Virtual Local Area Network, or VLAN: This technology divides a physical network into several virtual networks for improved security.
* NIC (Network Interface Card) virtualisation: By enabling the existence of multiple virtual NICs (vNICs) on a single physical NIC, network efficiency is increased.                                               
* Application virtualisation: This allows apps to run in separate environments without requiring direct installation.
* Desktop virtualisation: This feature allows users to access a virtual desktop environment remotely.

![Types of Virtulization](/images/Types%20of%20Virtualization.png)

## History of Virtualization
  
The process of building a virtual version of computer resources, or virtualisation, has changed dramatically over the years. It originated in mainframe computing and has since developed into a key component of contemporary cybersecurity, cloud computing, and IT infrastructure.

**The years of virtualisation(1960s–1970s)**

* IBM Time-Sharing & Mainframes
* IBM invented virtualisation in the 1960s, which let several users share processing power.
* Time-sharing systems laid the groundwork for virtual machines (VMs) by allowing multiple users to access the same mainframe at once.
* In 1972, IBM released the VM/370, a complete virtualisation system that enabled the use of the same hardware by several operating systems.  

**Decline (1980s to 1990s)**

* Interest in a virtualisation fell in the 1980s as personal computers (PCs) turned growing in popularity.
* The vast majority of computing tasks shifted from centralised mainframes to stand-alone computer systems.
* However, server virtualisation arrived as a solution for improving data centred efficiency in the 1990s.
* The symbol Solutions (1986) implemented SoftPC, which allowed x86 applications to run on non-x86 platforms, marking an early step towards * *  
  cross-platform virtualisation.  

**Modern Virtualisation (2000s)**

* The virtualisation technology advanced and expanded during the 2000s. 
* VMware created an important contribution by introducing VMware Workstation (1999).
* VMware ESX Server (2001) which allowed multiple operating systems to run on a single server.
* This helped businesses to use their hardware more efficiently.
* In 2003, the open-source Xen hypervisor was developed, introducing a technique called para-virtualization.
* These developments made virtualisation more accessible and efficient, and led to the rise of the cloud Computing.

**Cloud (2010s – Present)**

* The virtualisation built the foundation for cloud computing, which allows major platforms like Amazon AWS, Microsoft Azure, and Google Cloud offer scalable and flexible computing resources. 
* Instead of relying on physical servers, businesses are able to run applications and store data in virtual environments, expanding IT infrastructure accuracy and efficiency.
* Docker introduced containers in 2013, offering a lightweight and faster alternative to traditional virtual machines.
* Containers made it easier to develop, ship, and run applications across different operating systems while preventing compatibility issues.      
* Kubernetes was introduced in 2015 to efficiently manage these containers, and it is currently the most popular tool for automating and scaling  
  container-based applications.

 ![History of Virtualization](/images/History%20of%20Virtualization.png)


### **Classification of Virtualization Based on Area & Technology**  

Virtualization can be classified into two category which are:-
* Based on Area 
* Technology

### Based on Area

**Server Virtualization**

* Allows multiple virtual servers to run on a single physical server.
* Improves resource utilization and reduces hardware costs.


**Desktop Virtualization**  

* Enables users to access a virtual desktop environment from any device.
* Improves security and centralized management. 

**Storage Virtualization**  

* Combines multiple physical storage devices into a single virtual storage pool.
* Enhances storage management, scalability, and redundancy.

**Network Virtualization**  

* Creates multiple virtual networks over a single physical network.
* Improves flexibility, security, and network management.
 
**Application Virtualization**  

* Runs applications in a virtual environment without direct installation on a user's device.
* Enhances compatibility and simplifies software deployment. 

**Data Virtualization**  
* Allows users to access and manage data from multiple sources without knowing its physical location.
* Improves integration and real-time data access.  


### Based on Technology 

**Full Virtualization**

* Simulates an entire hardware system, allowing multiple OS instances on the same machine.
* Requires a hypervisor.

**Para-Virtualization**

* The guest OS is modified to work with the hypervisor, improving efficiency.
* Requires specialized drivers or software modifications in the guest OS for optimized operation.
* Improves performance and efficiency by allowing better resource sharing.

**Hardware-Assisted Virtualization**

* Uses processor-based extensions to improve virtualization performance.
* Helps in running unmodified guest operating systems with near-native performance.
* Provides direct hardware support for better security and isolation between virtual machines.

**OS-Level Virtualization**

* Multiple isolated user spaces (containers) run on a single OS kernel.
* Allows applications to run consistently across different environments without dependency issues.
* Supports rapid deployment and scaling of applications, often used in cloud computing and microservices architecture.

**Memory Virtualization**

* Uses virtual memory techniques to extend the available RAM beyond physical limits.
* Improves system stability by preventing applications from directly accessing physical memory.
* Helps in running large-scale applications that require extensive memory resources.
