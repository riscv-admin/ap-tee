# Confidential Computing on RISC-V platforms - Application-Processor Trusted Execution Environment (AP-TEE) TG

Acting Chair: Ravi Sahita

Confidential computing defines the mechanisms for protecting the confidentiality and integrity of data-in-use against software and hardware attacks. The data-in-use protection is achieved via a hardware-attested Trusted Compute Base (TCB). This TG will define the threat model, reference architecture and interfaces for Scalable Trusted Execution Environments on RISC-V Application Processor-based platforms to support confidential-compute scenarios. The TG will focus on multi-tenant hardware-virtualized workloads to enable the broadest set of confidential workloads while minimizing application changes.  

The TG aims to deliver: 
* A non-ISA specification for an ABI between the TCB and non-TCB components. This ABI enables OS/VMM software to manage confidential workloads, while keeping the OS/VMM software, firmware, developers and system operators outside the TCB.  A related non-ISA specification for an ABI between the TCB and workload components e.g. a TEE VM will be specified. 
*  ISA extensions required to fill potential gaps in the ratified privileged ISA (specifically H-extension) needed to satisfy security, performance, TCB isolation, and attestation requirements of various deployment models. Creation of new ISA extensions will be in collaboration with the Privileged Arch. TG and will work with the Priv committee to proceed in the appropriate fashion (as part of this TG or a new TG under priv or fastrack).
* A non-normative security analysis document for implementers of this capability that describes platform recommendations including the relevant standard protocols for attestation for interoperability.  

Development of these specifications will happen in collaboration with other SIGs/TGs, such as Privileged Arch., Hypervisor, Microarchitecture Side Channels, IOMMU, and Runtime Integrity.

As part of the DoD, the TG will create at least one open-source implementation. The POC consists of required SBI extension(s) for the proposed interfaces hosted by TCB elements e.g., a software and/or hardware-based TEE Security Manager (TSM). The required changes will be made to the Linux/KVM host and Linux guest software to validate the proposed interface. Any ISA proposals made will be modeled via tools such as QEMU/Spike to support the POC.
