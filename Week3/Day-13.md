
# Day 13 — Docker Fundamentals and Containerization

**Training Date:** 16 July 2026

## 1. Overview

Day 13 focused on understanding Docker and the fundamentals of containerization. The session explored how Docker helps package and run applications in isolated environments, making them more consistent and portable across different systems.

Hands-on practice included pulling the `hello-world` image from Docker Hub, exploring the execution of an Ubuntu container on Windows using Windows Subsystem for Linux 2 (WSL2), and creating sample website projects using Docker.

The session also introduced the main components of Docker, including the Docker Engine, Docker CLI, and related tools. These concepts provided a foundation for understanding how container images are downloaded, how containers are created and executed, and how Docker can simplify application deployment.

## 2. Topics Covered

### 2.1 Introduction to Docker

Docker is a platform that allows developers to build, package, distribute, and run applications using containers.

In traditional application deployment, an application may behave differently on different computers because of differences in operating systems, software libraries, dependencies, and configurations.

Docker helps reduce these differences by packaging an application and the components it requires into a container-based workflow.

#### Why Docker Is Used

Docker is widely used in software development and DevOps for the following reasons:

- **Portability:** Applications packaged as Docker images can be transferred between compatible environments.
- **Consistency:** Containers help maintain a predictable application environment across development and deployment.
- **Isolation:** Applications can run in separate containers instead of sharing the same application environment.
- **Efficient Resource Utilization:** Containers generally share the host operating system kernel rather than running a separate full operating system for every application.
- **Simplified Deployment:** Applications can be packaged into reusable images and deployed through repeatable steps.
- **Automation:** Docker can be integrated into CI/CD pipelines to automate application builds, testing, and deployment workflows.

For example, a website can be packaged into a Docker image and run as a container on a compatible system without manually configuring every component from scratch.

### 2.2 Understanding Containerization

**Containerization** is the process of packaging an application and its required components so that it can run in an isolated environment called a container.

A container provides an environment in which an application can execute while remaining separated from other applications running on the same host.

Containerization helps developers move applications between environments with fewer configuration differences.

#### How Containerization Works

1. An application and its required files are prepared.
2. A Docker image is created containing the application and its required runtime components.
3. The image is stored locally or obtained from a container registry.
4. A container is created from the image.
5. The application runs inside the container.

This approach makes it easier to distribute and deploy applications consistently.

### 2.3 Introduction to Docker Images

A **Docker image** is a reusable, read-only template used to create containers. It contains the filesystem components, application files, dependencies, and configuration needed for the intended application environment.

Images can be built using a Dockerfile or downloaded from a container registry such as Docker Hub.

Key characteristics of Docker images include:

- They serve as templates for creating containers.
- They can be reused to create multiple container instances.
- They can be stored and distributed through container registries.
- They contain image layers that can be reused to make image storage and distribution more efficient.

For example, the `hello-world` image provides a simple way to verify that Docker can download an image and run a container from it.

### 2.4 Pulling the Hello World Image from Docker Hub

Docker Hub is a container image registry that allows users to find, download, and share container images.

During the session, the `hello-world` image was pulled from Docker Hub for hands-on practice.

The `hello-world` image is commonly used to verify a Docker installation because it runs a small program that displays a confirmation message.

The basic command used for this purpose is:

```bash
docker pull hello-world
```

#### Understanding the Command

- `docker` invokes the Docker command-line interface.
- `pull` instructs Docker to download an image from a registry.
- `hello-world` specifies the image to download.

After pulling the image, it can be run using:

```bash
docker run hello-world
```

The `docker run` command creates a container from the image and starts it. The program displays its message and then exits.

This exercise helps demonstrate the basic workflow of downloading an image and running a container.

### 2.5 Understanding Docker Containers

A **Docker container** is an instance of a Docker image. It provides an environment in which an application can run.

A container can be running, stopped, or exited, depending on the state of its main process and the actions performed on it.

Important characteristics include:

- Containers are created from images.
- They provide isolated application environments.
- They can be started, stopped, restarted, and removed.
- Multiple containers can be created from the same image.
- A container's writable layer is separate from the original image layers.

For example, a Docker image containing a web server can be used to create a container that runs the web server and serves a website.

### 2.6 Exploring Ubuntu Containers on Windows Using WSL2

The session explored running an Ubuntu container on Windows using Windows Subsystem for Linux 2 (WSL2).

**WSL2** is a Windows feature that provides a Linux environment using a lightweight virtual machine and a real Linux kernel. It allows developers to use Linux tools and workflows while working on a Windows computer.

Docker Desktop can use WSL2 as its Linux environment for running Linux containers on Windows.

#### Why WSL2 Is Useful

- It provides access to Linux tools and command-line utilities on Windows.
- It supports Linux-based development workflows.
- It allows compatible Linux containers to run through Docker Desktop.
- It helps developers practice Linux and containerization without needing a separate physical Linux computer.

#### Understanding an Ubuntu Container

Ubuntu is a Linux distribution commonly used for development, servers, and cloud environments.

An Ubuntu Docker image provides a Linux userspace environment that can be used to create containers. It is useful for exploring Linux commands, application dependencies, and container behavior.

For example, the following command can start an interactive Ubuntu container if Docker is configured correctly:

```bash
docker run -it ubuntu bash
```

Command breakdown:

- `docker run` creates and starts a container.
- `-i` keeps the interactive input open.
- `-t` provides a terminal interface.
- `ubuntu` specifies the image.
- `bash` starts the Bash shell inside the container.

If the Ubuntu image is not already available locally, Docker will attempt to pull it from the configured registry.

An Ubuntu container is not the same as a complete standalone virtual machine. It normally shares the host's Linux kernel through Docker's container runtime environment.

### 2.7 Understanding the Docker Engine

The **Docker Engine** is the core technology responsible for building and running containers.

It manages the major operations required to work with container images and containers.

The Docker Engine includes the following important components:

- **Docker Daemon (`dockerd`):** A background service that manages Docker objects such as images, containers, networks, and volumes.
- **Docker API:** An interface through which tools and clients communicate with the Docker daemon.
- **Container Runtime Components:** Components responsible for creating and running containers using the configured container runtime.

When a user requests an operation such as creating a container, the Docker client communicates with the Docker daemon through the Docker API.

The daemon then coordinates the required operations to fulfill the request.

### 2.8 Understanding the Docker CLI

The **Docker Command-Line Interface (CLI)** is a tool used to interact with Docker through commands.

It allows users to perform tasks such as downloading images, creating containers, inspecting their status, and managing container resources.

Common Docker commands include:

| Command | Purpose |
|---|---|
| `docker --version` | Displays the installed Docker client version. |
| `docker pull hello-world` | Downloads the Hello World image. |
| `docker images` | Lists locally available images. |
| `docker run hello-world` | Creates and runs a container from the Hello World image. |
| `docker ps` | Lists running containers. |
| `docker ps -a` | Lists containers, including stopped containers. |
| `docker stop CONTAINER_ID` | Stops a running container identified by its ID or name. |

These commands provide a basic introduction to interacting with Docker and managing containerized applications.

### 2.9 Docker Desktop and Related Tools

Docker Desktop provides a graphical application for managing Docker on supported desktop operating systems, including Windows and macOS.

It integrates tools and services that help users build, run, and manage containers. On Windows, it can integrate with WSL2 to run Linux containers.

The session introduced Docker's main components and related tools to understand how the different parts work together.

A simplified workflow is:

1. The user enters a command through the Docker CLI or a supported graphical interface.
2. The Docker client sends the request through the Docker API.
3. The Docker daemon manages the requested operation.
4. The required image is downloaded or an existing local image is used.
5. A container is created and started when requested.

This explains how the Docker interface, engine, and container runtime work together to run applications.

### 2.10 Creating Sample Website Projects Using Docker

Sample website projects were created using Docker for practical experience with containerized applications.

A website typically consists of files such as HTML, CSS, JavaScript, and images. These files can be served through a web server running inside a Docker container.

Docker can help package the website's serving environment so it can be deployed more consistently.

#### General Workflow for a Docker-Based Website

1. Prepare the website files, such as `index.html` and image assets.
2. Choose a suitable web server image.
3. Configure the website files to be available to the web server inside the container.
4. Create and start a container from the selected image.
5. Configure port mapping when access from the host computer is required.
6. Open the mapped address in a browser to test the website.

For example, a web server container can expose its internal HTTP port to a port on the host computer. The website can then be accessed through the host's mapped port.

The exact setup depends on the web server image, the project files, and the Docker configuration being used.

This practical exercise demonstrated how Docker can be used to run sample web applications in containerized environments.

## 3. Practical Implementation

### 3.1 Pulling the Hello World Image

The `hello-world` image was downloaded from Docker Hub to explore the image-pulling process and gain hands-on familiarity with Docker.

### 3.2 Exploring Ubuntu on Windows Through WSL2

An Ubuntu container environment was explored on Windows using WSL2, providing exposure to Linux-based container workflows.

### 3.3 Exploring Docker Components

The Docker Engine, CLI, and related tools were studied to understand how commands are processed and how Docker manages images and containers.

### 3.4 Creating Sample Website Projects

Sample website projects were created using Docker to gain practical experience with containerized web applications and understand how Docker can support website deployment.

## 4. Key Learnings

The main learnings from Day 13 were:

- Understood Docker and the concept of containerization.
- Learned why Docker is useful for application packaging and deployment.
- Pulled the `hello-world` image from Docker Hub for hands-on practice.
- Understood the relationship between Docker images and containers.
- Explored running an Ubuntu container on Windows using WSL2.
- Learned about the Docker Engine, Docker CLI, and related tools.
- Understood how Docker commands interact with Docker's underlying components.
- Created sample website projects using Docker.
- Learned how containers can support consistent application execution and repeatable deployment workflows.

## 5. Learning Outcome

Day 13 strengthened the foundational understanding of Docker and containerization through image-pulling practice, exploration of Ubuntu containers on Windows, and sample website projects.

The session established how Docker images are used to create containers, how the Docker Engine and CLI work together, and how containerization can simplify the process of packaging and running web applications.

These concepts provide a foundation for further learning in container management, application deployment, and automated CI/CD pipelines.

---

[⬅️ Back to Week 3](README.md) | [⬅️ Back to Main Training Diary](../README.md)
