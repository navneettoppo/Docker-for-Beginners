# Docker Installation

## Pre-requisites
- Git
- Docker

## Step 1: Git - Linux, Windows & MacOS
- Git installation
    - Linux
        ```
        sudo apt-get install -y git                       #Ubuntu/Debian
        sudo yum install -y git                           #Redhat/AmazonLinux
        git --version
        ```

    - Windows ()
        Standalone Installer
            32-bit Git for Windows Setup. https://github.com/git-for-windows/git/releases/download/v2.38.0.windows.1/Git-2.38.0-32-bit.exe
            64-bit Git for Windows Setup. https://github.com/git-for-windows/git/releases/download/v2.38.0.windows.1/Git-2.38.0-64-bit.exe

        Portable ("thumbdrive edition")
            32-bit Git for Windows Portable. https://github.com/git-for-windows/git/releases/download/v2.38.0.windows.1/PortableGit-2.38.0-32-bit.7z.exe
            64-bit Git for Windows Portable. https://github.com/git-for-windows/git/releases/download/v2.38.0.windows.1/PortableGit-2.38.0-32-bit.7z.exe
    
    - MacOS
        ```
        brew install git                                   #Homebrew
        sudo port install git                              #MacPorts
        ```

## Step 2: Docker - Linux, Windows & MacOS
- Docker Installation
    - Linux
        - Ubuntu/Debian
        ```
        sudo apt-get remove docker docker-engine docker.io containerd runc
        sudo apt-get install -y ca-certificates && apt-get install -y curl && apt-get install -y gnupg && apt-get install -y lsb-release
        sudo hostnamectl set-hostname nav-docker
        sudo mkdir -p /etc/apt/keyrings
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
        echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
        sudo apt-get update -y
        sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin docker.io
        service docker status
        usermod -aG docker ubuntu
        docker version
        docker-compose version
        ```
        - Redhat/AmazonLinux
        ```
        sudo yum remove docker docker-engine docker.io containerd runc
        sudo yum install -y ca-certificates && yum install -y curl && yum install -y gnupg && yum install -y lsb-release
        sudo hostnamectl set-hostname nav-docker
        sudo mkdir -p /etc/apt/keyrings
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
        echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
        sudo yum update -y
        sudo yum install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin docker.io
        systemctl docker status
        usermod -aG docker ubuntu
        docker version
        docker-compose version
        ```
    - Windows
      Docker Setup (https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=dd-smartbutton&utm_location=header)
      https://www.docker.com/products/docker-desktop/
    
    - MacOs
      Docker Setup (https://www.docker.com/products/docker-desktop/)