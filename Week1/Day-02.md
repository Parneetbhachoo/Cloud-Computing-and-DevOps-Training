
# Day 02 — Operating Systems, Linux Fundamentals and SSH

## 1. Overview

The second day of the Master Class Program on Cloud Computing and DevOps focused on operating systems, software distribution models, Linux fundamentals, virtualization, basic shell programming, and remote access using SSH.

The session included theoretical learning as well as practical implementation. Ubuntu was installed using VirtualBox, basic Linux commands and shell programs were explored, and SSH was used to establish remote access between Windows and macOS environments.

## 2. Topics Covered

### 2.1 Operating Systems

Learned about different operating systems and their characteristics:

- **Linux:** An open-source, Unix-like operating system widely used in servers, cloud infrastructure, and DevOps environments.
- **Windows:** An operating system developed by Microsoft, commonly used on personal computers and in business environments.
- **macOS:** Apple's operating system designed for Mac computers.
- **Android:** A mobile operating system based on the Linux kernel, primarily used in smartphones and tablets.
- **iOS:** Apple's mobile operating system used on iPhones.

Studied the differences between these operating systems in terms of usage, interface, software compatibility, customization, and licensing.

### 2.2 Software Distribution Models

Explored different software distribution and licensing models:

- **Open-Source Software:** Software whose source code is available under a license that permits users to use, inspect, modify, and redistribute it according to the license terms.
- **Freeware:** Software provided at no monetary cost, which may still have restrictions on modification or redistribution.
- **Proprietary Software:** Software controlled by its owner, with usage, modification, and redistribution governed by its license.

### 2.3 Types of Software

Learned about the major categories of software:

- **System Software:** Manages computer hardware and provides a platform for other programs, such as operating systems.
- **Application Software:** Helps users perform specific tasks, such as writing documents or browsing the internet.
- **Utility Software:** Performs maintenance, protection, and optimization tasks, such as file compression, backup, and antivirus scanning.

### 2.4 Linux Fundamentals and File System Structure

Received an introduction to Linux, its command-line interface, and the Bash shell.

Studied the purpose of important Linux directories:

- **`/` (Root Directory):** The top-level directory of the Linux file system.
- **`/home`:** Contains the personal directories of regular users.
- **`/etc`:** Stores system-wide configuration files.
- **`/bin`:** Contains essential user command programs on systems that maintain this directory separately.
- **`/var`:** Stores variable data, including logs and other files that change during system operation.
- **`/usr`:** Contains many user applications, libraries, and supporting files.

Practiced basic Linux commands and explored how the command line can be used to navigate directories and manage files.

### 2.5 Bash and Shell Programming

Learned about **Bash (Bourne Again SHell)**, a command-line shell commonly used in Linux environments.

- Understood the role of a shell in accepting and executing commands.
- Practiced basic shell commands.
- Wrote and executed basic shell programs.
- Explored how shell scripts can automate repetitive tasks.

### 2.6 Virtualization and Hypervisors

Studied virtualization and the role of hypervisors in creating and running virtual machines.

- **Virtualization:** A technology that allows virtual computing environments to run on a physical machine.
- **Hypervisor:** Software or firmware that creates and manages virtual machines.

Explored the difference between bare-metal installation and virtual installation:

- **Bare-Metal Installation:** An operating system is installed directly on the physical computer's hardware.
- **Virtual Installation:** An operating system runs inside a virtual machine managed by virtualization software.

### 2.7 Rufus and Bootable USB Drives

Received an introduction to Rufus, a utility used to create bootable USB drives from ISO images.

Understood how bootable USB drives can be used to install operating systems on physical computers.

### 2.8 Introduction to Vercel

Received an introduction to Vercel and its role in deploying and hosting web applications.

## 3. Practical Implementation

### 3.1 Installing Ubuntu Using VirtualBox

- Installed Ubuntu in a virtual machine using VirtualBox.
- Explored the virtual installation process.
- Understood how a virtual machine allows an operating system to run without replacing the host operating system.
- Learned the practical difference between running an operating system virtually and installing it directly on physical hardware.

### 3.2 Practicing Linux Commands and User Management

- Practiced basic Linux commands.
- Explored the Linux file system through directory navigation.
- Used `sudo` to execute administrative commands.
- Created multiple user accounts and learned about basic user management.
- Wrote and executed basic shell programs.

### 3.3 Establishing SSH Access Between Windows and macOS

Practiced establishing a remote SSH connection between Windows and a Mac.

**SSH (Secure Shell)** is a network protocol that enables secure remote access to another computer through an encrypted connection.

The following workflow was explored:

1. Obtained the IPv4 addresses of both devices.
2. Tested network connectivity between the devices using `ping`.
3. Enabled Remote Login on the Mac to allow incoming SSH connections.
4. Checked the SSH service status and whether port 22 was listening.
5. Used the SSH command with the destination username and IP address.
6. Accepted the host authenticity prompt when appropriate and entered the required password.

#### Important Commands

**Check network connectivity**
```bash
ping <IP_ADDRESS>
```

**Check whether SSH is listening on port 22 on macOS**
```bash
sudo lsof -iTCP:22 -sTCP:LISTEN
```

**Check Remote Login status on macOS**
```bash
sudo systemsetup -getremotelogin
```

**Connect to the remote computer**
```bash
ssh username@ip_address
```

Replace `username` with the account name on the destination computer and `ip_address` with that computer's IPv4 address.

**Note:** The SSH server must be enabled on the destination device. Network access and firewall rules must also permit the connection. Windows can act as an SSH client, provided an SSH client is available. On macOS, Remote Login enables the SSH server. The command for checking Remote Login status is specific to macOS.

## 4. Key Learnings

- Understood the major differences between Linux, Windows, macOS, Android, and iOS.
- Learned the distinctions between open-source, freeware, and proprietary software.
- Identified system, application, and utility software.
- Gained practical experience installing Ubuntu through VirtualBox.
- Understood virtualization, hypervisors, and the difference between bare-metal and virtual installations.
- Learned the structure and purpose of important Linux directories.
- Practiced basic Linux commands, user management, and shell programming.
- Understood the purpose of Rufus and bootable USB drives.
- Learned the fundamentals of SSH and practiced remote access between Windows and macOS.
- Received an introduction to Vercel and its application deployment capabilities.

## 5. Outcome

Developed a practical foundation in Linux, virtualization, operating system concepts, and command-line usage. The session also provided hands-on exposure to shell programming, user management, and secure remote access through SSH, supporting further learning in cloud computing and DevOps.
