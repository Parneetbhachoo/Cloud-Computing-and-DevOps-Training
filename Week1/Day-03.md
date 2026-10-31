
# Day 03 — Linux Permissions, Web Servers and SSH Troubleshooting

**Training Date:** 02 July 2026

## 1. Overview

The third day of the Master Class Program on Cloud Computing and DevOps focused on Linux file permissions, user and group management, server fundamentals, and common web servers. The session also covered common HTTP errors and practical troubleshooting of SSH connections.

The practical work helped develop an understanding of how Linux controls access to files and directories, how web servers handle requests, and how connectivity issues can be identified and resolved.

## 2. Topics Covered

### 2.1 Linux Ownership: Owner, Group and Others

Learned how Linux organizes file and directory ownership into three categories:

- **Owner:** The user who owns a particular file or directory.
- **Group:** A group of users who can be assigned shared access permissions.
- **Others:** All users who are neither the file owner nor members of the file's owning group.

This ownership model helps Linux manage access to files and directories in a controlled manner.

### 2.2 Linux File Permissions

Studied the three basic types of Linux permissions:

- **Read (`r`):** Allows a user to view the contents of a file. For directories, it allows the user to list their contents.
- **Write (`w`):** Allows a user to modify a file. For directories, it allows the user to create, delete, or rename entries, subject to other access restrictions.
- **Execute (`x`):** Allows a user to execute a file as a program or script. For directories, it allows the user to access entries within the directory when the required permissions are satisfied.

These permissions can be assigned separately to the owner, group, and others.

### 2.3 Common Linux Permission Sets

Learned to interpret common Linux permission representations.

| Symbolic Permission | Numeric Value | Meaning |
|---|---:|---|
| `rwx` | 7 | Read, write and execute permissions are granted. |
| `rw-` | 6 | Read and write permissions are granted, but execution is not allowed. |
| `r-x` | 5 | Read and execute permissions are granted, but writing is not allowed. |
| `r--` | 4 | Only read permission is granted. |
| `---` | 0 | No permissions are granted. |

Linux commonly represents these permissions using a three-digit numeric format: the first digit represents the owner, the second represents the group, and the third represents others.

For example, `755` means:
- Owner: `rwx` (7)
- Group: `r-x` (5)
- Others: `r-x` (5)

Similarly, `644` means the owner can read and write the file, while the group and others can only read it.

### 2.4 The `chmod` Command

Studied the `chmod` command, which is used to change file and directory permissions in Linux.

**Syntax:**
```bash
chmod permissions filename
```

**Example:**
```bash
chmod 755 script.sh
```

This command assigns read, write and execute permissions to the owner, and read and execute permissions to the group and others.

The command can also modify permissions symbolically, such as:

```bash
chmod u+x script.sh
```

This adds execute permission for the file's owner.

### 2.5 The `chown` Command

Learned about the `chown` command, which changes the owner of a file or directory and can also change its group.

**Syntax:**
```bash
chown username filename
```

**Example:**
```bash
sudo chown user1 file.txt
```

This changes the owner of `file.txt` to `user1`, provided the command is run with the necessary privileges.

To change both the owner and group:

```bash
sudo chown user1:developers file.txt
```

These commands are useful for managing access and maintaining appropriate ownership across Linux systems.

### 2.6 Introduction to Servers

Learned the fundamentals of servers and their role in computer networks.

A **server** is a computer or software system that provides services, resources, or data to other computers called clients.

Examples include:
- Web servers that deliver websites.
- File servers that store and share files.
- Database servers that manage and provide access to data.
- Application servers that run application logic.

Servers are important in cloud computing and DevOps because they host applications, process requests, and provide services to users and other systems.

### 2.7 Common Web Servers: Apache and Nginx

Explored two widely used web server technologies.

**Apache HTTP Server**
- An open-source web server used to serve websites and web applications.
- Supports configurable modules and flexible server configuration.
- Can serve static content and work with application technologies.

**Nginx**
- An open-source web server known for its event-driven architecture.
- Efficiently handles many simultaneous connections.
- Commonly used for serving static content, reverse proxying, and load balancing.

Both Apache and Nginx are widely used to host websites and support modern web infrastructure.

### 2.8 Common Server Errors

Studied common HTTP error responses encountered while accessing websites.

**404 Not Found**

A 404 error indicates that the server cannot find the requested resource. This may happen because the URL is incorrect, the resource has been moved, or the requested file does not exist at the specified location.

**403 Forbidden**

A 403 error indicates that the server understood the request but refused to provide access to the requested resource. This can occur because of file permissions, server access rules, or other authorization restrictions.

Understanding these errors helps with identifying and troubleshooting website access problems.

## 3. Practical Implementation

### 3.1 Understanding and Managing Linux Permissions

Worked with the concepts of Linux file ownership and permissions, including:
- Owner, group, and others.
- Read, write, and execute permissions.
- Common numeric permission sets.
- The purpose and usage of the `chmod` and `chown` commands.

### 3.2 Web Server Fundamentals and Error Identification

Explored the purpose of web servers such as Apache and Nginx and learned to distinguish between common HTTP errors, including 404 Not Found and 403 Forbidden.

### 3.3 SSH Troubleshooting and Remote Connectivity

Identified and resolved issues encountered during SSH login and successfully established remote connections between macOS and Linux in both directions.

The troubleshooting process reinforced the importance of checking network connectivity, destination IP addresses, SSH service availability, login credentials, and access permissions.

Successfully connecting in both directions helped build practical familiarity with remote administration across different operating systems.

## 4. Key Learnings

- Understood Linux ownership through the owner, group, and others model.
- Learned the meaning of read, write, and execute permissions.
- Interpreted common numeric permission values such as `755` and `644`.
- Understood how `chmod` and `chown` are used to manage permissions and ownership.
- Learned the role of servers in providing network services.
- Explored Apache and Nginx and their common use cases.
- Distinguished between HTTP 404 Not Found and 403 Forbidden errors.
- Developed troubleshooting skills by resolving SSH login problems.
- Successfully established SSH connectivity between Linux and macOS in both directions.

## 5. Outcome

Developed a stronger understanding of Linux access control, server fundamentals, and web server technologies. The session also improved practical troubleshooting skills through successful SSH connectivity between Linux and macOS, providing useful foundational knowledge for server administration and DevOps workflows.
