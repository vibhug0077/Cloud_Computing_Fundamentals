### **IBM Mainframe Virtualization**

#### **Introduction** 

**What is IBM Mainframe Virtualization?**

IBM mainframe virtualization refers to the technology that allows a single physical IBM mainframe to run multiple virtual machines (VMs), each operating as an independent system with its own operating system, applications, and resources. It maximizes resource utilization, reduces costs, and enhances flexibility by partitioning a mainframe’s hardware into isolated environments.

![IBM Virtualization](/images/Architecture%20of%20IBM%20Z%20Virtualization.png)

**Historical Evolution**

* **1964: System/360** \- IBM introduced the System/360, the first modern mainframe, laying the groundwork for virtualization by separating hardware and software.  
* **1964: CP/CMS** \- Alongside System/360, IBM launched CP/CMS, featuring the first hypervisor (Control Program-40, or CP-40), enabling virtual machines to share resources efficiently.  
* **1972: VM/370** \- IBM released VM/370, the first commercially available OS with built-in virtualization, marking a milestone in mainframe virtualization.  
* **1980s-1990s: Expansion** \- Virtualization evolved with systems like VM/SP and VM/ESA, supporting more complex workloads and architectures.  
* **2000s-Present: z/VM and Modernization** \- The z/VM operating system became IBM’s flagship hypervisor, supporting Linux, z/OS, and other workloads on IBM Z systems, integrating with cloud and AI technologies.

**Key Concepts**

* **Hypervisor**: Software that creates and manages VMs. IBM uses both Type 1 (bare-metal, e.g., PR/SM) and Type 2 (software-based, e.g., z/VM) hypervisors.  
* **Logical Partitions (LPARs)**: Hardware-level partitions managed by PR/SM, dividing a mainframe into isolated environments.  
* **Virtual Machines**: Software-defined systems running on LPARs or z/VM, each with virtualized CPU, memory, and I/O.  
* **Backward Compatibility**: IBM Z systems maintain compatibility with System/360, allowing decades-old applications to run on modern virtualized platforms.

**Core Technologies**

* **PR/SM (Processor Resource/System Manager)**: A Type 1 hypervisor embedded in IBM Z hardware, enabling LPARs with high security and performance.  
* **z/VM**: A Type 2-like hypervisor (runs on LPARs), offering scalable virtualization for thousands of VMs, supporting Linux, z/OS, z/VSE, and z/TPF.  
* **z/OS**: IBM’s flagship mainframe OS, often run in VMs for mission-critical workloads, enhanced by virtualization for efficiency.

**Benefits of IBM Mainframe Virtualization**

* **Resource Efficiency**: Shares CPU, memory, and I/O across VMs, reducing hardware costs and energy use compared to physical servers.  
* **Scalability**: z/VM can run hundreds to thousands of VMs on one system, ideal for large-scale enterprise needs.  
* **Security**: Certified at high levels (e.g., EAL5+ for PR/SM), virtualization isolates workloads, enhancing data protection.  
* **Cost Savings**: Leverages zIIP processors for offloading workloads, minimizing general-purpose processor usage and licensing costs.  
* **Reliability**: Hot-swappable hardware and zero-downtime design (hence “Z” for zero downtime) ensure continuous operation.

**Key Use Cases**

* **Banking and Finance**: Processes massive transaction volumes (e.g., credit card payments, ATMs) with real-time reliability and security.  
* **Government**: Supports critical services (e.g., law enforcement, tax systems) with high availability and resilience.  
* **Cloud Integration**: Runs Linux VMs for hybrid cloud strategies, connecting mainframes to modern platforms.  
* **Development and Testing**: IBM ZD\&T (Z Development and Test) emulates z/OS on x86 or cloud for DevOps, accelerating innovation.

**Modern Relevance**

* **IBM Z Systems**: The latest IBM z16 (released 2022\) integrates AI and quantum-safe cryptography, with virtualization as a core feature via PR/SM and z/VM.  
* **Hybrid Cloud**: z/VM supports Red Hat OpenShift, linking mainframes to cloud ecosystems for agility and modernization.  
* **Data Virtualization**: Tools like IBM Data Virtualization Manager for z/OS provide virtual access to mainframe data without moving it, aiding analytics and API-driven applications.  
* **Market Growth**: The global mainframe market, valued at $2.9B in 2022, is projected to reach $5.6B by 2032, driven by virtualization’s role in digital transformation.

**Challenges and Considerations**

* **Complexity**: Managing LPARs and VMs requires specialized skills, though tools like IBM ZD\&T simplify access.  
* **Cost**: Initial investment is high, but long-term savings offset this for large enterprises.  
* **Skill Gap**: Demand for mainframe expertise grows as legacy knowledge retires, necessitating training.

IBM mainframe virtualization, pioneered over 60 years ago, remains a cornerstone of enterprise IT. Its ability to handle massive, secure, and reliable workloads while adapting to modern cloud and AI demands ensures its continued relevance. From System/360 to z16, it exemplifies innovation rooted in efficiency and resilience.

## **IBM PowerVM Virtualization**

**What is PowerVM?**

IBM PowerVM is a virtualization platform for IBM Power Systems servers. It allows you to create multiple virtual machines (VMs) or logical partitions (LPARs) on a single physical server, each running its own operating system (OS) and applications. This improves resource utilization, reduces costs, and simplifies management.

**Key Features:**

* **Logical Partitioning (LPARs):** Divides a physical server into multiple isolated environments, each with its own dedicated resources (CPU, memory, I/O).  
* **Virtual Machines (VMs):** Provides a more flexible virtualization approach, allowing for dynamic resource allocation and easier management.  
* **Virtual I/O:** Enables sharing of physical I/O devices (disk, network) among multiple LPARs or VMs.  
* **Live Partition Mobility:** Allows moving running LPARs between physical servers without downtime.  
* **PowerVM Editions:** Different editions (Express, Standard, Enterprise) offer varying features and capabilities to meet different needs.

**Benefits of PowerVM:**

* **Improved Resource Utilization:** Consolidate workloads onto fewer physical servers, maximizing hardware investment.

* **Reduced Costs:** Lower hardware, software, and energy costs.

* **Simplified Management:** Centralized management of virtual resources.

* **Increased Flexibility:** Easily create, modify, and delete LPARs or VMs as needed.

* **Enhanced Availability:** Live Partition Mobility and other features improve application availability.

**PowerVM Components:**

* **POWER Hypervisor:** The core virtualization layer that manages and isolates LPARs and VMs.

* **Virtual I/O Server (VIOS):** A special-purpose LPAR that provides virtual I/O services to other LPARs or VMs.

* **Hardware Management Console (HMC):** A dedicated system used to manage PowerVM and Power Systems servers.

* **Integrated Virtualization Manager (IVM):** A simplified web-based interface for managing PowerVM on smaller systems.

**PowerVM Editions Comparison:**

| Feature | Express | Standard | Enterprise |
| ----- | ----- | ----- | ----- |
| Max. Concurrent VMs | 2 per server | 20 per core (up to 1000\) | 20 per core (up to 1000\) |
| Virtual I/O Server | Yes | Yes | Yes |
| NPIV | No | Yes | Yes |
| Live Partition Mobility | No | No | Yes |

**Use Cases:**

* **Server Consolidation:** Reduce the number of physical servers by running multiple workloads on a single system.

* **Development and Testing:** Create isolated environments for development and testing new applications.

* **High Availability:** Use Live Partition Mobility to move critical applications to a different server in case of hardware failure.

* **Cloud Computing:** PowerVM can be used as the foundation for building a private cloud infrastructure.

IBM PowerVM is a powerful and versatile virtualization platform that can help organizations improve IT efficiency, reduce costs, and enhance application availability. It offers a wide range of features and capabilities to meet the needs of different environments, from small businesses to large enterprises.

### **Extending Virtualization to x86: Content Notes**

#### **Introduction and Background**

**Overview of Virtualization**

Virtualization allows multiple operating systems (OS) to run on a single physical machine by abstracting hardware resources.

* Key benefits: improved resource utilization, isolation, scalability, and cost efficiency.  
* Traditionally implemented on mainframes (e.g., IBM System/360) but faced challenges on x86 architecture.

**The x86 Architecture Challenge**

* x86 (Intel/AMD processors) dominates personal and server computing.  
* Pre-virtualization hurdles:

  * Non-virtualizable instruction set: certain privileged instructions (e.g., POPF, PUSHF) didn’t trap when executed in user mode, breaking isolation.  
  * Lack of hardware support for memory management and CPU state separation.  
* Early solutions relied on software emulation (e.g., VMware binary translation), which was slow and complex.

**Motivation for Extending Virtualization to x86**

* Demand for server consolidation and multi-OS environments in the late 1990s/early 2000s.  
* Need for efficient, secure, and scalable virtualization on commodity hardware.  
* Goal: enable hardware-assisted virtualization to overcome software-only limitations.

**Key Milestones**

* 2005-2006: Intel VT-x (Virtualization Technology) and AMD-V (AMD Virtualization) introduced.  
* These extensions added hardware support to x86, revolutionizing virtualization.

![X86 Virtulization Workflow](/images/x86%20Virtualization%20Workflow.png)

#### 

#### **Technical Details** 

**Hardware Extensions in Depth**

* **Intel VT-x**:

  * Introduced VMX (Virtual Machine Extensions) operation modes: VMX root (hypervisor) and VMX non-root (guest).

  * New instructions: VMENTER, VMEXIT, VMLAUNCH, VMRESUME.

  * VMCS (Virtual Machine Control Structure) for managing guest state transitions.

![Intel VT-x](/images/Intel%20VT-x.png)

* **AMD-V**:

  * Similar to VT-x, with SVM (Secure Virtual Machine) architecture.

  * Instructions like VMRUN, VMLOAD, VMSAVE.

  * Nested paging for efficient memory virtualization (contrast to Intel’s EPT \- Extended Page Tables).

* Both reduced overhead by trapping privileged instructions directly in hardware.

**Memory Virtualization**

* Pre-extensions: Shadow page tables managed by hypervisors (slow, memory-intensive).

* Post-extensions: Hardware-assisted memory virtualization (EPT/Nested Paging) maps guest-physical to host-physical addresses directly.

* Improves performance for memory-intensive workloads.

**Benefits of x86 Virtualization Extensions**

* Performance: Near-native speeds for virtual machines (VMs).

* Simplicity: Reduced reliance on complex software techniques (e.g., paravirtualization).

* Security: Better isolation between VMs and hypervisor.

* Flexibility: Support for unmodified guest OSes (e.g., Windows, Linux).

**Challenges and Considerations**

* Initial adoption required new hardware, limiting legacy support.

* Overhead still exists for I/O virtualization (addressed later by VT-d/AMD-Vi for direct device passthrough).

* Complexity in hypervisor design to leverage extensions effectively.

**Context**

* x86 virtualization is foundational to cloud computing (AWS, Azure, GCP).

* Evolving with containerization (e.g., Docker, Kubernetes) and hybrid virtualization models.

* Ongoing enhancements: better power management, security (e.g., Intel TDX, AMD SEV), and support for AI workloads.

### **Hardware Support for x86 Virtualization**

**Introduction to Hardware Support**

Virtualization on x86 architectures initially depended on software-based techniques such as binary translation and paravirtualization, which, while functional, suffered from significant inefficiencies in performance and resource utilization. These early methods struggled to fully leverage the underlying hardware, prompting the development of dedicated hardware support to overcome these limitations. This evolution paved the way for more efficient, secure, and scalable virtual machines (VMs), transforming virtualization into a cornerstone of modern computing. Leading the charge, Intel introduced VT-x in 2005, followed closely by AMD with AMD-V in 2006, marking a pivotal shift toward hardware-assisted virtualization that revolutionized the technology's capabilities and adoption.

**Why Hardware Support Was Needed**

* x86 architecture wasn’t inherently virtualizable:

  * Privileged instructions (e.g., POPF, CLI) didn’t trap in user mode, violating Popek and Goldberg virtualization requirements.  
  * No native support for CPU state isolation or memory management.

* Software-only solutions incurred high performance overhead and complexity.

**Intel VT-x (Virtualization Technology)**

* **Core Features**:

  * VMX (Virtual Machine Extensions) modes: VMX root (hypervisor) and VMX non-root (guest).  
  * New instructions: VMLAUNCH, VMRESUME (start VM), VMEXIT (return to hypervisor), VMCALL (guest-hypervisor communication).  
  * VMCS (Virtual Machine Control Structure): A data structure in memory to manage CPU state, interrupts, and transitions.

* **Operation**:

  * Hypervisor runs in VMX root mode, guests in VMX non-root.  
  * Sensitive instructions trap to hypervisor via VMEXIT, processed, then returned via VMENTER.

* **Benefits**: Hardware handles transitions, reducing software overhead.

**AMD-V (AMD Virtualization)**

* **Core Features**:

  * SVM (Secure Virtual Machine) architecture.  
  * Instructions: VMRUN (execute VM), VMLOAD/VMSAVE (state management), VMMCALL (guest-hypervisor calls).  
  * VMCB (Virtual Machine Control Block): Similar to VMCS, controls guest execution.

* **Operation**:

  * Similar trap-and-emulate model to VT-x, streamlined for AMD processors.

* **Unique Aspect**: Early adoption of nested paging (see below).

**Memory Virtualization Support**

* **Pre-Hardware Issue**: Hypervisors used shadow page tables to translate guest-virtual to host-physical addresses—slow and resource-heavy.

* **Intel EPT (Extended Page Tables)**:

  * Hardware-managed second-level address translation (guest-physical to host-physical).  
  * Reduces hypervisor intervention, boosts performance.

* **AMD Nested Paging**:

  * Equivalent to EPT, introduced with AMD-V.  
  * Direct mapping of guest memory, minimizing overhead.

* **Impact**: Critical for memory-intensive workloads (databases, cloud servers).

**I/O Virtualization Enhancements**

* **Intel VT-d (Virtualization Technology for Directed I/O)**:

  * Adds DMA (Direct Memory Access) remapping and interrupt remapping.  
  * Enables direct device passthrough to VMs (e.g., GPUs, NICs).

* **AMD-Vi (IOMMU)**:

  * Similar I/O virtualization support for AMD systems.

* **Benefit**: Near-native I/O performance for VMs.

**Additional Hardware Features**

* **Interrupt Virtualization**: Hardware handles interrupt delivery to VMs (e.g., Intel APICv, AMD AVIC).

* **Security Enhancements**:

  * Intel TDX (Trust Domain Extensions) and AMD SEV (Secure Encrypted Virtualization) encrypt VM memory.  
  * Protects against physical attacks and hypervisor breaches.

* **Performance Optimizations**: Reduced latency for VM exits/entries, better power management.

**Benefits of Hardware Support**

* **Performance**: Near-native execution speeds for VMs.  
* **Simplicity**: Eliminates need for complex software workarounds.  
* **Compatibility**: Runs unmodified guest OSes (e.g., Windows, Linux).  
* **Scalability**: Enables cloud-scale deployments (e.g., AWS EC2, Azure VMs).

**Current State** 

* Hardware support is standard in all modern x86 CPUs (Intel Core, AMD Ryzen, EPYC, Xeon).  
* Continual evolution: support for AI accelerators, confidential computing, and tighter integration with container runtimes.  
* Challenges: Balancing security (e.g., mitigating side-channel attacks like Spectre) with performance.

![IO Virtualization](/images/I_O%20Virtualization%20with%20VT-d_AMD-Vi.png)
