
# Week 1 Mini Project — Web Server Deployment and Bash Automation

**Program:** Master Class Program on Cloud Computing and DevOps  
**Project Title:** Build and Configure a Secure Linux Server for a Startup Company  
**Assignment Date:** 03 July 2026

## Project Report

The Week 1 mini project focused on web server deployment using Apache and system monitoring through Bash automation. This documentation covers Task 5 and Task 6 of the practical assignment.


[View Complete Practical Report (PDF)](week-1%20project%20report.pdf)

The PDF contains the implementation report, webpage screenshot, Bash script, and terminal output.

---

# Task 1 — Web Server Deployment Using Apache

## 1. Task Description

The objective was to configure the Apache Web Server, create a webpage containing project and student information, and access the webpage through a browser using localhost and the server's IP address.

The webpage was required to display:

- Project title
- Student name
- Roll number
- Branch
- Current date and time
- A welcome message for visitors

## 2. Implementation Procedure

### Step 1: Verify Apache Installation

Checked whether Apache HTTP Server was installed on macOS.

```bash
httpd -v
```

This command displays the installed Apache version.

### Step 2: Obtain Administrative Privileges

Obtained elevated privileges for server administration.

```bash
sudo -i
```

### Step 3: Verify Apache Configuration

Checked the Apache configuration for syntax errors.

```bash
apachectl configtest
```

### Step 4: Start Apache Web Server

Started the Apache Web Server.

```bash
apachectl -k start
```

### Step 5: Create the Webpage

Used the Apache document root directory to create the webpage.

**Document root:**

```text
/Library/WebServer/Documents/
```

**Command:**

```bash
nano /Library/WebServer/Documents/index.html
```

Created an HTML webpage containing the required project and student details and a welcome message.

### Step 6: Restart Apache

Restarted the server after creating the webpage.

```bash
apachectl restart
```

### Step 7: Access the Webpage Using Localhost

Opened the following address in a web browser:

```text
http://localhost
```

### Step 8: Access the Webpage Using the Server IP

Accessed the webpage using the server's IP address.

```text
http://<SERVER_IP>
```

The placeholder was to be replaced with the actual server IP address.

## 3. Output and Results

The practical report includes a screenshot of the webpage hosted through Apache.

The webpage displays:

- **Project:** Cloud Computing & DevOps Assignment
- **Project Title:** Build and Configure a Secure Linux Server
- **Student Name:** Parneet Kaur
- **Roll Number:** 2435114
- **Branch:** Computer Science and Engineering
- **Current Date and Time**
- **Welcome Message:** Welcome to ABC Tech Solutions Pvt. Ltd.

The screenshot serves as visual evidence of the webpage created for the assignment.

## 4. Outcome

Gained practical experience checking the Apache installation, validating server configuration, starting and restarting the server, creating an HTML webpage, and accessing hosted content through a web browser.

---

# Task 2 — Bash Automation Script

## 1. Task Description

The objective was to develop a Bash automation script named `server_health.sh` to display important system information in a structured server health report.

The script was required to display:

- Current date and time
- Logged-in user
- Hostname
- IP address
- Disk usage
- Memory usage
- CPU load
- System uptime

## 2. Implementation Procedure

### Step 1: Create the Script

Created a Bash script file.

```bash
nano server_health.sh
```

### Step 2: Write the Script

The script used existing command-line utilities to collect and display system information.

```bash
#!/bin/bash

echo "       SERVER HEALTH REPORT"

echo ""
echo "Current Date & Time:"
date

echo ""
echo "Logged-in User:"
whoami

echo ""
echo "Hostname:"
hostname

echo ""
echo "IP Address:"
ipconfig getifaddr en0

echo ""
echo "Disk Usage:"
df -h /

echo ""
echo "Memory Usage:"
vm_stat

echo ""
echo "CPU Load:"
uptime

echo ""
echo "System Uptime:"
uptime

echo "       REPORT COMPLETED"
```

### Step 3: Make the Script Executable

Granted execution permission to the script.

```bash
chmod +x server_health.sh
```

### Step 4: Execute the Script

Ran the script from the terminal.

```bash
./server_health.sh
```

The script displayed the collected information under the heading **SERVER HEALTH REPORT**.

## 3. Output and Results

The practical report contains screenshots of the script and its terminal output.

| Information | Command | Purpose |
|---|---|---|
| Date and time | `date` | Displays the current date and time. |
| Logged-in user | `whoami` | Identifies the current user. |
| Hostname | `hostname` | Displays the system hostname. |
| IP address | `ipconfig getifaddr en0` | Retrieves the IPv4 address of the `en0` interface when available. |
| Disk usage | `df -h /` | Displays disk usage for the root filesystem. |
| Memory usage | `vm_stat` | Displays virtual memory statistics on macOS. |
| CPU load | `uptime` | Displays system load averages. |
| System uptime | `uptime` | Displays how long the system has been running. |

The report concludes with the message **REPORT COMPLETED**.

## 4. Outcome

Created and executed a Bash script that automates the collection and display of basic system information. This demonstrated how shell scripting can combine multiple command-line utilities into a single, repeatable report.

---

# Conclusion

The Week 1 mini project provided practical exposure to web server deployment and basic system monitoring.

- **Task 5:** Focused on Apache configuration and hosting an HTML webpage containing project and student information.
- **Task 6:** Focused on Bash automation through a script that collected and displayed system health information.

These activities strengthened foundational skills in web hosting, server administration, command-line utilities, and automation, which are important areas of Cloud Computing and DevOps.
