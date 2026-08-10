# Section A: Operating Systems Introduction

## Operating System

An **operating system (OS)** is the core software that coordinates everything happening on a computer. It sits between the user, applications, and the system's physical hardware, acting as the invisible manager that keeps the entire machine running as one unified system.

Without an OS, each application would need direct control over the CPU, memory, files, devices, and security. This would quickly cause conflicts, and the OS handles this by acting as the central organizer.

---

## System Privilege Layers

Inside a modern computer, different parts of the system operate at various permission levels. Some components can communicate directly with the hardware, while regular applications run in a safe, restricted environment.

This separation is intentional and helps prevent conflicts and security issues.

### Kernel Space

The **kernel space** is the privileged, locked-down area of the OS.

This is where the kernel, the part of the OS that directly manages hardware and system resources, runs.

It has unrestricted access to:

- CPU
- Memory
- Storage
- Hardware components

### User Space

**User space** is where standard applications run.

Applications in user space are deliberately prevented from accessing hardware directly.

Whenever they need to:

- Open or save a file
- Play a sound
- Connect to Wi-Fi

they must make a **system call** and request that the kernel act on their behalf.

---

## Operating System Duties

| OS Responsibility | What the OS Does | Example |
|---|---|---|
| **Process Management** | Creates, schedules, prioritizes, and terminates running programs. The OS decides how much CPU time each process gets, making multitasking feel seamless. | Opening multiple apps such as a browser, music player, and social media without the computer freezing. |
| **Memory Management** | Allocates RAM to processes, protects applications from other processes, and reclaims memory when apps are closed. When RAM runs low, the OS uses virtual memory to keep the system stable. | Opening multiple applications while keeping them isolated so they do not interfere with or crash each other. |
| **File System Management** | Organizes files into directories and handles naming, paths, permissions, and metadata such as name, size, type, and timestamps. | Creating a new folder, saving a path, or setting a file to "read only". |
| **User Management** | Handles multiple user accounts, authentication, and permissions to determine who can access what. | Logging in with a password and keeping your files inaccessible to other user accounts. |
| **Device Management** | Loads drivers and provides a universal interface through hardware abstraction so applications can communicate with devices. | Plugging in a new mouse, printer, or external hard drive and having it work immediately. |

---

## OS Interfaces

Interaction with the OS can be divided into two main parts:

1. **Graphical User Interface (GUI)**
2. **Command-Line Interface (CLI)**

### GUI

A **GUI** provides a graphical representation of the information and functions available on a computer.

It allows users to interact with the OS using graphical elements such as windows, icons, menus, and buttons.

### CLI

The **CLI** is where you enter specific text-based commands to retrieve or manipulate information.

It provides far more precision, control, and speed, especially for advanced tasks.

---

## OS Security

It is important to understand that every OS also acts as a **security foundation**.

Before antivirus, firewalls, or security tools are introduced, the OS is already enforcing protections in the background.

At a basic level, the OS handles:

### 1. Authentication

Verifies who you are through methods such as:

- Login passwords
- Biometrics

### 2. Permissions

Controls exactly what each user and application is allowed to:

- Read
- Write
- Execute

### 3. Isolation

Keeps every process in its own protected box.

This includes the separation between **kernel space and user space**.

### 4. System Protection

Safeguards critical system files and settings from unauthorized changes.

---

## OS Landscape

| OS Type | Primary Use Case | Key Characteristics |
|---|---|---|
| **Desktop** | Personal computers, daily work, gaming, content creation | Rich graphical interface, runs many apps at once, user-focused |
| **Server** | Web hosting, databases, cloud services, back-end | Headless (no GUI), maximum uptime, multi-user, remote access |
| **Mobile** | Smartphones and tablets | Touch-based UI, power efficient, always connected, app sandboxing |
| **Embedded** | Appliances, cars, IoT devices, smart TVs, routers | Tiny footprint, runs on limited hardware |
| **Virtual / Cloud** | Lab machines, containers, cloud instances | Lightweight, scalable, rapid deployment |

---

## Real-World OS

### Desktop

#### Windows

The most widely used OS on personal computers.

Examples:

- Windows 10 (end-of-life)
- Windows 11

#### macOS

Apple's desktop OS, known for its polished GUI and integration with other Apple devices.

Examples:

- Sonoma (14)
- Sequoia (15)
- Tahoe (26)

#### Linux

Not a single OS but a family of open-source OSs called distributions.

Examples:

- Ubuntu
- Debian
- Fedora

---

### Server

#### Windows

Used in large networks, data centers, and corporate environments.

Examples:

- Server 2016
- Server 2019
- Server 2022
- Server 2025

#### Linux

The vast majority of web servers, trusted for its reliability and open-source nature.

Examples:

- Ubuntu Server
- Debian
- CentOS
- Red Hat

#### Unix

Used in large enterprise environments such as:

- Finance
- Telecom
- Government

Examples:

- IBM AIX
- Oracle Solaris

---

### Mobile

#### Android

The most widely used mobile OS, which runs on phones, tablets, and smart devices.

Examples:

- Android 14-16
- Manufacturer versions

#### iOS

Apple's mobile OS running on:

- iPhones
- iPads
- Other Apple devices

Examples:

- iOS 17
- iOS 18
- iOS 26

---

### Embedded & IoT Devices

#### Embedded Linux

Specialized OS built into devices with dedicated functions.

Examples:

- OpenWrt
- Ubuntu Core
- Yocto Project

#### Real-Time OS

Designed for apps where tasks need guaranteed response times.

Examples:

- FreeRTOS
- VxWorks
- QNX

---

### Virtual & Cloud

#### Cloud / VM

Massive data centers that host:

- Websites
- Apps
- Streaming services

Examples:

- Ubuntu LTS
- Amazon Linux
- Rocky Linux

#### Container-Optimized

Lightweight alternatives to VMs that package just the app and its dependencies.

Examples:

- Alpine Linux
- Bottlerocket AWS
- Flatcar Linux

---

## Why Are There So Many Operating Systems?

Different devices and environments require different capabilities from an OS.

A laptop must be user-friendly, support multitasking, provide strong security, and run many different applications.

Servers require stability, reliability, and the ability to run continuously without interruption.

Mobile devices need power efficiency and hardware integration to extend battery life.

Embedded systems use lightweight operating systems designed for a specialized purpose.

The companies and communities that develop these OSs also have their own goals. Some focus on performance, security, openness, or customization.

Because each environment has different requirements, no single OS is the perfect fit for every situation. Instead, an ecosystem of operating systems has evolved to meet different needs.
