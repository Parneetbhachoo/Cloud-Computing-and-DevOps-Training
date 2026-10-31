
# Day 05 — Web Servers, Databases and Website Hosting

**Training Date:** 06 July 2026

## 1. Overview

The fifth day of the Master Class Program on Cloud Computing and DevOps focused on understanding web servers, how browsers communicate with servers, commonly used web server technologies, databases, and Server-Side Rendering (SSR).

The practical session involved installing and configuring Apache Web Server, creating a personal portfolio website, adding images, accessing the website locally and through the server's IP address, and inspecting Apache access logs.

## 2. Topics Covered

### 2.1 Server vs. Web Server

Learned the difference between a server and a web server.

- **Server:** A computer or software system that provides services, resources, or data to other systems over a network.
- **Web Server:** Software that receives HTTP or HTTPS requests from clients and returns web content or other HTTP responses.

A web server is one type of server. Other servers include database servers, file servers, and application servers.

### 2.2 How a Browser Communicates with a Web Server

Studied the basic workflow involved in accessing a website:

1. A user enters a URL into a web browser.
2. The browser identifies the destination server using the domain name or IP address.
3. The browser sends an HTTP or HTTPS request.
4. The web server processes the request and locates the requested resource or passes the request to an application.
5. The server sends an HTTP response.
6. The browser processes the response and displays the webpage.

This process helps explain how websites are delivered to users over a network.

### 2.3 Common Web Server Technologies

Explored several web server technologies and their common uses.

- **Apache HTTP Server:** An open-source web server used to host websites and serve static content.
- **Nginx:** A web server commonly used for serving static content, reverse proxying, and load balancing.
- **Apache Tomcat:** A Java servlet container used to run Java web applications and handle servlet-based requests.
- **Kestrel:** A web server for ASP.NET Core applications built on the .NET platform.

Also received an introduction to their configuration files and the role of configuration in controlling server behaviour, document locations, ports, and request handling.

### 2.4 Introduction to Databases

Learned about popular database technologies used in modern applications.

- **MySQL:** A relational database management system that stores structured data in tables and supports SQL queries.
- **MongoDB:** A document-oriented NoSQL database that stores data in flexible, JSON-like documents.
- **Firebase:** Google's application development platform that provides services including databases, authentication, hosting, and other backend capabilities.

Understood that databases help applications store, organize, retrieve, and manage information.

### 2.5 Server-Side Rendering (SSR)

Learned about Server-Side Rendering, a technique in which a server generates a webpage's HTML before sending it to the browser.

SSR can allow users to receive meaningful HTML content directly from the server and can support search engine indexing and initial page rendering.

### 2.6 Apache Document Root and Configuration

Studied the role of the Apache document root, which specifies the directory from which Apache serves website files.

On many Linux distributions, the default Apache document root is:

```text
/var/www/html
```

Files placed in this directory can be served by Apache when the server configuration permits access.

Also explored the importance of Apache configuration files in controlling how the web server operates.

### 2.7 Apache Access Logs

Learned about Apache access logs and their role in monitoring web server activity.

Access logs typically record details such as:
- The client's IP address.
- The requested resource.
- The request method.
- The HTTP response status code.
- The time of the request.

These records help administrators understand incoming requests and investigate website access or response issues.

## 3. Practical Implementation

### 3.1 Installing and Configuring Apache

- Installed and configured Apache Web Server.
- Started the Apache service.
- Checked the service status to verify that the server was running.
- Learned how to manage the web server service during website deployment.

### 3.2 Creating a Personal Portfolio Website

- Created a personal portfolio website.
- Added images to the website.
- Placed the website files in the appropriate Apache-served directory.
- Prepared the webpage for access through the local web server.

### 3.3 Accessing the Website

Tested the hosted portfolio website using a web browser.

**Local access:**

```text
http://localhost
```

**Access through the server's IP address:**

```text
http://<SERVER_IP>
```

The IP address placeholder represents the actual address of the server.

Successfully accessed the website locally and through the server's IP address.

### 3.4 Inspecting Apache Access Logs

Viewed Apache's access log to understand how browser requests are recorded.

This provided practical exposure to server monitoring and helped connect browser activity with the requests received by the web server.

### 3.5 Restarting Apache

Learned how to restart the Apache service when configuration changes or other administrative operations require it.

Also explored how server administration can be performed while aiming to minimize disruption to a hosted website.

A service restart can briefly interrupt access, so it should not be assumed to occur without any downtime.

## 4. Key Learnings

- Understood the difference between a general-purpose server and a web server.
- Learned the basic request-response workflow between a browser and a web server.
- Explored Apache, Nginx, Tomcat, and Kestrel.
- Received an introduction to MySQL, MongoDB, and Firebase.
- Understood the concept of Server-Side Rendering.
- Learned about Apache's default document root on many Linux distributions.
- Installed, configured, and started Apache Web Server.
- Created a personal portfolio website and added images.
- Successfully accessed the website through localhost and the server's IP address.
- Inspected Apache access logs and learned about their role in monitoring requests.
- Gained familiarity with basic web server service management.

## 5. Outcome

Gained practical experience with Apache Web Server configuration and website hosting. Creating and accessing a personal portfolio website strengthened understanding of the interaction between browsers, web servers, and website files. Inspecting access logs also introduced the role of server monitoring in web administration and DevOps workflows.
