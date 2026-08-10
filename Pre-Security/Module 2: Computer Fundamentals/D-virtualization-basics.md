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
  
