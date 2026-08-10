---
title: Module 2 - Computer Fundamentals
tags:
  - pre-security
  - computer-fundamentals
difficulty: Beginner
prerequisites: []
last_updated: 2026-08-06
---

# Module 2: Computer Fundamentals

## Progress

- ✅ Section A: Inside a Computer System
- ✅ Section B: Computer Types
- ✅ Section C: Client-Server Basics
- ✅ Section D: Virtualization Basics
- ⏳ Section E: Pending

---

# A. Inside a Computer System

## Motherboard

**Role:** The skeleton and nervous system of the computer.

- Connects all computer components.
- Allows communication between all components.

---

## CPU (Central Processing Unit)

**Role:** The brain of the computer.

- Executes instructions and performs calculations.
- Also known as the **processor**.
- Modern CPUs contain multiple cores that can process instructions in parallel.
- Connects to the motherboard through the **CPU socket**.

---

## RAM (Random Access Memory)

**Role:** Short-term memory.

- Stores data temporarily while the computer is running.
- RAM is **volatile**—all stored data is lost when power is removed.
- Modern RAM modules commonly use technologies such as:
  - DDR5 (Double Data Rate 5 Synchronous Dynamic RAM)
  - DDR6
- Newer RAM technologies provide increased speed and performance.

---

## Storage (SSD / HDD)

**Role:** Long-term memory.

### SSD (Solid State Drive)

- Stores data permanently.
- Uses memory chips.
- Has no moving parts.
- Provides much faster speeds.

### HDD (Hard Disk Drive)

- Stores data permanently.
- Uses older technology with moving parts.
- Remains popular because of its large storage capacity at a lower cost.

### Storage Connections

Storage devices connect using:

- SATA cables
- PCI Express slots

---

## Network Adapter

- Enables communication with other computers and networks.
- Available in both wired and wireless versions.
- Often integrated into the motherboard but can also be installed as an expansion card.
- Network cards typically connect through PCI Express ports.

---

## Power Supply (PSU)

**Role:** The heart and lungs of the computer.

- Supplies electrical power to all computer components.
- Must provide enough power for installed hardware.
- If component power requirements exceed the PSU's capacity, the system may fail.
- Receives power from a wall outlet and distributes it through connectors such as:
  - Main motherboard connector
  - Molex connectors

---

## Graphics Card (GPU)

**Role:** Visual Cortex.

- Processes and outputs visual information.
- Receives graphical data from the operating system and applications.
- Sends processed visual output to the monitor.
- Connects to the motherboard through a PCI Express slot.

---

## Input / Output Devices

Input and output devices allow data to be sent to and received from the computer.

### Input Devices

- Keyboard
- Microphone
- Mouse
- Scanner

### Output Devices

- Monitor
- Printer
- Speakers

### Common Connectors

- USB (Universal Serial Bus)
- HDMI (High-Definition Multimedia Interface)
- DisplayPort

---

## Rear I/O Ports

- Connect external peripherals such as keyboards, mice, monitors, and USB devices.
- Typically include USB, network, and video ports.

---

## 24-pin ATX Power Connector

- Main power connector from the PSU.
- Supplies power to the motherboard and multiple components.

---

## SATA Ports

- Connect 2.5" and 3.5" SSDs and HDDs.
- Use thin L-shaped SATA data connectors.

---

## CPU Socket

- Holds the CPU securely on the motherboard.
- A locking lever keeps the processor firmly in place.

---

## PCI Express Slots

### PCI Express x16

- Commonly used for graphics cards.
- Can also support other high-bandwidth expansion cards.

### PCI Express x1 / x4

- Used for:
  - Network cards
  - Capture cards
  - Other expansion cards

---

# Boot Process

## What happens when the power button is pressed?

```text
Press Power Button
        │
        ▼
Firmware Starts
        │
        ▼
POST
        │
        ▼
Select Boot Device
        │
        ▼
Start Bootloader
        │
        ▼
Operating System Starts
```

### Step 1 – Press the Power Button

Pressing the power button sends a signal to the PSU, allowing electrical power to flow through the system.

### Step 2 – Firmware Starts

The computer firmware starts and initializes system hardware.

Modern computers use **UEFI**, while **BIOS** performs the same function on older systems.

### Step 3 – POST (Power-On Self-Test)

The firmware performs POST to verify that required hardware components are present, correctly configured, and functioning.

### Step 4 – Select Boot Device

UEFI maintains a boot order and selects the appropriate storage device containing the operating system.

### Step 5 – Start Bootloader

The bootloader on the selected storage device loads the operating system into RAM.

After the operating system is transferred, UEFI hands control over to the operating system.

---

## Notes

### UEFI

Provides an interface between the operating system and the platform firmware.

UEFI replaces the traditional BIOS.

---

### BIOS

The **Basic Input/Output System (BIOS)** is boot firmware that provides runtime services for the operating system.

It:

- Starts the computer.
- Checks hardware components.
- Loads the operating system according to the configured boot priority.

---

### Operating System (OS)

The operating system acts as the layer between hardware and applications.

It provides applications with access to hardware components such as:

- CPU
- RAM
- Disk storage

Examples include:

- Android
- FreeBSD
- Linux
- macOS
- Windows

---

### LAMP

LAMP stands for:

- Linux
- Apache
- MySQL
- PHP

It is a popular open-source software stack used to host dynamic web applications and is one of the most common environments encountered during penetration testing.

---

# B. Computer Types

## Laptop

- Includes a built-in screen and keyboard.
- Designed for portable everyday computing.
- Battery powered.
- Uses compact cooling components such as:
  - Small fan
  - Heat pipes
  - Heat sink

---

## Desktop

- Includes a screen and keyboard.
- Designed for sustained performance at a fixed location.
- Uses wall power.
- Larger cooling components provide improved airflow and cooling.
- More internal space results in better cooling and sustained performance.

---

## Workstation

- Includes a screen and keyboard.
- Designed for precision and reliability in professional workloads.
- ECC RAM and cache memory are more common.
- Prioritizes accuracy and reliability during long or complex computations.

---

## Server

- Usually operates without a dedicated screen or keyboard.
- Provides services to multiple users over a network.
- Runs continuously.
- Handles requests from multiple users simultaneously.
- Redundant power reduces single points of failure.
- Uptime improves when redundancy is combined with backups and monitoring.

---

## Smartphone

- Pocket-sized computer optimized for battery life and connectivity.
- Examples:
  - iPhone
  - Android phones

---

## Tablet

- Touch-first computer with a larger screen.
- Examples:
  - iPad
  - Drawing tablet

---

## IoT Device

A network-connected device designed for a specific purpose.

Examples include:

- Thermostat
- Smart doorbell
- Fitness tracker

### IoT (Internet of Things)

IoT refers to a network of physical objects embedded with sensors and software that allow them to collect and exchange data over the Internet.

These devices range from household appliances to industrial equipment and vehicles.

---

## Embedded Computer

A computer built into another device.

Examples include:

- Coffee maker controller
- Automatic door sensor
- Lamp dimmer chip

### IoT vs Embedded

Both IoT devices and embedded computers are often small and designed for a specific purpose.

The key difference is connectivity:

- **IoT devices** connect to a network to send data or receive commands.
- **Embedded computers** may not connect to any network and instead perform dedicated tasks within the device.

---

# C. Client-Server Basics

## Client-Server Model

The **client-server model** is a network architecture where a client requests a service and a server provides the requested service.

```text
Client  ─────── Request ───────>  Server
Client  <────── Response ───────  Server
```

A client initiates communication with the server, and the server responds to the client's request.

---

## Client

A **client** is a network application that requests a service.

### Examples

- Web browser
- SSH client
- Email client
- FTP client

A client sends requests to a server and receives the requested service or resource in response.

---

## Server

A **server** is a system, application, or service that provides a service or resource to clients.

A single computer can run multiple servers/services simultaneously.

### Examples

- Web server
- DNS server
- Mail server
- SSH server
- FTP server

The server receives requests from clients, processes them, and sends back a response.

---

## Request and Response

Client-server communication follows a **request-and-response** model.

### Request

A **request** is sent by the client to ask the server for a resource or service.

```text
Client → Request → Server
```

### Response

A **response** is sent by the server after processing the client's request.

```text
Server → Response → Client
```

The response is divided into two parts:

- **Response Header** → contains metadata about the response.
- **Response Body** → contains the requested content.

```text
Response
├── Response Header
└── Response Body
```

## Protocol

A **protocol** is a set of rules that defines how computers communicate.

It specifies:

- What commands are understood
- How requests are structured
- What syntax should be used
- What the response should look like
- How communication is controlled

---

## Port

A **port** is used to identify a particular network service.

A port is a logical endpoint that allows a specific service to communicate over a network.

A port number is used to access a particular service.

---

## DNS

**DNS (Domain Name System)**

It is the protocol responsible for resolving hostnames to their respective IP addresses.

---

## HTTP(S)

- **HTTP** → Hypertext Transfer Protocol
- **HTTPS** → Hypertext Transfer Protocol Secure

HTTP(S) is a **client-server protocol** used primarily for communication on the World Wide Web.

It is a **stateless protocol**, i.e. the server does not inherently remember previous requests made by the client. Each request is treated as an independent request.

---

## HTTP Request Methods

HTTP uses methods to indicate what the client wants to do.

### a) GET

- Used to retrieve data from a server.
- In the Inspect tab → Network section → in the right-hand panel:

  - **Scheme** → tells us which protocol was used (HTTP/HTTPS)
  - **Host** → tells us the name of the host we request resources from
  - **Filename** → indicates which file we requested from the host
  - **Address** → displays the IP address where the website is hosted
  - **Status** → indicates whether the request was successful

When a request is sent, we will get a response from the server.

The response is divided into two parts:

- **Response Header** → contains metadata about the response
- **Response Body** → contains the requested content

### b) POST

- It is generally used to send data to a server.
- Common uses:
  - Login forms
  - Creating accounts
  - Submitting forms
  - Uploading data

### c) PUT

- It is generally used to create / completely replace a resource at a specified location.

### d) DELETE

- It requests the server to delete a resource.

### e) PATCH

- It is used to partially modify an existing resource.
- **PUT** → replaces / updates the whole resource
- **PATCH** → modifies part of the resource

### f) HEAD

- It works similarly to GET, but the server returns the response headers without the response body.
- Useful for checking information such as:
  - Whether a resource exists
  - Content-Type
  - Content-Length
  - Last modification information
- This can be done without downloading the actual content.

### g) OPTIONS

- It asks the server what communication options / methods are available for a resource.

### h) CONNECT

- It is used to establish a network tunnel to the server.

### i) TRACE

- It is primarily a diagnostic method.
- It asks the server to return the request it received, allowing the client to see how the request was processed through the HTTP infrastructure.
- It is generally disabled on production servers because of security considerations.

---

## Note

- HTTP is also called **Request for Comments (RFC)** documents.
- **RFC** is a publication in a series from the principal technical development and standards-setting bodies for the Internet, most prominently the **Internet Engineering Task Force (IETF)**.

# D: Virtualization Basics

Before virtualization, the common approach was:

```text
One server = One application
```

Each application typically ran on its own physical server.

---

## Problems with Traditional Physical Servers

### 1. High Cost

Buying multiple physical servers is expensive, not just the hardware, but also electricity, cooling, maintenance, and data center space.

### 2. Low Utilization

Most applications don't use the server's full capacity. Many servers stayed at **5–20% usage**, wasting CPU, memory, and storage resources.

### 3. Slow Deployment

Setting up new physical servers could take days or weeks.

### 4. Hard to Scale

If an application suddenly needed more resources, you often had to buy yet another server.

---

## Virtualization

Virtualization allows multiple virtual computers to run on a single physical server while sharing its hardware resources.

### Advantages of Virtualization

#### 1. Resource Efficiency

Multiple VMs can share unused CPU, memory, storage, etc.

#### 2. Lower Cost

Fewer physical servers are required.

#### 3. Faster Deployment

A VM can often be created much faster than purchasing and installing a physical server.

#### 4. Isolation

VMs are separated from each other, so problems in one VM generally don't directly affect another.

#### 5. Scalability

Resources can be allocated to VMs as needed.

---

## Hypervisor

- It is the core software used for virtualization.
- It creates and manages VMs and controls how they access the physical computer's resources.

### Main Responsibilities

A hypervisor:

- Creates virtual machines
- Allocates CPU, RAM & storage to VMs
- Keeps VMs isolated from each other
- Manages the VM lifecycle:
  - Start
  - Stop
  - Pause
  - Clone
  - Delete

### Types of Hypervisors

#### Type 1 — Bare-Metal Hypervisor

- It runs directly on physical hardware.

**Characteristics:**

- Fast, efficient, and good performance
- Common in servers & data centers
- Suitable for production environments

**Typical Use Cases:**

- Data centers
- Production servers
- Database servers

> There is no general-purpose OS underneath the hypervisor.

#### Type 2 — Hosted Hypervisor

- It runs on top of an existing OS.

**Characteristics:**

- Easy to install
- Convenient for personal computers
- Good for learning & testing
- Common in home labs

**Typical Use Cases:**

- Software testing
- Kali Linux labs
- Learning virtualization
- Testing suspicious files in isolated environments

**Examples:**

- Oracle VirtualBox
- VMware Workstation

---

## Virtual Machine

- It is a virtualized computer that behaves like an independent computer and is managed by a hypervisor.
- A VM can have its own:
  - OS
  - Applications
  - Files
  - Network configuration
  - Settings

---

## Containers

- They are packages of software that bundles up code & all its dependencies so it can be run reliably in any environment.
- It is a lightweight, isolated environment that runs a single application & all the necessary components to support it.

Containers behave like small, self-contained spaces because:

- They package the application & its dependencies (libraries, tools, versions).
- They share the host's OS, so they start almost instantly.
- They remain isolated from each other, so a misbehaving container doesn't affect the other.
- They can run consistently on any machine, making them perfect for development, testing & scalable deployments.

The easiest way to deploy containers in a VM is using **Docker**.

---

## Docker

- It is an open-source software platform that simplifies the process of building, deploying, & running applications using containerization.
- It makes containerization easier by providing tools for:
  - Creating container images *(a pre-packed recipe/template used to create containers)*
  - Running containers
  - Managing containers
  - Packaging applications with dependencies
  
