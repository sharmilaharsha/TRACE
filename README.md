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


**Essential Processes**

The list of all essential processes are listed in Table

1. System Idle Process:  Represents the portion of CPU time when the computer is idle. It's a placeholder that uses CPU resources when no other processes are executing. 
		
2. System: The core kernel process of Windows. It's responsible for managing system resources, hardware abstraction, and general system operations.
3. Registry: This refers to the Windows Registry, where the system stores configuration settings and options. It's not typically a standalone process but represents the part of the operating system that handles system configuration.
4. smss.exe (Session Manager Subsystem): Initializes the system environment during boot, sets up the user session, and starts critical system processes like wininit.exe and csrss.exe.
5. csrss.exe (Client/Server Runtime Subsystem): Manages user-mode system processes, such as creating and deleting threads, and managing console windows.

6. 
		wininit.exe& Initializes the Windows environment after boot, setting up services and running system processes like services.exe.\\ \hline
		%
		winlogon.exe& Handles user logon and logoff, managing the login screen and securing access to the system.\\ \hline
		%
		services.exe (Service Control Manager)& Manages Windows services, starting, stopping, and managing background processes.\\ \hline
		%
		lsass.exe (Local Security Authority Subsystem Service)&Handles security policies, user authentication, and Active Directory management.\\ \hline
		%
		svchost.exe& A generic host process that runs Windows services. Multiple instances of svchost.exe run at the same time, each hosting a different group of services.\\ \hline
		%
		fontdrvhost.exe& Manages font loading and rendering on the system, associated with the font subsystem.\\ \hline
		%
		spoolsv.exe (Print Spooler)& Handles print jobs by queuing them for printing in the background.\\ \hline
		%
		rundll32.exe& A utility that runs functions stored in dynamic-link libraries (DLLs). It’s often used to launch system utilities and other applications that use DLLs.\\ \hline
		%
		wuauclt.exe (Windows Update AutoUpdate Client)& Manages the download and installation of Windows updates.\\ \hline
		%
		MoUsoCoreWorker.exe& A background process related to the installation and maintenance of modern (UWP) updates in Windows 10. \\ \hline
		%
		MsMpEng.exe& The core process of Microsoft Defender Antivirus that performs real-time protection against malware and other security threats.\\ \hline
		%
		SearchIndexer.exe& Indexes files on the system to improve the performance of Windows search.\\ \hline
		%
		explorer.exe& The Windows File Explorer, which provides the graphical user interface (GUI) for managing files, folders, and launching applications.\\ \hline
		%
		RuntimeBroker.exe&Manages app permissions for Universal Windows Platform (UWP) apps, ensuring that they do not misuse system resources.\\ \hline
		%
		SecurityHealthService.exe& Monitors the health of Windows security services, ensuring that the firewall and antivirus are enabled, among other things.\\ \hline
		%
		dwm.exe (Desktop Window Manager)& Manages visual effects on the desktop, such as transparency, window composition, and rendering of desktop items.\\ \hline
		%
		sihost.exe (Shell Infrastructure Host)& Handles the graphical elements of the Windows UI, such as the Start Menu, taskbar transparency, and visual effects.\\ \hline
		%
		taskhostw.exe& A process that acts as a host for Windows processes that are not executables but rely on DLL files.\\ \hline
		%
		taskmgr.exe& The Task Manager, used to view and manage running processes, system performance, and applications.\\ \hline
		%
		dllhost.exe& The COM Surrogate process. It runs COM objects in a separate process to prevent crashes in applications.\\ \hline
		%
		NisSrv.exe& Part of Windows Defender, responsible for network protection features and security scanning.\\ \hline
		%
		makecab.exe& A command-line utility for creating CAB files, which are used for packaging and compressing files.\\ \hline
		%
		TrustedInstaller.exe& The service that installs, modifies, and removes system components and Windows updates.\\ \hline
		%
		TiWorker.exe& Windows Modules Installer Worker. It is responsible for installing and updating system components and updates.\\ \hline
		%
		WmiPrvSE.exe (WMI Provider Host)& Hosts Windows Management Instrumentation (WMI) providers, which provide management and monitoring capabilities.			\\ \hline

