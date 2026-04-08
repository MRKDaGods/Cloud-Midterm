# Lecture 2 — Virtualization
## Unified Questions and Answers

Each question is followed by its answer and topic from the answer key.

### Section 1: Virtual Machines & Why Virtualization

**Q1.** A Virtual Machine (VM) is best described as:
- A) A physical server dedicated to one application
- B) Software that runs applications and is not tied to a physical machine
- C) A hardware component that simulates network traffic
- D) An OS installed directly on bare-metal hardware


**Answer:** **B** — Software that runs applications, not tied to a physical machine
**Topic:** VM Definition

---

**Q2.** Which of the following is a key property of a VM regarding its operating system?
- A) It shares the host OS kernel
- B) It has no operating system
- C) It has its own independent Guest OS
- D) It must run the same OS as the host


**Answer:** **C** — It has its own independent Guest OS
**Topic:** VM Properties

---

**Q3.** Virtualization is considered the foundation of cloud services and is referred to as:
- A) Cloud v2.0
- B) Cloud v1.0
- C) Cloud v3.0
- D) Cloud Legacy


**Answer:** **B** — Cloud v1.0
**Topic:** Why Virtualization

---

**Q4.** Which of the following is NOT listed as a benefit of virtualization?
- A) Hide hardware details
- B) Deploy any configuration
- C) Increase physical hardware costs
- D) Reduce set-up time


**Answer:** **C** — Increase physical hardware costs
**Topic:** Why Virtualization

---

**Q5.** Virtualization allows multiple jobs to share the same resource. This primarily helps with:
- A) Increasing power consumption
- B) Resource utilization and efficiency
- C) Reducing network bandwidth
- D) Replacing the need for an OS


**Answer:** **B** — Resource utilization and efficiency
**Topic:** Why Virtualization

---

### Section 2: Virtualization Concepts & Terminology

**Q6.** The term "Host Machine" in virtualization refers to:
- A) The virtual machine running a guest OS
- B) The physical machine
- C) The hypervisor software layer
- D) Any machine running Docker


**Answer:** **B** — The physical machine
**Topic:** Terminology

---

**Q7.** The "Guest Machine" in virtualization refers to:
- A) The physical server
- B) The VMM software
- C) The virtual machine created through virtualization
- D) The host OS


**Answer:** **C** — The virtual machine created through virtualization
**Topic:** Terminology

---

**Q8.** A "Hypervisor" is also known as:
- A) Guest OS
- B) Host Machine
- C) Virtual Machine Monitor (VMM)
- D) Kernel Module


**Answer:** **C** — Virtual Machine Monitor (VMM)
**Topic:** Terminology

---

**Q9.** What is the primary role of the Hypervisor?
- A) Run user applications directly on hardware
- B) Replace the physical network card
- C) Create and manage virtual environments
- D) Provide internet connectivity to VMs


**Answer:** **C** — Create and manage virtual environments
**Topic:** Hypervisor Role

---

**Q10.** Which of the following is NOT a function of the Hypervisor (VMM)?
- A) Identify, capture, and respond to CPU instructions and HW requests
- B) Schedule VM requests queue
- C) Compile guest OS source code
- D) Return physical machine processing results to corresponding VM


**Answer:** **C** — Compile guest OS source code
**Topic:** Hypervisor Functions

---

**Q11.** The Hypervisor can be described as:
- A) A lightweight container runtime
- B) A complete OS for controlling VMs and resource sharing
- C) A network protocol for VM migration
- D) A physical add-on card


**Answer:** **B** — A complete OS for controlling VMs and resource sharing
**Topic:** Hypervisor

---

### Section 3: Virtualization Types (Type 1 vs Type 2)

**Q12.** In Bare-Metal Virtualization (Type 1), the VMM runs:
- A) On top of a Host OS
- B) Inside a container
- C) Directly on the hardware
- D) Inside the Guest OS


**Answer:** **C** — Directly on the hardware
**Topic:** Type 1

---

**Q13.** In Hosted Virtualization (Type 2), the VMM runs:
- A) Directly on the hardware
- B) As a common application on top of a Host OS
- C) Inside the Guest OS kernel
- D) As a hardware driver


**Answer:** **B** — As a common application on top of a Host OS
**Topic:** Type 2

---

**Q14.** Which virtualization type is best suited for large resource-intensive workloads?
- A) Hosted Virtualization (Type 2)
- B) Container-based virtualization
- C) Bare-Metal Virtualization (Type 1)
- D) Paravirtualization only


**Answer:** **C** — Bare-Metal Virtualization (Type 1)
**Topic:** Virt Types

---

**Q15.** Which virtualization type is best suited for desktop and development environments?
- A) Bare-Metal Virtualization (Type 1)
- B) Hosted Virtualization (Type 2)
- C) Hardware-assisted virtualization
- D) Full virtualization only


**Answer:** **B** — Hosted Virtualization (Type 2)
**Topic:** Virt Types

---

**Q16.** Bare-Metal Virtualization (Type 1) requires:
- A) Basic user knowledge
- B) No technical knowledge
- C) System administrator-level knowledge
- D) Only Docker knowledge


**Answer:** **C** — System administrator-level knowledge
**Topic:** Type 1

---

**Q17.** Which of the following is an example of Bare-Metal Virtualization (Type 1)?
- A) VirtualBox
- B) VMware Workstation
- C) Hyper-V
- D) QEMU standalone


**Answer:** **C** — Hyper-V
**Topic:** Type 1 Examples

---

**Q18.** Which of the following is an example of Hosted Virtualization (Type 2)?
- A) KVM
- B) Xen
- C) Hyper-V
- D) VirtualBox


**Answer:** **D** — VirtualBox
**Topic:** Type 2 Examples

---

### Section 4: Virtualization Characteristics

**Q19.** The "Partitioning" characteristic of virtualization means:
- A) Splitting the network into VLANs
- B) Allocating server resources to multiple VMs to prevent overuse
- C) Dividing the hard disk into multiple file systems
- D) Separating kernel mode from user mode


**Answer:** **B** — Allocating server resources to multiple VMs to prevent overuse
**Topic:** Partitioning

---

**Q20.** In the Partitioning characteristic, each VM can only access:
- A) All physical hardware directly
- B) The host OS kernel
- C) Its virtual HW quota provided by the VMM
- D) The hypervisor's complete memory space


**Answer:** **C** — Its virtual HW quota provided by the VMM
**Topic:** Partitioning

---

**Q21.** If a Linux VM crashes due to a driver failure while a Mac OS VM runs on the same host, the Mac OS VM:
- A) Also crashes due to shared kernel
- B) Is not affected due to Isolation
- C) Slows down significantly
- D) Must be restarted by the hypervisor


**Answer:** **B** — Is not affected due to Isolation
**Topic:** Isolation

---

**Q22.** The "Encapsulation" characteristic means a VM is stored as:
- A) A single binary executable file
- B) A group of HW-independent files (e.g., .vbox, .vdi)
- C) A network packet stream
- D) A compressed tar archive only


**Answer:** **B** — A group of HW-independent files (e.g., .vbox, .vdi)
**Topic:** Encapsulation

---

**Q23.** VM migration is enabled by which virtualization characteristic?
- A) Partitioning
- B) HW Independence
- C) Isolation
- D) Encapsulation


**Answer:** **D** — Encapsulation
**Topic:** VM Migration

---

**Q24.** The "HW Independence" characteristic means a VM can be migrated to another host as long as:
- A) The physical CPUs are identical
- B) The same Guest OS is used
- C) The same VMM is running on the target host
- D) Both hosts use the same network


**Answer:** **C** — The same VMM is running on the target host
**Topic:** HW Independence

---

### Section 5: Conditions for Efficient Virtualization (Popek & Goldberg)

**Q25.** According to Popek and Goldberg, a program running inside a VM should:
- A) Run slower than on native hardware
- B) Behave identically to running on an equivalent machine directly
- C) Always inform the VMM before executing each instruction
- D) Only run privileged instructions


**Answer:** **B** — Behave identically to running on an equivalent machine directly
**Topic:** Popek & Goldberg

---

**Q26.** According to Popek and Goldberg, the VMM should have:
- A) Read-only access to virtualized resources
- B) No access to physical hardware
- C) Complete control of virtualized resources
- D) Shared control with the Guest OS


**Answer:** **C** — Complete control of virtualized resources
**Topic:** Popek & Goldberg

---

**Q27.** According to Popek and Goldberg, what fraction of machine instructions must execute without VMM intervention?
- A) All instructions
- B) No instructions
- C) Only privileged instructions
- D) A statistically significant fraction


**Answer:** **D** — A statistically significant fraction
**Topic:** Popek & Goldberg

---

### Section 6: CPU Virtualization — Instruction Types

**Q28.** Non-privileged instructions (e.g., +, -, *, /) run in:
- A) Kernel mode only
- B) Guest mode only
- C) User mode directly
- D) VMM mode


**Answer:** **C** — User mode directly
**Topic:** Instruction Types

---

**Q29.** Privileged instructions (e.g., system calls like getDate(), int 32) must run in:
- A) User mode (Ring 3)
- B) Kernel mode (Ring 0)
- C) Ring 1
- D) Ring 2


**Answer:** **B** — Kernel mode (Ring 0)
**Topic:** Instruction Types

---

**Q30.** When a user-mode application attempts to execute a privileged instruction, what happens?
- A) The instruction is silently ignored
- B) A hardware interrupt is triggered and control transfers to the VMM
- C) A SW interrupt "Trap" is triggered, transferring control to the OS
- D) The CPU switches to Ring 2


**Answer:** **C** — A SW interrupt "Trap" is triggered, transferring control to the OS
**Topic:** Privileged Instructions

---

**Q31.** Non-sensitive instructions are those that:
- A) Change hardware settings
- B) Behave differently based on HW settings
- C) Do not change hardware settings
- D) Always require kernel mode execution


**Answer:** **C** — Do not change hardware settings
**Topic:** Non-Sensitive Instructions

---

**Q32.** "Control Sensitive" instructions are those that:
- A) Only read hardware state
- B) Change hardware settings
- C) Behave differently based on hardware settings
- D) Execute only in user mode


**Answer:** **B** — Change hardware settings
**Topic:** Control Sensitive

---

**Q33.** "Behavior Sensitive" instructions are those that:
- A) Change hardware settings
- B) Only run in kernel mode
- C) Behave differently based on hardware settings
- D) Are always non-privileged


**Answer:** **C** — Behave differently based on hardware settings
**Topic:** Behavior Sensitive

---

**Q34.** Without virtualization, the Host OS runs at which CPU ring?
- A) Ring 3
- B) Ring 1
- C) Ring 2
- D) Ring 0


**Answer:** **D** — Ring 0
**Topic:** CPU Rings (No Virt)

---

**Q35.** With virtualization (Full Virtualization), the Guest OS is pushed to which ring?
- A) Ring 0
- B) Ring 3
- C) Ring 1
- D) Ring 2


**Answer:** **C** — Ring 1
**Topic:** CPU Rings (Full Virt)

---

**Q36.** In a virtualized environment, applications inside a VM run at which ring?
- A) Ring 0
- B) Ring 1
- C) Ring 2
- D) Ring 3


**Answer:** **D** — Ring 3
**Topic:** CPU Rings (Full Virt)

---

### Section 7: CPU Virtualization — Full Virtualization (Binary Translation)

**Q37.** Full Virtualization uses which technique to handle instructions?
- A) Hypercalls
- B) Direct paravirtual API calls
- C) Binary Translation
- D) Hardware VMX root mode only


**Answer:** **C** — Binary Translation
**Topic:** Full Virtualization

---

**Q38.** In Full Virtualization with Binary Translation, when an application runs a normal CPU instruction (e.g., Add, Mul) on the SAME ISA, it is handled by:
- A) Translating to a different ISA
- B) Direct Execution on the physical machine
- C) Trapping to the hypervisor
- D) Calling a hypercall


**Answer:** **B** — Direct Execution on the physical machine
**Topic:** Full Virt — Same ISA

---

**Q39.** In Full Virtualization, when an application runs a normal CPU instruction on a DIFFERENT ISA (e.g., ARM mul on x86), the VMM:
- A) Directly executes it unchanged
- B) Rejects the instruction
- C) Translates the instruction to the physical machine's ISA equivalent
- D) Passes it to the Guest OS to handle


**Answer:** **C** — Translates the instruction to the physical machine's ISA equivalent
**Topic:** Full Virt — Different ISA

---

**Q40.** When an application in a VM executes a system call (e.g., read file), in Full Virtualization (same ISA), what happens first?
- A) The Guest OS directly handles it
- B) The instruction Traps to the VMM
- C) The VMM sends a hypercall
- D) The instruction is silently dropped


**Answer:** **B** — The instruction Traps to the VMM
**Topic:** Full Virt — System Calls

---

**Q41.** After a system call Traps to the VMM in Full Virtualization, the VMM:
- A) Crashes the VM
- B) Passes it directly to the physical OS
- C) Emulates the Guest OS behavior
- D) Translates the instruction to a different ISA


**Answer:** **C** — Emulates the Guest OS behavior
**Topic:** Full Virt — Emulation

---

**Q42.** The "Potential Problem" with Full Virtualization (Binary Translation) is:
- A) The Guest OS must be open-source
- B) Not all sensitive instructions trigger a SW interrupt (trap)
- C) Hypercalls are too slow
- D) Hardware must support VMX non-root mode


**Answer:** **B** — Not all sensitive instructions trigger a SW interrupt (trap)
**Topic:** Full Virt — Problem

---

**Q43.** How many instructions on the Pentium processor are sensitive and non-privileged (problematic for virtualization)?
- A) 5
- B) 32
- C) 17
- D) 8


**Answer:** **C** — 17
**Topic:** Pentium Problem

---

**Q44.** Which of the following is an example of a Full Virtualization product?
- A) Xen (PV mode)
- B) Denali
- C) VMware ESX Server
- D) KVM paravirtual driver


**Answer:** **C** — VMware ESX Server
**Topic:** Full Virt Examples

---

**Q45.** A key PRO of Full Virtualization (Binary Translation) is:
- A) High execution speed
- B) No hardware or OS modifications required
- C) Requires open-source Guest OS
- D) Uses hypercalls for efficiency


**Answer:** **B** — No hardware or OS modifications required
**Topic:** Full Virt Pros

---

**Q46.** A key CON of Full Virtualization (Binary Translation) is:
- A) Requires modified Guest OS
- B) Poor portability of guest OS
- C) Slow execution due to translation overhead and VMM complexity
- D) Cannot run on same-ISA systems


**Answer:** **C** — Slow execution due to translation overhead and VMM complexity
**Topic:** Full Virt Cons

---

### Section 8: CPU Virtualization — Paravirtualization

**Q47.** Paravirtualization modifies the:
- A) Hypervisor to be unaware of VMs
- B) Host OS to run VMs natively
- C) Guest OS to be aware it is virtualized
- D) Physical hardware firmware


**Answer:** **C** — Guest OS to be aware it is virtualized
**Topic:** Paravirtualization

---

**Q48.** In Paravirtualization, system calls are replaced by:
- A) Direct hardware interrupts
- B) Hypercalls
- C) Binary translated instructions
- D) Ring 0 trap instructions


**Answer:** **B** — Hypercalls
**Topic:** Paravirtualization

---

**Q49.** In Paravirtualization, user-mode instructions are:
- A) Always translated by the VMM
- B) Emulated by the hypervisor
- C) Directly executed on the CPU
- D) Executed through hypercall interface only


**Answer:** **C** — Directly executed on the CPU
**Topic:** Paravirt — User Mode

---

**Q50.** Which of the following is an example of a Paravirtualization VMM?
- A) VMware ESX
- B) VirtualBox
- C) Xen
- D) Hyper-V


**Answer:** **C** — Xen
**Topic:** Paravirt Examples

---

**Q51.** A PRO of Paravirtualization is:
- A) No modification to Guest OS needed
- B) Works with closed-source Guest OS
- C) High execution speed similar to non-virtualized systems
- D) Better isolation than Full Virtualization


**Answer:** **C** — High execution speed similar to non-virtualized systems
**Topic:** Paravirt Pros

---

**Q52.** A CON of Paravirtualization is:
- A) Slow execution due to translation
- B) VMM complexity increases significantly
- C) Guest OS must be open-source to be modified, and has poor portability
- D) Cannot run multiple VMs simultaneously


**Answer:** **C** — Guest OS must be open-source to be modified, and has poor portability
**Topic:** Paravirt Cons

---

### Section 9: CPU Virtualization — Hardware-Assisted Virtualization

**Q53.** Hardware-Assisted Virtualization solves the "sensitive non-privileged instruction" problem by:
- A) Modifying the Guest OS
- B) Using binary translation for all instructions
- C) Ensuring all sensitive instructions trigger a trap to the hypervisor at the hardware level
- D) Replacing the VMM with a lighter container engine


**Answer:** **C** — Ensuring all sensitive instructions trigger a trap to the hypervisor at the hardware level
**Topic:** HW-Assisted Virt

---

**Q54.** Hardware-Assisted Virtualization removes the need for:
- A) A Guest OS
- B) Binary Translation
- C) A Hypervisor
- D) Memory virtualization


**Answer:** **B** — Binary Translation
**Topic:** HW-Assisted Virt

---

**Q55.** Intel's hardware virtualization technology is called:
- A) AMD-V
- B) VT-d
- C) VT-x
- D) VMX-V


**Answer:** **C** — VT-x
**Topic:** Intel HW Virt

---

**Q56.** Intel VT-x introduces "VMX root" mode, which is used for:
- A) Running guest VMs
- B) VMM Operations
- C) User-mode applications
- D) Memory paging


**Answer:** **B** — VMM Operations
**Topic:** VMX Root

---

**Q57.** Intel VT-x introduces "VMX non-root" mode, which is used for:
- A) Running the Hypervisor
- B) Kernel mode operations of the host
- C) Supporting VM execution
- D) Hardware interrupt handling only


**Answer:** **C** — Supporting VM execution
**Topic:** VMX Non-Root

---

**Q58.** In Hardware-Assisted Virtualization, the Guest OS runs at which ring inside VMX non-root?
- A) Ring 3
- B) Ring 2
- C) Ring 1
- D) Ring 0


**Answer:** **D** — Ring 0 (inside VMX non-root context)
**Topic:** HW-Assisted Rings

---

**Q59.** A PRO of Hardware-Assisted Virtualization compared to Binary Translation is:
- A) No hardware support needed
- B) Even faster execution
- C) No VMM required
- D) Works without Intel VT-x or AMD-V


**Answer:** **B** — Even faster execution
**Topic:** HW-Assisted Pros

---

### Section 10: VM Context Switching

**Q60.** VM Context Switching is triggered when a VM is blocked due to:
- A) A user logging out
- B) Waiting for an IO operation or CPU Timeout
- C) A network packet being dropped
- D) The Guest OS updating its kernel


**Answer:** **B** — Waiting for an IO operation or CPU Timeout
**Topic:** VM Context Switch

---

**Q61.** What is the CORRECT order of the first three steps in VM Context Switching?
- A) Hypervisor selects next VM -> Timer Interrupt -> Context switch to Hypervisor
- B) Timer Interrupt in running VM -> Context switch to Hypervisor -> Hypervisor saves state of running VM
- C) Context switch to Hypervisor -> Timer Interrupt -> Save VM state
- D) Hypervisor saves state -> Timer Interrupt -> Select next VM


**Answer:** **B** — Timer Interrupt -> Context switch to Hypervisor -> Hypervisor saves state
**Topic:** VM Context Switch Steps

---

**Q62.** After the Hypervisor saves the state of the running VM during context switching, the next step is:
- A) Restore state of next VM
- B) Set timer interrupt
- C) Determine next VM to execute
- D) Transfer control back to running VM


**Answer:** **C** — Determine next VM to execute
**Topic:** VM Context Switch Steps

---

**Q63.** At the end of VM Context Switching, the Hypervisor sets the program counter to:
- A) The next user-mode application instruction
- B) The timer interrupt handler of the next VM
- C) Ring 0 of the physical machine
- D) The previous VM's checkpoint


**Answer:** **B** — The timer interrupt handler of the next VM
**Topic:** VM Context Switch Steps

---

### Section 11: Containers

**Q64.** Containers are best described as:
- A) Full virtual machines with independent Guest OS kernels
- B) Lightweight process virtualization sharing the host OS kernel
- C) Bare-metal hypervisors running on hardware
- D) Hardware emulators for different CPU architectures


**Answer:** **B** — Lightweight process virtualization sharing the host OS kernel
**Topic:** Containers

---

**Q65.** Unlike VMs, containers:
- A) Have their own independent OS kernel
- B) Use binary translation for instructions
- C) Share the same kernel of the host OS
- D) Require a Type 1 hypervisor


**Answer:** **C** — Share the same kernel of the host OS
**Topic:** Containers vs VMs

---

**Q66.** A container is technically a:
- A) KVM module
- B) Linux process with separate namespace/network space
- C) Full OS snapshot
- D) Xen domain


**Answer:** **B** — Linux process with separate namespace/network space
**Topic:** Containers

---

### Section 12: Memory Virtualization

**Q67.** In Memory Virtualization, the address mapping flow goes through these levels in order:
- A) Machine Frames -> Guest Physical Frames -> Virtual Address
- B) Virtual Address -> Machine Frames -> Guest Physical Frames
- C) Virtual Address -> Guest Physical Frames (V-to-P) -> Machine Frames (P-to-M)
- D) Guest Physical Frames -> Virtual Address -> Machine Frames


**Answer:** **C** — Virtual Address -> Guest Physical Frames (V-to-P) -> Machine Frames (P-to-M)
**Topic:** Memory Virt

---

**Q68.** In Memory Virtualization, "GPFN" stands for:
- A) General Purpose Frame Number
- B) Guest Physical Frame Number
- C) Global Page Frame Node
- D) Guest Paging Function Node


**Answer:** **B** — Guest Physical Frame Number
**Topic:** Memory Virt Terms

---

**Q69.** In Memory Virtualization, the translation from Guest Physical Frames to Machine Frames is performed by:
- A) The Guest OS
- B) The application
- C) The Hypervisor
- D) The physical CPU directly


**Answer:** **C** — The Hypervisor
**Topic:** Memory Virt

---

### Section 13: KVM (Kernel-based Virtual Machine)

**Q70.** KVM transforms the Linux OS into a:
- A) Type 2 hosted hypervisor
- B) Container runtime
- C) Bare-Metal VMM
- D) Paravirtualization platform only


**Answer:** **C** — Bare-Metal VMM
**Topic:** KVM

---

**Q71.** KVM relies on which CPU virtualization technique?
- A) Binary Translation
- B) Paravirtualization only
- C) Hardware-Assisted Virtualization
- D) Software emulation


**Answer:** **C** — Hardware-Assisted Virtualization
**Topic:** KVM

---

**Q72.** KVM is structured in Linux as a device at:
- A) /dev/vm
- B) /dev/hypervisor
- C) /dev/kvm
- D) /dev/vmm


**Answer:** **C** — /dev/kvm
**Topic:** KVM Structure

---

**Q73.** VMs are created and run in KVM using a set of:
- A) hypercall() commands
- B) ioctl() commands
- C) syscall() wrappers
- D) fork() system calls


**Answer:** **B** — ioctl() commands
**Topic:** KVM API

---

**Q74.** Which KVM kernel module handles x86 ISA virtualization?
- A) kvm-intel.ko
- B) kvm-amd.ko
- C) kvm.ko
- D) kvm-x86.ko


**Answer:** **C** — kvm.ko
**Topic:** KVM Modules

---

**Q75.** Which KVM module handles Intel-specific virtualization features?
- A) kvm.ko
- B) kvm-amd.ko
- C) kvm-hw.ko
- D) kvm-intel.ko


**Answer:** **D** — kvm-intel.ko
**Topic:** KVM Modules

---

**Q76.** KVM introduces a third OS mode beyond User mode and Kernel mode. This is called:
- A) VMX root mode
- B) Hypervisor mode
- C) Guest mode (VMX non-root)
- D) Ring -1


**Answer:** **C** — Guest mode (VMX non-root)
**Topic:** KVM Modes

---

**Q77.** QEMU is described as a:
- A) Type 1 bare-metal hypervisor
- B) Portable Binary Translator / Dynamic Translator
- C) Linux kernel module for CPU isolation
- D) Container orchestration engine


**Answer:** **B** — Portable Binary Translator / Dynamic Translator
**Topic:** QEMU

---

**Q78.** QEMU communicates with KVM through which interface?
- A) TCP socket to /dev/vm
- B) Direct kernel system calls
- C) ioctl() via /dev/kvm
- D) Shared memory buffers


**Answer:** **C** — ioctl() via /dev/kvm
**Topic:** QEMU-KVM Interface

---

**Q79.** In the KVM/QEMU model, vCPUs are mapped to physical CPUs and utilize:
- A) Software binary translation
- B) Hardware VT (Virtualization Technology)
- C) Paravirtual hypercalls
- D) IO Ring batching


**Answer:** **B** — Hardware VT (Virtualization Technology)
**Topic:** KVM/QEMU Model

---

**Q80.** In the KVM/QEMU model, QEMU is responsible for:
- A) CPU scheduling of physical cores
- B) Mapping guest virtual addresses to machine frames
- C) Initiating VM processes, managing memory space, and emulating I/O devices
- D) Writing kernel modules for hardware drivers


**Answer:** **C** — Initiating VM processes, managing memory space, and emulating I/O devices
**Topic:** QEMU Role

---

### Section 14: Xen

**Q81.** Xen is classified as which type of VMM?
- A) Type 2 hosted hypervisor
- B) Container runtime
- C) Bare-Metal VMM (Type 1)
- D) Software-only emulator


**Answer:** **C** — Bare-Metal VMM (Type 1)
**Topic:** Xen

---

**Q82.** Xen is primarily based on which CPU virtualization approach?
- A) Binary Translation
- B) Hardware-Assisted Virtualization only
- C) Paravirtualization
- D) Full Virtualization (software emulation)


**Answer:** **C** — Paravirtualization
**Topic:** Xen

---

**Q83.** In Xen terminology, each VM is referred to as a:
- A) Node
- B) Container
- C) Instance
- D) Domain


**Answer:** **D** — Domain
**Topic:** Xen Terminology

---

**Q84.** In Xen, "Dom0" is special because it:
- A) Is the first guest VM created by a user
- B) Controls the Xen VMM, manages other domains, and emulates devices
- C) Runs without any OS
- D) Is a read-only snapshot domain


**Answer:** **B** — Controls the Xen VMM, manages other domains, and emulates devices
**Topic:** Dom0

---

**Q85.** In Xen's architecture, paravirtualized guest domains communicate with the hypervisor through:
- A) ioctl() commands
- B) Binary translation
- C) Hypercalls
- D) Direct Ring 0 system calls


**Answer:** **C** — Hypercalls
**Topic:** Xen PV

---

**Q86.** The IO Ring in Xen is used to:
- A) Encrypt network traffic between VMs
- B) Schedule VM CPU time
- C) Reduce overhead of VM context switching by batching IO requests
- D) Manage memory page tables


**Answer:** **C** — Reduce overhead of VM context switching by batching IO requests
**Topic:** IO Ring

---

**Q87.** In Xen's IO Ring architecture, the "Front-end" driver resides in:
- A) Dom0 (Driver domain)
- B) The Xen Hypervisor
- C) The physical hardware
- D) The Guest domain (DomU)


**Answer:** **D** — The Guest domain (DomU)
**Topic:** IO Ring

---

### Section 15: Virtualization Security Downsides

**Q88.** A "Rouge Hypervisor" attack involves:
- A) A VM consuming all CPU resources
- B) Inserting a Virtual-Machine Based Rootkit (VMBR) between physical hardware and the real VMM
- C) A container escaping its namespace
- D) An attacker modifying the Guest OS kernel


**Answer:** **B** — Inserting a VMBR between physical hardware and the real VMM
**Topic:** Rouge Hypervisor

---

**Q89.** In a layered privilege structure, a defensive mechanism at a layer can be disabled by:
- A) Another application at the same layer
- B) The Hypervisor's scheduler
- C) Malware in a lower (more privileged) layer
- D) The Guest OS memory manager


**Answer:** **C** — Malware in a lower (more privileged) layer
**Topic:** Security

---

**Q90.** A Virtual-Machine Based Rootkit (VMBR) can be used to: (Select the INCORRECT statement)
- A) Create malicious OSs
- B) Spy on real guest OS
- C) Perform DoS on guest OSs
- D) Improve VM performance and resource allocation


**Answer:** **D** — Improve VM performance and resource allocation (this is NOT what VMBR does)
**Topic:** VMBR

---

**Q91.** The "Noisy Neighbor" problem in virtualization refers to:
- A) A VM generating excessive network noise
- B) A VM using all system resources, degrading performance of other VMs on the same host
- C) A container sharing its kernel with a VM
- D) A hypervisor generating excessive log entries


**Answer:** **B** — A VM using all system resources, degrading performance of other VMs
**Topic:** Noisy Neighbor

---

**Q92.** A "Rouge VM" is best described as:
- A) A VM running a deprecated OS
- B) A VM that fails to start
- C) A hidden VM created by an attacker on your machine
- D) A VM running without a Guest OS


**Answer:** **C** — A hidden VM created by an attacker on your machine
**Topic:** Rouge VM

---

**Q93.** How can an attacker create a Rouge VM on a VMware ESXi server?
- A) By physically accessing the server room
- B) By modifying the network switch configuration
- C) By gaining SSH access and running simple scripts
- D) By replacing the hypervisor firmware directly


**Answer:** **C** — By gaining SSH access and running simple scripts
**Topic:** Rouge VM

---

### Section 16: Mixed / Tricky Concepts

**Q94.** Which of the following correctly distinguishes Sensitive Instructions from Privileged Instructions?
- A) They are exactly the same set
- B) Sensitive instructions are a subset of privileged instructions
- C) Not all sensitive instructions are privileged — some are non-privileged and do not automatically trap
- D) Privileged instructions are a subset of sensitive instructions


**Answer:** **C** — Not all sensitive instructions are privileged — some are non-privileged and do not auto-trap
**Topic:** Sensitive vs Privileged

---

**Q95.** In Hardware-Assisted Virtualization (Intel VT-x), for the Popek & Goldberg conditions to be satisfied, the sensitive instructions set must be:
- A) A superset of privileged instructions
- B) A subset of privileged instructions (all sensitive = privileged, all trap to VMM)
- C) Completely disjoint from privileged instructions
- D) Identical to non-sensitive instructions


**Answer:** **B** — Sensitive instructions must be a subset of privileged instructions
**Topic:** HW-Assisted & Popek

---

**Q96.** The key difference between a container and a VM is:
- A) Containers use a Type 1 hypervisor; VMs use Type 2
- B) VMs share the host OS kernel; containers have their own kernel
- C) Containers share the host OS kernel; VMs have their own independent Guest OS
- D) Containers are slower than VMs


**Answer:** **C** — Containers share the host OS kernel; VMs have their own independent Guest OS
**Topic:** Containers vs VMs

---

**Q97.** KVM is classified as a Bare-Metal (Type 1) hypervisor even though it runs inside Linux because:
- A) It uses hardware VT-x exclusively
- B) It transforms the Linux kernel itself into a hypervisor
- C) Linux is not considered a real OS
- D) It uses QEMU to bypass the Linux kernel


**Answer:** **B** — It transforms the Linux kernel itself into a hypervisor
**Topic:** KVM Classification

---

**Q98.** Xen supports both Paravirtualization and Full Virtualization. Its fully virtualized guests are called:
- A) Dom0
- B) DomU (PV)
- C) DomU (HVM)
- D) DomU (KVM)


**Answer:** **C** — DomU (HVM)
**Topic:** Xen HVM

---

**Q99.** The VM Context Switching step "Hypervisor sets timer interrupt" occurs at which step number?
- A) Step 3
- B) Step 4
- C) Step 5
- D) Step 6


**Answer:** **C** — Step 5
**Topic:** VM Context Switch Steps

---

**Q100.** Which of the following is the MOST direct benefit of virtualization's "Encapsulation" in cloud computing?
- A) CPU scheduling efficiency
- B) VM live migration between physical hosts
- C) Memory overcommitment
- D) Kernel-level isolation between VMs


**Answer:** **B** — VM live migration between physical hosts
**Topic:** Encapsulation Benefit

---

**Q101.** In Full Virtualization, when a Guest OS executes a kernel-mode instruction (e.g., kill()), what happens at Ring 1?
- A) The Guest OS directly accesses Ring 0 hardware
- B) The instruction traps to the Hypervisor at Ring 0 which emulates the behavior
- C) The instruction is silently ignored
- D) The instruction is passed to Ring 2 for processing


**Answer:** **B** — The instruction traps to the Hypervisor at Ring 0 which emulates the behavior
**Topic:** Full Virt Kernel Call

---

**Q102.** Hardware interrupts (e.g., keyboard input) in Full Virtualization are handled by:
- A) The Guest OS directly
- B) Ring 3 application layer
- C) The VMM (Hypervisor)
- D) The physical CPU without VMM involvement


**Answer:** **C** — The VMM (Hypervisor)
**Topic:** HW Interrupts

---

*End of Lecture 2 MCQ Bank — 102 Questions*
