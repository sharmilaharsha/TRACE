# TRACE
This work is submitted 

![image](https://github.com/user-attachments/assets/0e26c6f8-197f-4e8a-96a7-9b8f41c7529d)


**Tools and detailed description**

**1. Oracle VirtualBox - Windows-10 machine**
Oracle VirtualBox{https://www.virtualbox.org/} is a popular Type2 hypervisor, open-source for dynamic malware analysis, offering several advantages over other virtualization platforms like VMware, QEMU, and Hyper-V. It is free to use with no licensing restrictions, making it ideal for budget-conscious analysis, and supports a variety of host (Windows, Linux, BSD) and guest operating systems. VirtualBox provides features like snapshots and cloning, allowing saving and restoring VM states or cloning VMs for flexible testing. It ensures full isolation of the virtual machine from the host system, preventing malware from spreading, and offers customizable network settings to control external communication. Additionally, VirtualBox is lightweight and performs efficiently even on systems with limited resources.

**2. Volatility**
Volatility{https://volatilityfoundation.org/} is a powerful, open-source memory forensic tool widely used for analyzing memory dumps to investigate malware, uncover attacks, and conduct digital forensics. It is highly accessible to integrate with other tools, offering a rich plugin ecosystem for various analysis tasks, including process listing, network connections, rootkit detection, and volatile data analysis. It offers a support to multiple operating systems providing detailed insights of system processes, memory contents, and relationships. Supporting multiple operating systems like Windows, Linux, and macOS, Volatility provides detailed insights into system processes, memory contents, and relationships. 
It excels at detecting sophisticated malware techniques such as rootkits, process injection, and in-memory malware. Additionally, Volatility includes memory carving for recovering deleted files and artifacts, as well as timeline-based analysis to correlate system events, making it ideal for identifying system modifications caused by malware and comparing memory dumps to detect attack-related changes. Post attack usage is commonly observed, in our work we recommend it for live detection.

**3. Winpmem**
WinPMEM{https://winpmem.velocidex.com/} is a widely-used, Windows-based memory dump capture tool for digital forensics and incident response, designed to acquire memory dumps in a forensically sound manner. It creates a bit-for-bit copy of system memory, including both physical and virtual memory, offering a comprehensive snapshot at the time of acquisition. WinPMEM integrates well with the Volatility framework for memory forensics and operates with low overhead to minimize system disruption. Its optimized performance for Windows systems, open-source nature, and customization potential make it a valuable tool for both analysis and further development.

**4. Ghidra for reverse engineering**
Ghidra{https://ghidra-sre.org/} is a powerful open-source reverse engineering framework developed by the NSA, offering a comprehensive set of tools for disassembling, analyzing, and decompiling binary executables. Unlike commercial tools like IDA Pro, Ghidra is free to use and provides a user-friendly graphical interface, supporting Windows, Linux, and macOS. It features advanced static analysis capabilities, including disassembly, decompilation, control flow graph analysis, function identification, and data type reconstruction. Ghidra's intuitive decompiler converts machine code into high-level pseudo-code, and it supports extensibility through Java or Python scripting for task automation. With built-in debugger integration, Ghidra eliminates the need for third-party debuggers and supports multiple processor architectures and binary formats. Additionally, its symbolic execution and advanced analysis tools help identify vulnerabilities and trace potential exploits, making it a versatile and accessible tool for reverse engineering.


