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


**5. Content of EPDict**

**Essential Processes**

The list of all essential processes including System Processes and Kernel processes are listed here.

1. System Idle Process:  Represents the portion of CPU time when the computer is idle. It's a placeholder that uses CPU resources when no other processes are executing. 
2. System: The core kernel process of Windows. It's responsible for managing system resources, hardware abstraction, and general system operations.
3. Registry: This refers to the Windows Registry, where the system stores configuration settings and options. It's not typically a standalone process but represents the part of the operating system that handles system configuration.
4. smss.exe (Session Manager Subsystem): Initializes the system environment during boot, sets up the user session, and starts critical system processes like wininit.exe and csrss.exe.
5. csrss.exe (Client/Server Runtime Subsystem): Manages user-mode system processes, such as creating and deleting threads, and managing console windows.
6. wininit.exe: Initializes the Windows environment after boot, setting up services and running system processes like services.exe.
7. winlogon.exe: Handles user logon and logoff, managing the login screen and securing access to the system.
8. services.exe (Service Control Manager): Manages Windows services, starting, stopping, and managing background processes.
9. lsass.exe (Local Security Authority Subsystem Service): Handles security policies, user authentication, and Active Directory management.
10. svchost.exe: A generic host process that runs Windows services. Multiple instances of svchost.exe run at the same time, each hosting a different group of services.
11. fontdrvhost.exe: Manages font loading and rendering on the system, associated with the font subsystem.
12  spoolsv.exe (Print Spooler): Handles print jobs by queuing them for printing in the background.
13. rundll32.exe& A utility that runs functions stored in dynamic-link libraries (DLLs). It’s often used to launch system utilities and other applications that use DLLs.
14. wuauclt.exe (Windows Update AutoUpdate Client): Manages the download and installation of Windows updates.
15. MoUsoCoreWorker.exe: A background process related to the installation and maintenance of modern (UWP) updates in Windows 10.
16. MsMpEng.exe: The core process of Microsoft Defender Antivirus that performs real-time protection against malware and other security threats.
17. SearchIndexer.exe: Indexes files on the system to improve the performance of Windows search.
18. explorer.exe: The Windows File Explorer, which provides the graphical user interface (GUI) for managing files, folders, and launching applications.
19. RuntimeBroker.exe: Manages app permissions for Universal Windows Platform (UWP) apps, ensuring that they do not misuse system resources.
20. SecurityHealthService.exe: Monitors the health of Windows security services, ensuring that the firewall and antivirus are enabled, among other things.
21. dwm.exe (Desktop Window Manager): Manages visual effects on the desktop, such as transparency, window composition, and rendering of desktop items.
22. sihost.exe (Shell Infrastructure Host): Handles the graphical elements of the Windows UI, such as the Start Menu, taskbar transparency, and visual effects.
23. taskhostw.exe: A process that acts as a host for Windows processes that are not executables but rely on DLL files.
24. taskmgr.exe: The Task Manager, used to view and manage running processes, system performance, and applications.
25. dllhost.exe: The COM Surrogate process. It runs COM objects in a separate process to prevent crashes in applications.
26. NisSrv.exe: Part of Windows Defender, responsible for network protection features and security scanning.
27. makecab.exe: A command-line utility for creating CAB files, which are used for packaging and compressing files.
28. TrustedInstaller.exe: The service that installs, modifies, and removes system components and Windows updates.
29. TiWorker.exe: Windows Modules Installer Worker. It is responsible for installing and updating system components and updates.
30. WmiPrvSE.exe (WMI Provider Host): Hosts Windows Management Instrumentation (WMI) providers, which provide management and monitoring capabilities.

**User-Facing Applications and System Utilities**

These processes are associated with user applications and the management of the Windows user interface and their description are mentioned here.

1. OneDriveSetup.exe:A setup process for OneDrive, Microsoft's cloud storage service. It installs OneDrive and sets up its synchronization.
2. PhotosApp.exe: The Windows Photos app used for viewing and editing images and videos on the system.
3. SystemSettings.exe: The Settings app in Windows 10, used to configure system preferences, network settings, and more.
4. UserOOBEBroker.exe: Part of the Out-Of-Box Experience (OOBE) process that runs during initial setup of the system, helping users configure their system preferences.
5. WerFault.exe: Windows Error Reporting, which collects error data from failed programs or system components and reports it to Microsoft.
6. WindowsPackageManagerServer.exe: A service related to Windows Package Manager (winget), which is used for installing and managing apps from the command line.
7. winpmem\_mini.exe: A lightweight version of winpmem (a memory acquisition tool) for capturing memory dumps.
8. PhotosService.exe: Supports the Photos app, managing background tasks related to photo management and display.
9. msedgewebview2.exe: A process related to Microsoft Edge WebView2, allowing Edge-based web content to be embedded into other apps.
10. FileCoAuth.exe: Part of Office that enables real-time collaborative editing in Office documents stored in the cloud.
11. SearchApp.exe: Manages search functionality within the Windows operating system, especially for Cortana and the search box in the Start Menu.
12. ctfmon.exe: Handles alternative input devices, such as speech recognition or handwriting input, and the language bar.
13. audiodg.exe: The Audio Device Graph Isolation process, which manages audio effects like enhancements or virtual sound processing.
14. StartMenuExperienceHost .exe: A background process that manages the Start Menu experience in Windows 10.
15. smartscreen.exe: Windows SmartScreen, which helps protect the system by preventing access to unsafe websites and applications.
16. SecurityHealthSystray.exe: A tray icon that shows the security status of your system, such as antivirus status and firewall settings.
17. ApplicationFrameHost.exe: Hosts modern Windows Store (UWP) applications, allowing them to run within their own windows.
18. TextInputHost.exe: Manages the Text Input framework, supporting virtual keyboards and alternative text input methods.
19. cmd.exe: The Command Prompt, a command-line interface for interacting with the operating system.
20. conhost.exe: The Console Window Host, which manages the graphical elements of the command prompt.
21. SearchProtocolHost.exe: A background process that handles search indexing and filters content for the Windows search feature.
22. SearchFilterHost.exe: Works with SearchProtocolHost.exe to process and filter search results.

**Security and Maintenance Tools**

These processes are associated with security, maintenance, and system health. and their description are mentioned here.
1. MpDefenderCoreService.exe: Core service of Microsoft Defender Antivirus that runs in the background to protect the system.
2. MpCmdRun.exe: A command-line utility for managing Microsoft Defender, allowing you to run scans and perform other security-related tasks.
3. sppsvc.exe: The Software Protection Platform Service, ensuring that Windows is activated and licensed.
4. DeviceCensus.exe: Collects device information for telemetry and compatibility purposes, helping Microsoft improve the system.
5. RuntimeBroker.exe: Ensures that UWP apps do not misuse system resources by managing permissions and access controls.
6. MicrosoftEdgeUpdate.exe: Manages updates for the Microsoft Edge browser.
7. SgrmBroker.exe: Part of the security feature ``Windows Defender System Guard," which helps protect against system tampering.
8. ShellExperienceHost.exe: Hosts the Windows Shell experience, including elements like the taskbar, start menu, and action center.
9. OneDrive.exe: The OneDrive client for cloud file synchronization between your computer and Microsoft's cloud storage.
10. Microsoft.SharePoint.exe: A process related to Microsoft SharePoint, often part of enterprise collaboration tools that integrate with the Office 365 suite.
11. PhoneExperienceHost.exe: Part of the integration between a Windows PC and a mobile device (e.g., the "Your Phone" app for syncing data with smartphones).

**User-Installed and Miscellaneous Applications**

These processes are generally associated with third-party applications that are installed on the system, Some processes are related to specialized functions or utilities within Windows and their description are mentioned here.
1. WinRAR.exe: A file compression utility, commonly used to open and create RAR and ZIP files.
2. python.exe / py.exe:These are the executables for Python, a popular programming language. python.exe runs Python scripts, while py.exe is used as a launcher for Python scripts.
3. msedge.exe: The main process for the Microsoft Edge browser, which is used for web browsing.
4. HxTsr.exe: Associated with the Office Hub app, part of the Microsoft 365 suite.
5. MemCompression: Handles the compression of data in memory to free up system resources.
