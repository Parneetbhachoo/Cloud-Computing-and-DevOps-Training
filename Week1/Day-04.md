
# Day 04 — DNS, Web Security, FTP and Web Server Configuration

**Training Date:** 03 July 2026

## 1. Overview

The fourth day of the Master Class Program on Cloud Computing and DevOps focused on understanding how websites are accessed over the internet, the role of domain names and name servers, secure web communication, FTP-based file transfer, and web server configuration.

The session also included practical work involving the creation of an FTP account on InfinityFree and the installation and configuration of Apache and Nginx on Linux using terminal commands.

## 2. Topics Covered

### 2.1 Domain Names, Name Servers and Web Servers

Learned how domain names, name servers, and web servers work together to make websites accessible over the internet.

- **Domain Name:** A human-readable address used to access a website, such as `example.com`.
- **DNS (Domain Name System):** A system that translates domain names into information needed to locate internet services, commonly including IP addresses.
- **Name Server:** A server that provides DNS information for a domain or helps resolve DNS queries.
- **Web Server:** Software that receives HTTP requests and delivers website content to clients, such as web browsers.

**How they work together:**

1. A user enters a domain name into a browser.
2. DNS resolution helps the browser discover the appropriate server IP address.
3. The browser sends an HTTP or HTTPS request to the server.
4. The web server processes the request and returns the requested content.
5. The browser displays the website to the user.

### 2.2 HTTP and HTTPS

Studied the difference between HTTP and HTTPS.

**HTTP (Hypertext Transfer Protocol)** is a protocol used for communication between web browsers and web servers.

**HTTPS (Hypertext Transfer Protocol Secure)** uses HTTP over an encrypted connection secured by TLS.

Key differences:

- **HTTP:** Communication is not encrypted by the protocol itself, so transmitted information may be exposed to interception or modification.
- **HTTPS:** Encrypts communication between the client and server, helping protect data confidentiality and integrity.
- **Default Ports:** HTTP commonly uses port 80, while HTTPS commonly uses port 443.

HTTPS is particularly important when transmitting login credentials, personal information, payment details, or other sensitive data.

### 2.3 SSL Certificates and Secure Communication

Learned about SSL certificates and their role in securing websites.

Although commonly called SSL certificates, modern HTTPS connections generally use **TLS (Transport Layer Security)**.

A TLS certificate helps a browser verify the identity of a website's server. TLS also establishes the cryptographic parameters used to encrypt communication.

Important purposes include:

- Authenticating the website's identity.
- Helping prevent unauthorized interception or modification of data.
- Enabling encrypted communication between the browser and server.

A valid certificate is an important part of HTTPS, although website security also depends on correct server configuration and other security practices.

### 2.4 Search Operators and Sitemaps

Explored ways to locate information on websites more efficiently.

**Search Operators**

Search operators are special terms used in search engines to narrow or refine search results.

Example:

```text
site:example.com
```

The `site:` operator restricts search results to a specified website or domain.

Another example:

```text
site:example.com documentation
```

This searches for pages containing relevant information from the specified domain.

**Sitemaps**

A sitemap is a file that lists URLs from a website to help search engines discover and understand its pages.

A commonly used sitemap location is:

```text
https://example.com/sitemap.xml
```

The actual location depends on the website. Sitemaps support content discovery and indexing, but they do not guarantee that every listed page will appear in search results.

### 2.5 FTP and Website File Management

Learned about FTP and its use in transferring files between computers and servers.

**FTP (File Transfer Protocol)** is a protocol designed for transferring files over a network.

It can be used to upload website files to a hosting server, download files, and manage remote directories.

Also explored the role of WinSCP, a file transfer client that supports protocols such as SFTP and FTP.

- **FTP:** A file transfer protocol that does not encrypt credentials or data by itself.
- **SFTP:** A file transfer protocol that operates over SSH and provides encrypted communication.
- **WinSCP:** A tool for transferring and managing files between a local computer and a remote server.

For secure file transfers, SFTP or another appropriately secured transfer method is preferable to unencrypted FTP.

### 2.6 InfinityFree Hosting

Explored InfinityFree as a free web hosting platform and created an FTP account for website file management.

Understood how hosting platforms provide access to server resources and how FTP-compatible credentials can be used with a supported file transfer client to manage website files.

## 3. Practical Implementation

### 3.1 Creating an FTP Account on InfinityFree

- Accessed the InfinityFree hosting platform.
- Created an FTP account.
- Learned about the credentials required to connect a file transfer client to a hosting server.
- Explored how FTP tools can be used to transfer and manage website files.

### 3.2 Installing and Configuring Apache on Linux

Installed and configured Apache HTTP Server using Linux terminal commands.

Learned how Apache can be used to serve website content and how web server configuration helps make applications accessible through HTTP requests.

### 3.3 Installing and Configuring Nginx on Linux

Installed and configured Nginx using terminal commands.

Explored its role in serving web content and its use in web hosting and application infrastructure.

### 3.4 Understanding Website Deployment

Connected the concepts of domains, DNS, hosting, file transfer, and web servers to understand the main components involved in publishing a website.

Learned how website files and server configuration work together to make web content available to users.

## 4. Key Learnings

- Understood the relationship between domain names, DNS, name servers, and web servers.
- Learned how a browser locates and communicates with a website's server.
- Distinguished between HTTP and HTTPS.
- Understood the role of TLS certificates in website authentication and encrypted communication.
- Explored the `site:` search operator and the purpose of website sitemaps.
- Learned the fundamentals of FTP and the use of WinSCP for file transfer.
- Created an FTP account on InfinityFree.
- Gained hands-on experience installing and configuring Apache and Nginx on Linux.
- Developed a better understanding of website hosting, server configuration, and deployment.

## 5. Outcome

Developed a foundational understanding of the technologies involved in making websites accessible and secure over the internet. Practical exposure to FTP account creation and Apache and Nginx configuration strengthened understanding of web hosting and server administration in a DevOps environment.
