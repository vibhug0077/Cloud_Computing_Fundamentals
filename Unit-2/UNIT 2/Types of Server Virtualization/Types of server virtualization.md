Server virtualization is a technology that allows you to run multiple virtual servers on a single physical server. This can help you to improve your server utilization, reduce your hardware costs, and simplify your server management. 

The operating system and hardware are separated by a virtualisation layer. Through dynamic partitioning and sharing of the available physical resources, including CPU, storage, memory, and I/O devices, this virtualisation layer enables several operating system instances to run concurrently within virtual machines on a single computer.





Here's a breakdown of how it works:

**The Hypervisor: The Conductor**

At the heart of server virtualization is the **hypervisor**. This is a special piece of software that acts as a conductor, managing the physical server's resources (CPU, memory, storage) and allocating them to the virtual servers.

There are two types of hypervisors:

- **Type 1 (Bare-metal)**: Runs directly on the physical hardware, without an underlying host OS. Examples include VMware ESXi, Microsoft Hyper-V, and Xen.
- **Type 2 (Hosted)**: Runs on top of an existing operating system, which then interacts with the hardware. Examples include VMware Workstation, Oracle VirtualBox.


**Creating Virtual Machines (VMs)**

The hypervisor creates **virtual machines (VMs)**. Each VM is like a separate computer with its own operating system (like Windows or Linux) and applications. The hypervisor makes each VM think it has its own dedicated hardware, even though they all share the same physical machine.

**Sharing Resources Efficiently**

The hypervisor cleverly divides the physical server's resources (CPU, memory, storage) among the VMs. It ensures that each VM gets the resources it needs to run smoothly, while also preventing any one VM from hogging all the resources.

**Isolation and Independence**

Each VM operates in its own isolated environment. This means that if one VM crashes or has a problem, it won't affect the other VMs running on the same physical server. It's like having multiple separate rooms in a house - if something goes wrong in one room, it doesn't necessarily affect the others.

**Advantages of server virtualization:**

Among the many advantages of server virtualisation are:

**Increased server utilisation:** By enabling you to host several virtual servers on a single physical server, server virtualisation can help you increase your server utilisation. This might assist you in lowering your energy usage and hardware expenses.

**Decreased hardware expenses**: Server virtualisation can assist you in lowering your hardware expenses by increasing server utilisation. It might be possible to combine several physical servers into one, which could result in cost savings on maintenance, software, and hardware.

**Simplified server management:** By enabling you to control several virtual servers from a single panel, server virtualisation can make your server management easier. Provisioning, keeping an eye on, and maintaining your servers may become simpler as a result.

**Greater flexibility**: By making it simple to switch virtual servers between real servers, server virtualisation can help you become more flexible. Scaling your apps or disaster recovery may benefit from this.

**Applications for virtualizing servers:**

There are numerous applications for server virtualisation, such as:

**Web hosting**: Web hosting companies frequently utilise server virtualisation to house several websites on a single physical server.

**Cloud computing**: One of the main factors enabling cloud computing is server virtualisation. Server virtualisation is used by cloud providers to build virtual machines that are available for rent to clients.

**Enterprise IT**: Many businesses utilise server virtualisation to increase server utilisation and consolidate their server architecture.

**Disaster recovery**: Virtual machines that can be utilised for disaster recovery can be created using server virtualisation. The virtual machines can be swiftly transferred to a different physical server in case the real server fails.

There are three main types of Server Virtualization:


**1) Full Virtualization:**

Since this kind of virtualisation just entails basic virtualisation, it is frequently used in the IT world. It uses hypervisors to simulate a hardware device and all the components required to host operating systems.

Separate hardware emulations are developed for each guest operating system in complete virtualisation. In a single physical hardware unit, this renders every guest server completely operational and separate from the other servers. Because they are not dependent on one another, this type of server is ideal for running many operating systems. 

While the core concept of full virtualization remains the same – creating a complete virtual hardware environment for each VM – there are a couple of key approaches within full virtualization that are worth understanding:

**a) Software Assisted Full virtualization:** Software-assisted full virtualization is a type of full virtualization that relies heavily on software techniques, specifically **binary translation**, to emulate the hardware environment for virtual machines (VMs).

Software-assisted full virtualization, an older technique, emulates hardware entirely through software. The hypervisor uses **binary translation**, intercepting and modifying guest OS instructions before they reach the physical hardware. This allows running any operating system without modification, a key advantage.

` `However, binary translation introduces significant performance overhead, as each instruction must be translated. This makes it resource-intensive and slower compared to hardware-assisted virtualization.

` `While it offers flexibility for legacy systems or situations lacking hardware virtualization support, it's less common today due to the performance penalty. Modern CPUs with virtualization extensions (like Intel VT-x or AMD-V) have made hardware-assisted virtualization the preferred and much more efficient method.


**b) Hardware Assisted Full virtualization:** Binary translation is not required with hardware-assisted virtualisation. Rather, the virtualisation technique on the X86 Processors (Intel VT-x and AMD-V) interrupts the original hardware directly. Privilege commands can be carried out directly on the processor, depending on what the guest operating system instructs.


- VMware vSphere with ESX/ESXi
- Kernel-based Virtual Machine (KVM)
- Microsoft Hyper-V
- Oracle VM
- Citrix Hypervisor

` `**Type 2 Hypervisor,** sometimes referred to as the hosted hypervisor type, is set up within the host computer's operating system. This hypervisor has a single software layer below, in contrast to Type 1.



Data centres with few physical servers are usually the ones that use the Type 2 hypervisor. Its similarity to the apps in the present operating system is what makes it easy to use. After installing the hypervisor, setting up and maintaining several virtual computers is simple. Some of the type 2 hypervisors available on the market are as follows:

- Oracle VM Virtualbox
- VMWare Workstation Pro/VMWare Fusion
- Windows Virtual PC
- Parallels Desktop

` `Instead of relying solely on software emulation, the hypervisor can offload certain virtualization tasks directly to the CPU. This dramatically reduces the overhead associated with translating guest OS instructions, leading to near-native performance for virtual machines (VMs).

**Improved Performance:** VMs achieve near-native performance, as the CPU handles many instructions directly.

**Enhanced Efficiency:** The CPU handles more virtualization tasks, freeing the hypervisor for other management functions.

**Increased Scalability:** Better performance allows running more VMs on a single physical server.

**Advantages of Full Virtualization:**

- **Operating System Agnostic:** Run any operating system, including legacy or proprietary ones, without modification. This is crucial for supporting older applications or diverse software requirements.
- **Strong Isolation:** VMs are completely isolated from each other. A crash or security issue in one VM won't affect others, enhancing stability and security.
- **Easy Migration:** VMs can be easily moved between physical servers (live migration), minimizing downtime for maintenance or load balancing.
- **Resource Management:** The hypervisor can dynamically allocate and manage resources (CPU, memory, storage) among VMs, optimizing utilization.
- **Consolidation:** Run multiple VMs on a single physical server, reducing hardware costs, power consumption, and physical space requirements.

**Disadvantages of Full Virtualization:**

- **Performance Overhead:** While hardware-assisted virtualization has significantly reduced this, there's still some inherent overhead as the hypervisor manages resource allocation and emulates hardware.
- **Resource Intensive (Relatively):** Full virtualization can be more resource-intensive compared to other virtualization methods like containerization, especially for I/O-intensive workloads.
- **Complexity:** Setting up and managing a full virtualization environment can be more complex than other virtualization solutions.

In summary, full virtualization offers excellent flexibility, isolation, and migration capabilities, making it ideal for diverse workloads and server consolidation. However, it can have some performance overhead and resource intensity compared to other virtualization types.

**2) OS- level virtualization:**

OS-level virtualization, also known as containerization, is a lightweight virtualization technique that operates at the operating system (OS) level. Instead of emulating hardware like in full virtualization, it leverages features within the host OS kernel to create isolated containers.

**Here's a detailed explanation:**

**Core Concept:**

OS-level virtualization takes advantage of the fact that an OS kernel already manages and isolates processes. It extends this capability to create isolated environments called containers, which share the same kernel as the host OS but have their own user space, libraries, and applications.

**Key Features:**

- **Shared Kernel:** All containers on a host share the same OS kernel. This is the key difference from full virtualization, where each VM has its own kernel.
- **Isolated User Space:** Each container has its own isolated user space, meaning it has its own file system, process space, and network interfaces. This provides a level of isolation between containers, preventing them from interfering with each other.
- **Lightweight:** Because containers share the kernel and don't need to emulate hardware, they are very lightweight and have minimal overhead. This makes them very efficient and allows for a high density of containers on a single host.

**How it Works:**

The OS kernel uses features like namespaces and control groups (cgroups) to create and manage containers:

- **Namespaces:** Isolate various resources like process IDs, network interfaces, file system mounts, and inter-process communication (IPC) objects. This makes each container believe it has its own dedicated resources.
- **Cgroups:** Limit and account for the resource usage (CPU, memory, I/O) of each container. This ensures that containers don't consume more resources than they are allocated.

**Advantages of OS-Level Virtualization:**

- **Lightweight and Efficient:** Containers have minimal overhead, leading to high density and efficient resource utilization.
- **Fast Startup Times:** Containers start up very quickly, often in seconds, as there's no need to boot a separate OS kernel.
- **Portable:** Containers can be easily moved between different hosts running the same OS kernel.

**Disadvantages of OS-Level Virtualization:**

- **OS Restriction:** All containers must run the same OS kernel as the host. This limits flexibility compared to full virtualization, where you can run different OSs on the same host.
- **Less Isolation (Potentially):** While containers provide good isolation, they share the same kernel. A vulnerability in the kernel could potentially affect all containers.

**Use Cases:**

OS-level virtualization is commonly used for:

- **Microservices:** Deploying and scaling individual components of an application as separate containers.
- **Cloud-Native Applications:** Building and running applications designed for cloud environments.
- **DevOps:** Streamlining development, testing, and deployment workflows.
- **Continuous Integration/Continuous Deployment (CI/CD):** Automating the building and deployment of applications.

**Examples of OS-Level Virtualization Technologies:**

- **Docker:** A popular platform for building, running, and managing containers.
- **LXC (Linux Containers):** A low-level container technology for Linux.
- **Solaris Zones:** A containerization technology for Solaris.

**In summary,** OS-level virtualization offers a lightweight and efficient way to run multiple isolated applications on a single host. Its speed, portability, and resource efficiency make it a popular choice for modern application development and deployment. However, it's important to be aware of the OS restriction and potential security implications of sharing the kernel.

**3) Para Virtualization:**

Para-virtualization is a virtualization technique that aims to boost performance by having the guest operating systems (OSs) cooperate with the hypervisor. It stands in contrast to full virtualization, where guest OSs are completely oblivious to the virtualization layer. The only main difference is that the guest systems are aware of each other’s presence and they all work as one entire unit.Here's a detailed breakdown:

**Core Concept:**

The fundamental idea behind para-virtualization is to reduce the overhead associated with hardware emulation in full virtualization. Instead of the hypervisor emulating every hardware interaction, the guest OS is modified to be aware of the hypervisor and can directly request services through special calls. This minimizes the "translation" work the hypervisor has to do, leading to performance gains.

- It's crucial to remember that para-virtualization always requires modifications to the guest OS. This is a fundamental characteristic that distinguishes it from full virtualization.
- The specific details of para-virtualization implementations can vary depending on the hypervisor and the guest OS.
- Due to the OS modification requirement, para-virtualization is less common than full virtualization or containerization in general-purpose server virtualization.

**Key Components and Interactions:**

**1. Modified Guest Operating Systems**

- Unlike full virtualization, where guest operating systems are unaware of the virtualization layer, para-virtualization requires modifications to the guest OS.
- These modifications make the guest OS "hypervisor-aware," enabling it to communicate directly with the hypervisor.

**2. Hypercalls**

- Instead of relying on the hypervisor to emulate hardware, the modified guest OS uses special calls called "hypercalls" to request services from the hypervisor.
- These hypercalls are more efficient than emulated hardware interactions, as they allow the guest OS to bypass the emulation layer and communicate directly with the hypervisor.

**3. Reduced Overhead**

- By working together with the hypervisor, the guest OSes can avoid the overhead associated with hardware emulation.
- This leads to better performance, especially for input/output (I/O) intensive workloads.

**How it Works (Step-by-Step):**

1. A guest OS within a VM needs to perform an I/O operation (e.g., read from disk).
1. In full virtualization, the hypervisor would intercept this request and emulate the disk controller.
1. In para-virtualization, the modified guest OS recognizes it's in a virtualized environment.
1. Instead of trying to access the hardware directly, it makes a hypercall to the hypervisor, requesting the I/O operation.
1. The hypervisor, knowing the context of the request, can handle it more efficiently, potentially by directly accessing the physical disk or using other optimized methods.
1. The hypervisor returns the results of the I/O operation to the guest OS.


Para-virtualization, while not as widely used as it once was, offers some distinct advantages, primarily centered around performance:

- **Improved Performance:** This is the core strength of para-virtualization. By modifying the guest operating systems to be aware of the hypervisor, they can communicate directly and efficiently, bypassing the need for the hypervisor to emulate hardware. This leads to reduced overhead and can significantly boost performance, especially for I/O-intensive workloads.
- **Efficient Resource Sharing:** Para-virtualization allows for more efficient sharing of resources between virtual machines (VMs). Because the guest OSes can directly interact with the hypervisor, they can coordinate and allocate resources more effectively, leading to better overall utilization of the physical hardware.
- **Granular Control:** Para-virtualization can provide more granular control over resources. This allows for fine-tuning and optimization of resource allocation based on the specific needs of each VM, leading to more efficient use of hardware.

  **Disadvantages:**

- **Operating System Modification Required:** This is the biggest and most impactful disadvantage. Para-virtualization necessitates modifying the guest operating systems to be aware of and cooperate with the hypervisor. This is a complex undertaking, requiring specialized knowledge and access to the OS source code.
- **Limited OS Support:** Because of the OS modification requirement, only operating systems specifically designed or modified for para-virtualization can be used. This drastically restricts the choice of guest OSs and makes it unsuitable for running legacy or proprietary operating systems.
- **Maintenance Overhead:** Maintaining modified OS kernels adds complexity to system administration. Updates to the OS or the hypervisor can require further modifications and testing, increasing the maintenance burden.
- **Compatibility Issues:** Modified OS kernels can sometimes introduce compatibility issues with applications or drivers designed for standard, unmodified OSs. This can lead to unexpected problems and require additional effort to resolve.
- **Less Isolation (Potentially):** While para-virtualization still provides isolation between VMs, the closer interaction between the guest OS and the hypervisor *could*, in theory, introduce slightly more risk compared to full virtualization. Careful hypervisor design is essential to mitigate this. However, this is generally less of a concern than the OS modification issue.
- **Diminishing Returns with Hardware Virtualization:** With the widespread adoption and advancements in hardware-assisted virtualization (Intel VT-x, AMD-V), the performance gap between full virtualization and para-virtualization has significantly narrowed. This diminishes the primary advantage of para-virtualization, making the drawbacks even more pronounced.

In short, the significant challenges related to OS modification, limited compatibility, and increased maintenance overhead have outweighed the performance benefits of para-virtualization for most use cases. The rise of efficient hardware-assisted full virtualization has largely relegated para-virtualization to niche applications.

**Use Cases and Current Relevance:**

Historically, para-virtualization was explored as a way to improve virtualization performance. However, with advancements in hardware-assisted virtualization (Intel VT-x, AMD-V), the performance gap between full virtualization and para-virtualization has narrowed significantly. Coupled with the significant disadvantage of requiring OS modifications, para-virtualization is less commonly used today. While it might still be found in some specialized high-performance computing environments, full virtualization and containerization are much more prevalent in modern data centers and cloud environments.

` `Para-virtualization is a technique that aims to enhance virtualization performance by enabling cooperation between the guest OS and the hypervisor. While it can offer performance benefits, the requirement for OS modifications has limited its adoption and made it less relevant in the face of advancements in full virtualization technologies.


**Simulation:**

Simulation plays a dual role in the world of virtualization, acting both as a core mechanism and as a powerful analytical tool. 

**1. Simulation *within* Virtualization: Hardware Emulation**

At the heart of full virtualization lies the concept of hardware emulation. The hypervisor, the software that manages virtual machines (VMs), essentially *simulates* the physical hardware for each VM. This simulated hardware environment includes:

- **CPU:** The hypervisor creates a virtual CPU, making the VM believe it has its own dedicated processor. This involves translating instructions from the guest OS into instructions that the physical CPU can understand.
- **Memory:** The hypervisor manages the physical RAM and allocates portions to each VM, creating isolated memory spaces. The VM interacts with this virtualized memory as if it were directly accessing physical RAM.
- **Storage:** The hypervisor presents virtualized storage devices (virtual hard disks) to each VM. These virtual disks are mapped to files or partitions on the physical storage.
- **Networking:** The hypervisor creates virtual network adapters, allowing VMs to connect to the network. Network traffic from the VM is routed through the hypervisor to the physical network interface.

This hardware emulation is crucial. It allows different operating systems, even older or incompatible ones, to run simultaneously on the same physical hardware without any modifications. The guest OS is completely unaware that it's interacting with simulated, not real, hardware
.

**2. Simulation *of* Virtualized Environments: Modeling and Analysis**

Beyond the internal simulation performed by the hypervisor, simulation tools are also used to model and analyze virtualized environments, particularly in cloud computing. These simulations help with:

- **Capacity Planning:** Predicting resource needs and optimizing the allocation of servers, storage, and network bandwidth. Simulations can model different workload scenarios to ensure the infrastructure can handle peak demand.
- **Performance Evaluation:** Testing how applications will perform under various conditions, identifying bottlenecks, and optimizing configurations. This can involve simulating different load levels, network latency, and resource availability.
- **Infrastructure Design:** Designing and optimizing the layout and configuration of data centers and cloud environments. Simulations can help determine the optimal placement of servers, network devices, and other infrastructure components.
- **Disaster Recovery Testing:** Simulating failures to evaluate the effectiveness of backup and recovery procedures. This helps identify weaknesses in disaster recovery plans and ensure business continuity.

Tools like CloudSim, iFogSim, and others provide frameworks for building these simulations. They allow researchers and cloud providers to experiment with different scenarios, optimize their systems, and improve the efficiency and reliability of their virtualized environments.

In short, simulation is both a fundamental part of how virtualization *works* (hardware emulation) and a valuable tool for *analyzing and improving* virtualized systems, especially in the context of cloud computing.


**Hardware Assisted Virtualization**

Hardware-assisted virtualization represents a significant advancement in virtualization technology, drastically improving performance and efficiency compared to software-based approaches. It leverages features built directly into modern CPUs to streamline the virtualization process, reducing overhead and enabling near-native performance for virtual machines (VMs).

**The Challenge: Emulation Overhead**

Traditional full virtualization, without hardware assistance, relies on the hypervisor to emulate the hardware environment for each VM. This involves interpreting and translating instructions from the guest OS to the physical hardware. This translation, while essential for isolation and managing resources, introduces significant overhead. The hypervisor acts as a middleman, constantly translating between the virtual and physical worlds, which consumes processing power and slows down execution.

**The Solution: CPU Virtualization Extensions**

Hardware-assisted virtualization addresses this performance bottleneck by offloading much of the translation work to the CPU itself. Modern CPUs from Intel and AMD include specific instructions and features designed to support virtualization. These features, known as virtualization extensions (Intel VT-x and AMD-V), create a new execution mode specifically for VMs, enabling them to run more directly on the hardware.

**Key Components and Mechanisms:**

1. **Virtualization Extensions (VT-x and AMD-V):** These CPU extensions are the foundation of hardware-assisted virtualization. They introduce new instructions and capabilities that allow the CPU to differentiate between the hypervisor and the VMs.
1. **Guest Mode (Non-Root Mode):** The CPU extensions create a "guest mode" or "non-root mode" specifically for VMs. This isolated execution mode prevents VMs from directly accessing or interfering with the hypervisor or other VMs, ensuring security and stability.
1. **Host Mode (Root Mode):** The hypervisor itself runs in "host mode" or "root mode," which has full access to the physical hardware. This privileged mode allows the hypervisor to manage the VMs, allocate resources, and handle any necessary interactions with the hardware.
1. **VM Control Block (VMCB):** The hypervisor uses a data structure called the VM Control Block (VMCB) to manage the state of each VM. The VMCB stores information about the VM's registers, memory mappings, and other settings, allowing the hypervisor to quickly switch between different VMs.
1. **VM Entry and VM Exit:** These are crucial operations that manage the transitions between the hypervisor and the VMs. A "VM Entry" occurs when the hypervisor switches the CPU from host mode to guest mode, starting or resuming a VM's execution. A "VM Exit" occurs when the VM needs to perform an operation that the hypervisor needs to handle (e.g., I/O requests, privileged instructions, or interrupts). The CPU automatically switches back to host mode, giving the hypervisor control.
1. **Extended Page Tables (EPT) / Nested Page Tables (NPT):** These features enhance memory virtualization. They allow the hypervisor to manage the guest OS's memory translations more efficiently, reducing overhead and improving memory access performance within the VMs. They essentially create a "shadow" page table for each VM, enabling the hypervisor to control memory access without constantly interrupting the VM.


**The Process: A Detailed Look**

1. **VM Startup:** When a VM is started, the hypervisor sets up the VMCB for that VM, configuring its initial state and memory mappings.
1. **VM Entry:** The hypervisor performs a VM Entry, transitioning the CPU to guest mode and starting the VM's execution.
1. **Direct Execution:** The VM now runs directly on the CPU in guest mode. Many instructions can be executed without any intervention from the hypervisor, significantly reducing overhead.
1. **VM Exit:** When the VM encounters an instruction or event that requires hypervisor intervention, the CPU automatically triggers a VM Exit. This switches the CPU back to host mode, and the hypervisor takes control.
1. **Hypervisor Handling:** The hypervisor examines the reason for the VM Exit and performs the necessary action. This might involve emulating a hardware device, handling a privileged instruction, or managing memory access.
1. **VM Entry (Return):** Once the hypervisor has handled the event, it performs another VM Entry to return control to the VM, allowing it to continue execution.

**Benefits Revisited:**

- **Near-Native Performance:** VMs achieve performance much closer to that of running directly on the hardware.
- **Reduced Overhead:** The CPU handles many virtualization tasks, reducing the load on the hypervisor.
- **Improved Scalability:** More VMs can be run on a single physical server.
- **Enhanced Stability and Security:** Better isolation and resource management improve the stability and security of the virtualized environment.

**Conclusion:**

Hardware-assisted virtualization has revolutionized server virtualization. By leveraging CPU features, it has made full virtualization practical and efficient, enabling the widespread adoption of cloud computing, data center virtualization, and other virtualization-dependent technologies. It's the reason why VMs can perform so well today, running demanding applications with minimal performance penalty.





