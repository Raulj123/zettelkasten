# What is a Virtual Machine?
* A Virtual Machine (VM) is a virtual environment that functions as a virtual computer system with its own CPU, memory, network interface, and storage, created on a physical hardware system
* A software called a hypervisor separates the machine's resources from the hardware and provisions them appropriately so they can be used by the VM
* VMs are isolated from the rest of the system, and multiple VMs can exist on a single piece of hardware, like a server
* Working on the hardware level

# What is a Hypervisor?
* Virtual Machine Monitor (VMM), isolates the operating system and resources from the virtual machines and enables the creation and management of those VMs

# Why use a virtual machine?
*  Most operating system and application deployments only use a small amount of the physical resources available
* By virtualizing our servers, we can place many virtual servers onto each physical server to improve hardware utilization
* provides an environment that is isolated from the rest of a system, so whatever is running inside a VM won't interfere with anything else running on the host hardware

# What is a Container?
* A container is a standard unit of software that packages up code and all its dependencies such as specific versions of runtimes and libraries so that the application runs quickly and reliably from one computing environment to another
* applications can be abstracted from the environment in which they actually run

# Why do we need them?
**Separation of responsibility**
Containerization provides a clear separation of responsibility, as developers focus on application logic and dependencies, while operations teams can focus on deployment and management.

**Workload portability**
Containers can run virtually anywhere, greatly easing development and deployment.

**Application isolation**
Containers virtualize CPU, memory, storage, and network resources at the operating system level, providing developers with a view of the OS logically isolated from other applications.

**Agile development**
Containers allow developers to move much more quickly by avoiding concerns about dependencies and environments.

**Efficient operations**
Containers are lightweight and allow us to use just the computing resources we need.

# VM's vs Containers 
In traditional virtualization, a hypervisor virtualizes physical hardware. The result is that each virtual machine contains a guest OS, a virtual copy of the hardware that the OS requires to run, and an application and its associated libraries and dependencies.

Instead of virtualizing the underlying hardware, containers virtualize the operating system so each container contains only the application and its dependencies making them much more lightweight than VMs. Containers also share the OS kernel and use a fraction of the memory VMs require.