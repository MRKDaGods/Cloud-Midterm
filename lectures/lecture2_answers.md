# Lecture 2 — Virtualization
## Answer Key

| Q   | Answer | Topic |
|-----|--------|-------|
| 1   | **B** — Software that runs applications, not tied to a physical machine | VM Definition |
| 2   | **C** — It has its own independent Guest OS | VM Properties |
| 3   | **B** — Cloud v1.0 | Why Virtualization |
| 4   | **C** — Increase physical hardware costs | Why Virtualization |
| 5   | **B** — Resource utilization and efficiency | Why Virtualization |
| 6   | **B** — The physical machine | Terminology |
| 7   | **C** — The virtual machine created through virtualization | Terminology |
| 8   | **C** — Virtual Machine Monitor (VMM) | Terminology |
| 9   | **C** — Create and manage virtual environments | Hypervisor Role |
| 10  | **C** — Compile guest OS source code | Hypervisor Functions |
| 11  | **B** — A complete OS for controlling VMs and resource sharing | Hypervisor |
| 12  | **C** — Directly on the hardware | Type 1 |
| 13  | **B** — As a common application on top of a Host OS | Type 2 |
| 14  | **C** — Bare-Metal Virtualization (Type 1) | Virt Types |
| 15  | **B** — Hosted Virtualization (Type 2) | Virt Types |
| 16  | **C** — System administrator-level knowledge | Type 1 |
| 17  | **C** — Hyper-V | Type 1 Examples |
| 18  | **D** — VirtualBox | Type 2 Examples |
| 19  | **B** — Allocating server resources to multiple VMs to prevent overuse | Partitioning |
| 20  | **C** — Its virtual HW quota provided by the VMM | Partitioning |
| 21  | **B** — Is not affected due to Isolation | Isolation |
| 22  | **B** — A group of HW-independent files (e.g., .vbox, .vdi) | Encapsulation |
| 23  | **D** — Encapsulation | VM Migration |
| 24  | **C** — The same VMM is running on the target host | HW Independence |
| 25  | **B** — Behave identically to running on an equivalent machine directly | Popek & Goldberg |
| 26  | **C** — Complete control of virtualized resources | Popek & Goldberg |
| 27  | **D** — A statistically significant fraction | Popek & Goldberg |
| 28  | **C** — User mode directly | Instruction Types |
| 29  | **B** — Kernel mode (Ring 0) | Instruction Types |
| 30  | **C** — A SW interrupt "Trap" is triggered, transferring control to the OS | Privileged Instructions |
| 31  | **C** — Do not change hardware settings | Non-Sensitive Instructions |
| 32  | **B** — Change hardware settings | Control Sensitive |
| 33  | **C** — Behave differently based on hardware settings | Behavior Sensitive |
| 34  | **D** — Ring 0 | CPU Rings (No Virt) |
| 35  | **C** — Ring 1 | CPU Rings (Full Virt) |
| 36  | **D** — Ring 3 | CPU Rings (Full Virt) |
| 37  | **C** — Binary Translation | Full Virtualization |
| 38  | **B** — Direct Execution on the physical machine | Full Virt — Same ISA |
| 39  | **C** — Translates the instruction to the physical machine's ISA equivalent | Full Virt — Different ISA |
| 40  | **B** — The instruction Traps to the VMM | Full Virt — System Calls |
| 41  | **C** — Emulates the Guest OS behavior | Full Virt — Emulation |
| 42  | **B** — Not all sensitive instructions trigger a SW interrupt (trap) | Full Virt — Problem |
| 43  | **C** — 17 | Pentium Problem |
| 44  | **C** — VMware ESX Server | Full Virt Examples |
| 45  | **B** — No hardware or OS modifications required | Full Virt Pros |
| 46  | **C** — Slow execution due to translation overhead and VMM complexity | Full Virt Cons |
| 47  | **C** — Guest OS to be aware it is virtualized | Paravirtualization |
| 48  | **B** — Hypercalls | Paravirtualization |
| 49  | **C** — Directly executed on the CPU | Paravirt — User Mode |
| 50  | **C** — Xen | Paravirt Examples |
| 51  | **C** — High execution speed similar to non-virtualized systems | Paravirt Pros |
| 52  | **C** — Guest OS must be open-source to be modified, and has poor portability | Paravirt Cons |
| 53  | **C** — Ensuring all sensitive instructions trigger a trap to the hypervisor at the hardware level | HW-Assisted Virt |
| 54  | **B** — Binary Translation | HW-Assisted Virt |
| 55  | **C** — VT-x | Intel HW Virt |
| 56  | **B** — VMM Operations | VMX Root |
| 57  | **C** — Supporting VM execution | VMX Non-Root |
| 58  | **D** — Ring 0 (inside VMX non-root context) | HW-Assisted Rings |
| 59  | **B** — Even faster execution | HW-Assisted Pros |
| 60  | **B** — Waiting for an IO operation or CPU Timeout | VM Context Switch |
| 61  | **B** — Timer Interrupt -> Context switch to Hypervisor -> Hypervisor saves state | VM Context Switch Steps |
| 62  | **C** — Determine next VM to execute | VM Context Switch Steps |
| 63  | **B** — The timer interrupt handler of the next VM | VM Context Switch Steps |
| 64  | **B** — Lightweight process virtualization sharing the host OS kernel | Containers |
| 65  | **C** — Share the same kernel of the host OS | Containers vs VMs |
| 66  | **B** — Linux process with separate namespace/network space | Containers |
| 67  | **C** — Virtual Address -> Guest Physical Frames (V-to-P) -> Machine Frames (P-to-M) | Memory Virt |
| 68  | **B** — Guest Physical Frame Number | Memory Virt Terms |
| 69  | **C** — The Hypervisor | Memory Virt |
| 70  | **C** — Bare-Metal VMM | KVM |
| 71  | **C** — Hardware-Assisted Virtualization | KVM |
| 72  | **C** — /dev/kvm | KVM Structure |
| 73  | **B** — ioctl() commands | KVM API |
| 74  | **C** — kvm.ko | KVM Modules |
| 75  | **D** — kvm-intel.ko | KVM Modules |
| 76  | **C** — Guest mode (VMX non-root) | KVM Modes |
| 77  | **B** — Portable Binary Translator / Dynamic Translator | QEMU |
| 78  | **C** — ioctl() via /dev/kvm | QEMU-KVM Interface |
| 79  | **B** — Hardware VT (Virtualization Technology) | KVM/QEMU Model |
| 80  | **C** — Initiating VM processes, managing memory space, and emulating I/O devices | QEMU Role |
| 81  | **C** — Bare-Metal VMM (Type 1) | Xen |
| 82  | **C** — Paravirtualization | Xen |
| 83  | **D** — Domain | Xen Terminology |
| 84  | **B** — Controls the Xen VMM, manages other domains, and emulates devices | Dom0 |
| 85  | **C** — Hypercalls | Xen PV |
| 86  | **C** — Reduce overhead of VM context switching by batching IO requests | IO Ring |
| 87  | **D** — The Guest domain (DomU) | IO Ring |
| 88  | **B** — Inserting a VMBR between physical hardware and the real VMM | Rouge Hypervisor |
| 89  | **C** — Malware in a lower (more privileged) layer | Security |
| 90  | **D** — Improve VM performance and resource allocation (this is NOT what VMBR does) | VMBR |
| 91  | **B** — A VM using all system resources, degrading performance of other VMs | Noisy Neighbor |
| 92  | **C** — A hidden VM created by an attacker on your machine | Rouge VM |
| 93  | **C** — By gaining SSH access and running simple scripts | Rouge VM |
| 94  | **C** — Not all sensitive instructions are privileged — some are non-privileged and do not auto-trap | Sensitive vs Privileged |
| 95  | **B** — Sensitive instructions must be a subset of privileged instructions | HW-Assisted & Popek |
| 96  | **C** — Containers share the host OS kernel; VMs have their own independent Guest OS | Containers vs VMs |
| 97  | **B** — It transforms the Linux kernel itself into a hypervisor | KVM Classification |
| 98  | **C** — DomU (HVM) | Xen HVM |
| 99  | **C** — Step 5 | VM Context Switch Steps |
| 100 | **B** — VM live migration between physical hosts | Encapsulation Benefit |
| 101 | **B** — The instruction traps to the Hypervisor at Ring 0 which emulates the behavior | Full Virt Kernel Call |
| 102 | **C** — The VMM (Hypervisor) | HW Interrupts |

---

## Quick Reference: Key Facts to Memorize

### CPU Virtualization Comparison
| Technique | Guest OS Modified? | Speed | Example |
|-----------|-------------------|-------|---------|
| Full Virt (Binary Translation) | No | Slow (translation overhead) | VMware ESX |
| Paravirtualization | Yes (open-source needed) | Fast (near-native) | Xen, Denali |
| Hardware-Assisted | No | Fastest | KVM (VT-x) |

### CPU Rings (With Full Virtualization)
- **Ring 3** — Application (user mode)
- **Ring 1** — Guest OS (pushed down by hypervisor)
- **Ring 0** — Hypervisor
- **VMX non-root Ring 0** — Guest OS (Hardware-Assisted)
- **VMX root** — Hypervisor (Hardware-Assisted)

### Virtualization Characteristics
1. **Partitioning** — Resource quotas per VM
2. **Isolation** — Crash in one VM does not affect others
3. **Encapsulation** — VM stored as files (.vbox, .vdi) → enables migration
4. **HW Independence** — Same VMM on target = can migrate across different hardware

### Hypervisor Type Comparison
| | Type 1 (Bare-Metal) | Type 2 (Hosted) |
|-|---------------------|-----------------|
| Runs on | Hardware directly | Host OS |
| Best for | Large workloads | Desktop/Dev |
| Knowledge | Sysadmin | Basic user |
| Examples | Hyper-V, KVM, Xen | VirtualBox, VMware Workstation |

### Popek & Goldberg (1974) — 3 Conditions
1. Programs in VM behave identically to native execution
2. VMM has **complete control** of virtualized resources
3. **Statistically significant fraction** of instructions execute without VMM intervention

### Pentium Problem
- **17** instructions are **sensitive but non-privileged** — do NOT auto-trap — Full Virt must detect them manually

### VM Context Switching — 8 Steps
1. Timer Interrupt in running VM
2. Context switch to Hypervisor
3. Hypervisor **saves** state of running VM
4. Hypervisor **determines** next VM
5. Hypervisor **sets** timer interrupt
6. Hypervisor **restores** state of next VM
7. Hypervisor sets PC to timer interrupt handler of next VM
8. Next VM active

### KVM Modules
- `kvm.ko` — x86 ISA support
- `kvm-intel.ko` — Intel VT-x features
- `kvm-amd.ko` — AMD-V features

### KVM/QEMU Division of Responsibility
- **KVM** — CPU virtualization (vCPUs, HW VT mapping), `/dev/kvm` interface
- **QEMU** — VM process management, memory space, I/O device emulation, communicates via `ioctl()`

### Xen Key Facts
- Type 1 (Bare-Metal), Paravirtualization-based, supports HVM
- **Dom0** = privileged domain controlling Xen VMM
- **DomU (PV)** = paravirtualized guest
- **DomU (HVM)** = fully virtualized guest
- **IO Ring** = batches IO requests to reduce context switch overhead
- Guest communicates via **Hypercalls**

### Security Downsides
- **Rouge Hypervisor / VMBR** — Insert malicious VMM between HW and real VMM
- **Noisy Neighbor** — One VM consumes all resources, degrades other VMs
- **Rouge VM** — Attacker creates hidden VM via SSH + scripts (e.g., on VMware ESXi)
