**NETWORK VIRTUALIZATION.**

**Introduction**

Network Virtualization is a process of logically grouping physical
networks and making them operate as single or multiple independent
networks and these independent networks are called Virtual Networks. In
this form of virtualization all hardware and software in the virtual
network appear as a single collection of resource. This innovative
approach enables all hardware and software components within the virtual
network to function as a cohesive collection of resources, streamlining
management and enhancing efficiency. Network virtualization supports
automation, reduces hardware costs, and simplifies network management,
making it a fundamental technology in cloud computing, enterprise
networking, and telecommunication industries. Network virtualization is
not a completely new concept but it has been in use to limited extent
such as Virtual Private Networks (VPNs) & virtual local area networks
(VLANs).

**Key Features Of Network Virtuaization**

1.  **Partitioning:** Network virtualization enables the creation of
    multiple **Logical Network Partitions** over a shared physical
    infrastructure. The re-configurability capability of Network
    virtualization makes the logical partitions capable of easily and
    rapidly creating network topologies and reconfiguration according to
    users' requirements, the status of networks, policies of resource
    owners, etc.

2.  **Isolation:** One of the critical aspects of network virtualization
    is **strong isolation between virtual networks**. This includes the
    isolation to deterioration of the performance of a logical partition
    due to exhaustion of network resource by a malicious logical
    partition.

3.  **Abstraction:** Network abstraction allows hiding the underlying
    characteristics of network elements from the way in which other
    network elements, applications, or 3 users interact with those
    network elements and separates infrastructure instances and control
    frameworks of network virtualization. This abstraction simplifies
    network management, enabling applications and users to operate
    seamlessly without being affected by hardware configurations or
    network topology changes.

4.  **Aggregation:** Multiple network resources can be combined into a
    single, high-performance resource pool. It enhances network
    efficiency by distributing workloads more effectively, improving
    overall performance, and optimizing resource usage.

**Architecture Of Network Virtualization**

Network virtualization is designed to create multiple **Logically
Isolated Network Partitions (LINPs)** over a shared physical
infrastructure. Each LINP is isolated from each other and is
programmable to satisfy the user's demand on the functionality and
amount. Users' demand is conveyed to an entity known as LINP manager
which coordinates infrastructures resource so that appropriate LINP is
provided to the user as per the user's demand.

The LINP Manager is responsible for:

-   Allocating network resources to different virtual networks.

-   Ensuring that each LINP remains isolated from others.

-   Handling user requests for network customization.

-   Monitoring and optimizing network performance.

This architecture is used in **cloud computing, enterprise networks, and
data centres** to improve operational efficiency and security.

**Benefits Of Network Virtualization**

Virtualization technology offers a unique opportunity for organizations
to enhance **efficiency, scalability, and cost-effectiveness** while
simplifying network management. It provides an efficient way to
centrally manage network resources, simplifying provisioning and
maintenance tasks.

Virtual Networks attempt to better utilize networking infrastructure by
reusing individual routers or links. Additionally, resources can be
**aggregated** to improve network performance, enhance fault tolerance,
and provide redundancy for critical services.

Network virtualization when done at the device level minimizes the need
for additional physical hardware by consolidating network functions. And
when done at the network level it enables multiple logical networks to
operate within a single physical infrastructure, optimizing resource
allocation and improving overall network performance.

**In brief, following are some of the benefits of network
virtualization-**

a.  Enables multiple virtual networks to function independently over
    shared infrastructure.

b.  It provides paths to the future network approaches.

c.  It reduces cost of ownership.

d.  Enhances resource utilization by ensuring optimal use of network
    infrastructure.

e.  Modernizes network architecture by introducing greater flexibility
    and efficiency.

**Areas Of Concern**

-   **Isolation:** Providing secure isolation among the network services
    is an important issue. Performance issues in one virtual network
    should not impact others sharing the same infrastructure. For
    example, as multiple network services coexist over shared physical
    infrastructures, performance problems in a service may spread out
    over the whole network and may cause performance degradation of
    other services.

-   **Flexibility:** Some legacy systems and traditional network designs
    may lack support for virtualization technologies, limiting
    flexibility.

-   **Management:** Since each virtual network is independent from other
    virtual networks, it has to be managed independently from other
    virtual networks. If isolation is not properly implemented, managing
    multiple virtual networks can become challenging and
    resource-intensive.

-   **Security:** Malfunctions, misconfigurations, or vulnerabilities in
    one virtual network must not compromise the security of others.
    Unauthorized access or breaches could expose sensitive data if
    virtualized environments are not properly secured.

**Implementation Example**

**Router architecture for virtualization support.**

To support virtualization capability, the router architecture has three
layers viz. router hardware, router software, and control framework
layer.

figure below shows the architecture of router which supports
virtualization.

The router hardware typically consists of a switching component for
packet forwarding and flow table, and the router software is responsible
for running routing protocols, building routing tables, and managing
network traffic.

The software part includes virtualization layer which allows router to
support virtualization. This layer creates and manages logically
isolated virtual systems, which runs various components on native
hardware thus, the virtualization layer can support virtualization of
router hardware resources by creating the isolated virtual systems, i.e.
virtual router.

The virtual router is nothing but the software implementation of a
router that executes the same operations as a physical router. We can
say that its an isolated partition of a real router. Multiple virtual
routers can coexist over the virtualization layer and each virtual
router is completely isolated from the others.

The control framework acts as an interface/communicator between the
virtual or physical router and other network entities. It performs the
interaction between the virtual and physical router. Control framework
defines interfaces, message types including basic protocols and required
functions, message flows between router and network entities. these
network entities include elements such as routers, switches, etc. it can
also include logical entities like user information, registry for
managing of LINPs, network resources.
