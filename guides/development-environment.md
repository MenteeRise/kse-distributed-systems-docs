---
layout: default
title: Development Environment Setup
nav_order: 1
parent: Guides
has_children: false
permalink: /development-environment/
---

# Development Environment Setup

{: .no_toc }

This guide will walk you through setting up a complete development environment for the Distributed Systems course.
Following these steps will ensure you have all the necessary tools to work on lab assignments and your team project.

<details open markdown="block">
  <summary>Table of Contents</summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## System Requirements

Before beginning installation, ensure your system meets these minimum requirements:

| Component | Minimum Requirement                                |
|:----------|:---------------------------------------------------|
| CPU       | 4 cores (8 recommended)                            |
| RAM       | 16GB (32GB recommended)                            |
| Storage   | 10GB free space                                    |
| OS        | Windows 10/11, macOS 12+, or Linux (Ubuntu 20.04+) |
| Network   | Reliable internet connection                       |

## IDE Installation

You can choose between Visual Studio 2022 or JetBrains Rider as your primary IDE.

### Option 1: Visual Studio 2022

1. Download Visual Studio 2022 Community Edition
   from [visualstudio.microsoft.com](https://visualstudio.microsoft.com/vs/community/)
2. Run the installer and select the following workloads:
    - ASP.NET and web development
    - Azure development
    - .NET desktop development
    - .NET Multi-platform App UI development
3. In the Individual components tab, ensure the following are selected:
    - .NET 9.0 Runtime
    - Git for Windows
    - GitHub Extension for Visual Studio

{: .note }
If you're on macOS or Linux, use Visual Studio for Mac or proceed with Option 2 (Rider).

### Option 2: JetBrains Rider

1. Apply for a free educational license
   at [jetbrains.com/community/education](https://www.jetbrains.com/community/education/)
2. Download Rider from [jetbrains.com/rider/download](https://www.jetbrains.com/rider/download/)
3. Install with default settings
4. Install the following plugins:
    - .NET Core User Secrets
    - Docker
    - Kubernetes
    - Rainbow Brackets

## .NET SDK Installation

1. Download the .NET 9.0 SDK
   from [dotnet.microsoft.com/download/dotnet/9.0](https://dotnet.microsoft.com/download/dotnet/9.0)
2. Follow the installation instructions for your operating system
3. Verify installation by opening a terminal or command prompt and running:
   ```bash
   dotnet --version
   ```
   You should see version 9.0.x displayed

## Docker Installation

### Windows

1. Ensure Hyper-V is enabled (Windows 10/11 Pro, Enterprise, or Education)
    - If using Windows Home, you'll need to use WSL 2 backend
2. Download Docker Desktop from [docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
3. Complete the installation and restart your computer if prompted
4. Start Docker Desktop and ensure the service is running

### macOS

1. Download Docker Desktop for Mac
   from [docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
2. Drag Docker to your Applications folder
3. Start Docker and allow any permissions it requests
4. Wait for Docker to start completely (the whale icon in the menu bar stops animating)

### Linux

1. Follow the official Docker Engine installation guide for your distribution:
    - [Ubuntu](https://docs.docker.com/engine/install/ubuntu/)
    - [Debian](https://docs.docker.com/engine/install/debian/)
    - [Fedora](https://docs.docker.com/engine/install/fedora/)
    - [CentOS](https://docs.docker.com/engine/install/centos/)
2. Configure Docker to start on boot:
   ```bash
   sudo systemctl enable docker
   sudo systemctl start docker
   ```
3. Add your user to the docker group to run Docker without sudo:
   ```bash
   sudo usermod -aG docker $USER
   ```
   (Log out and back in for this to take effect)

## Git Client Installation

### Windows

1. Download Git for Windows from [git-scm.com/download/win](https://git-scm.com/download/win)
2. During installation, use the following options:
    - Use Visual Studio Code as Git's default editor (or your preferred editor)
    - Use Git from the Windows Command Prompt
    - Use the OpenSSL library
    - Checkout Windows-style, commit Unix-style line endings
    - Use Windows' default console window
    - Enable file system caching
    - Enable Git Credential Manager

### macOS

1. Install Homebrew if not already installed:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. Install Git using Homebrew:
   ```bash
   brew install git
   ```

### Linux

```bash
# Ubuntu/Debian
sudo apt update
sudo apt install git

# Fedora
sudo dnf install git

# Arch Linux
sudo pacman -S git
```

## Additional Tools

### Postman (API Testing)

1. Download from [postman.com/downloads](https://www.postman.com/downloads/)
2. Install with default settings
3. Create a free account or skip sign-in

### Visual Studio Code (Optional Secondary Editor)

1. Download from [code.visualstudio.com](https://code.visualstudio.com/)
2. Install with default settings
3. Install the following extensions:
    - C# Dev Kit
    - Docker
    - REST Client
    - GitLens
    - YAML

### DataGrip (different database management)

1. Apply for a free educational license
   at [jetbrains.com/community/education](https://www.jetbrains.com/community/education/)
2. Download DataGrip from [jetbrains.com/datagrip/download](https://www.jetbrains.com/datagrip/download/)
3. Install with default settings

### pgAdmin (PostgreSQL GUI)

pgAdmin can be run in a Docker container or installed natively.

**Windows:**
1. Go to: https://www.pgadmin.org/download/pgadmin-4-windows/
2. Download installer.
3. Run it → Follow GUI steps. 
4. Access via Start Menu.

**macOS:**
1. Go to: https://www.pgadmin.org/download/pgadmin-4-macos/
2. Download installer.
3. Run it → Follow GUI steps.
4. Access via Applications folder.

**Linux:**
```bash
curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add -
echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" | sudo tee /etc/apt/sources.list.d/pgadmin4.list
sudo apt update
sudo apt install pgadmin4-desktop
```

### MongoDB Compass

**Windows / MacOS / Linux**:
1. Go to: https://www.mongodb.com/try/download/compass
2. Select OS → Download. 
3. Install via GUI installer. 
4. Run → Connect to MongoDB.

### RedisInsight (by Redis Labs)

**Windows / MacOS / Linux**:
1. Go to: https://redis.com/redis-enterprise/redis-insight/
2. Complete the form to download.
2. Select OS → Download.
3. Install via GUI installer.
4. Run → Connect to Redis.

## Course-Specific Repository Setup

Refer to the [repository setup guide](repo-setup.md) for instructions on creating and configuring your course project
repository.

## Troubleshooting

### Docker Issues

- **Windows:** Ensure Virtualization is enabled in BIOS/UEFI
- **WSL 2 Backend:** Follow [Microsoft's WSL 2 installation guide](https://docs.microsoft.com/windows/wsl/install)
- **Docker Daemon Not Starting:** Check the Docker logs in the application

### .NET SDK Issues

- **Multiple SDK Versions:** Use `dotnet --list-sdks` to view all installed SDKs
- **Path Issues:** Ensure the .NET SDK is in your PATH
- **VS Code .NET Extension:** Install the C# Dev Kit extension for better .NET support

### Git Authentication Issues

- **SSH Keys:** Consider setting up SSH keys for GitHub authentication
- **Git Credential Manager:** Ensure this is enabled for smoother authentication

If you encounter problems not covered here, please post in the course forum or contact the teaching assistants.

## Next Steps

Now that your environment is set up, we recommend:

1. Completing the [Git workflow tutorial](git-workflow.md)
2. Exploring the [Docker basics guide](docker-basics.md)
3. Familiarizing yourself with the [.NET microservices architecture](../reference/dotnet-libraries.md)

## Resources

- [Official .NET Documentation](https://docs.microsoft.com/dotnet/)
- [Docker Documentation](https://docs.docker.com/)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)