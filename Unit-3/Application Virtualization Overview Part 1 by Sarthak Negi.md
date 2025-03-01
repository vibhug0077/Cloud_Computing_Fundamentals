**Application Virtualization Overview**

**What is application virtualization?**

Application virtualization is the process of abstracting (or separating)
an application from the underlying computer hardware it is stored on.
Virtualizing an application allows an organization's employees to access
that application from almost any device and any location as long as they
have an internet connection. While users don't have to physically
install the application on their devices, they can still interact with
the application almost as if they did have it installed.

There are a couple ways to create a virtual application - one is through
application virtualization and the other is through desktop
virtualization. With desktop virtualization, or virtual desktop
infrastructure (VDI), the apps run on servers in an organization's
datacenter and users' entire desktops, including operating systems, are
accessed remotely via a range of devices. These apps can be considered
"virtual" because they aren't actually installed on each user's physical
device. Also, the virtualized desktops (including apps) are typically
stored on virtual machines that are controlled by a hypervisor.

Application virtualization also makes it possible to access apps
remotely on any device. But in contrast to VDI, app virtualization only
virtualizes an application, not the surrounding operating system and
other components. These virtualized apps are essentially streamed to
user devices. Where VDI virtualizes applications and operating systems,
application virtualization just virtualizes the application itself.

**How does application virtualization work**

Simply put, application virtualization "tricks" a typical application
into acting as if it's connected to a remote device's operating system
when it isn't. What makes it work is a layer of virtualization between
the application and the OS of the user's remote device. The
virtualization layer acts as a piece of the runtime environment and
diverts files and registry log modifications to a separate executable
file instead of dispersing that data across the underlying OS. The
executable file is stored on the host server as an image, which means
end user devices are not at risk of vulnerabilities or other security
issues because the application's data isn't stored there.

Because all the data is kept in a single file, doesn't affect the OS
it's running on, and remains "invisible" to the other applications and
systems on the user's remote device, application virtualization can be
used on a range of devices - and applications that were incompatible
with each other can now run on the same device.

When a user works within a virtualized application, any changes they
make to new data they input is saved back at the hosting server's
location where the actual application resides. The remote delivery of
the application allows IT to maintain and manage applications in a
single, centralized location and also simplifies the processes of
patching and updating because they only have to update the application
once and when users access it, they'll be accessing the latest version.

While application virtualization and desktop virtualization are often
referred to as similar processes, they are not the same thing. As
mentioned above, desktop virtualization through VDI delivers a flexible
and more complete remote desktop user experience. Virtualizing specific
apps instead of entire desktop environments can be more cost-effective
for organizations with significant demand for a single application.
Application virtualization can also be a component of a more
comprehensive desktop virtualization process.

**Benefits of application virtualization**

There are many benefits of application virtualization:

-   **Simple installation and deployment** -- An application is only
    installed once on the host server and then deployed remotely through
    the distribution of an .exe file to user devices.

-   **Easy, centralized management** -- IT can oversee many applications
    for thousands of users from a single centralized location.

-   **Increased flexibility and scalability** -- Eliminate the time and
    effort spent installing applications many times to hundreds or
    thousands of end devices. As new employees are onboarded, they
    simply need to be given remote access to already installed apps.

-   **Mobility support** -- Virtualized applications supports mobility
    and portability; in fact, some devices can't handle a full remote
    desktop environment, but almost every device can handle a
    virtualized app.

-   **Reduced potential for system crashes** -- Virtualized apps can run
    alongside apps they might not naturally be compatible with. Plus,
    technical issues with a virtualized app can be handled by IT from
    the centralized server location.

-   **Enhanced security through isolation** -- Apps that run virtually
    are isolated from each other, so if one application is compromised
    through attack or malfunction, the others aren't automatically
    compromised as well. Also, if a device is lost or stolen, the
    application data is still safe because it isn't stored on devices -
    it's stored on the host server.

-   **Better control over access** -- IT has better control over who can
    access which applications because they can simply deny access
    permissions to users who are no longer authorized or have left the
    company - without having to uninstall actual software from the
    user's device.

-   **Fast, easy access to critical apps on the go** -- Remote users can
    get immediate access to the apps they need to do their jobs. No
    waiting for installation or long load times.

-   **Simpler compliance to regulations** -- Because data isn't stored
    on devices, organizations can maintain compliance with security and
    privacy regulations such as Health Insurance Portability and
    Accountability Act (HIPAA) and Payment Card Industry Data Security
    Standards (PCI-DSS).

-   **Ability to run legacy apps alongside today's advanced
    apps** -- [Virtualization](https://www.nutanix.com/info/virtualization) allows
    organizations to run legacy apps even when they wouldn't be
    compatible with more modern applications. This is important because
    many organizations, especially those in highly regulated industries
    such as finance and healthcare, still rely heavily on legacy
    applications.

-   **Fast, intuitive incident resolution **-- IT can easily roll back
    an application to a previous state if data gets corrupted or an
    attacker infiltrates the system. This makes it simpler to respond to
    incidents and keep operations running after an attack.

-   Reduced performance issues -- When devices get "bloated" with too
    many applications, performance can take a nosedive. By keeping
    applications stored on a host server and delivering them remotely,
    users' devices won't slow down or crash from too many apps.

**Who benefits from app virtualization?**

Application virtualization delivers benefits to many people across an
organization:

**End users**

End users of virtualized applications have the freedom to use the
devices they prefer and the flexibility to work where and when they
want - with easy remote access to the business-critical systems they
need to do their jobs. With remote, virtualized apps, employees can
switch devices at will and don't have to worry about security issues or
installation or maintenance hassles. They get all the advantages of
remote access to applications with none of the downside of having to
manage them.

**IT admins**

Application virtualization reduces the application deployment and
management burden for IT. Instead of having to install software on
hundreds or thousands of devices - and then making sure to patch and
upgrade each one when needed - IT can simply deploy an application on a
host server and make it remotely available to authorized users when
needed. They have a single, centralized location for applications and
can manage and maintain those apps much faster and more efficiently.
Some studies have shown that app virtualization can also result in fewer
support tickets, as users don't have software to worry about on their
devices. Implementing security and configuring policies is easier and
more streamlined in a centralized location as well. And decommissioning
apps or removing employee access permissions can also be done easily.

**Developers**

Application virtualization benefits software and app developers because
it makes resources more accessible. IT can virtualize several apps and
environments on the same system so teams can test their software on
various OS versions or systems and make improvements as needed. With
virtualization, developers can also safely access or test files that
might be contaminated or corrupted because the virtualization layer
separates the application from the OS and contamination won't be able to
infiltrate the entire system.

**Organizations**

Thanks to application virtualization, organizations can implement BYOD
initiatives simply and securely, and no longer have to provide
corporate-owned devices for employee use. That can help keep costs down.
Costs are also reduced when it comes to IT workloads - now that IT teams
don't have to spend most of their time installing and managing software
on many individual devices. Streamlined IT management can translate into
real savings for an organization. The company can accomplish more with a
smaller staff and lower capital expenditures for multiple copies of
software. Organizations can also benefit from providing employees easy,
secure access to apps where and when they need them. That keeps workers
productive and efficient, which also can have a real effect on any
company's bottom line.
