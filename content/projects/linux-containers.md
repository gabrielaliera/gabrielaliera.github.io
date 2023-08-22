---
title: "Linux Workstation & Containerized Applications"
#description: "Virtualizes Fedora server with Apache, Samba, & File Transfer Protocol containerized using Linux Containers (LXC)"
dateString: "May 2021 ∙ "
ShowWordCount: true
ShowReadingTime: true
author: Gabriela Liera
draft: false
tags: ["Linux","Windows","Containers","Samba", "Apache","VM Virtual Box", "Fedora", "Documentation"]
showToc: false
weight: 204
cover:
    image: "projects/linux-containers/cover.png"
    alt: "Systems - Virtualizes Fedora server with Apache, Samba, & File Transfer Protocol containerized using Linux Containers (LXC)"
--- 
### 🔗 [GitHub](https://github.com/gabrielaliera/Linux-Containerized_Applications)
### 🔗 [Project Presentation](https://github.com/gabrielaliera/Linux-Containerized_Applications/blob/main/Presentation_CISN-34.pdf)
### 🔗 [Step-by-step Documentation](https://github.com/gabrielaliera/Linux-Containerized_Applications/blob/main/Documentation_CISN34.pdf)

## Project Summary
***
This project is composed of 2 **Linux** systems: a workstation and a virtualized server. Both systems are using **Fedora 35** operating system along with the containerized software, **Linux Containers**. In addition, I used **Oracle VM VirtualBox** to virtualize the workstation and server. This allows users to take the image of our systems and replicate them in their personal devices. Because workstations usually contain a minimal amount of memory and rely upon servers for applications, storage and processing, it is common to keep some applications local.

## Features
***
The client workstation has two containers. The first container is an email program, **Thunderbird**, and the second container is a word processor, **Libre Word**.

In the server, there are also 2 containers. The first container has **Samba** installed so a **Windows** client can access the server files. A user called “smb-user” was added to both the container and the Samba user list in order to access these files with a secure password. The shared Samba folder also contains this documentation. The second container has an **Apache web server** installed in order to create a group web page about this project. This second container also includes **FTP** to allow data transfer. The user “ftp-user” was created with a secure password and configured to the vsftp user list. Firewalls are configured to open all Samba, Apache and FTP ports. In addition, the firewall is configured to allow port forward requests to the appropriate container IP-address. Hence users outside this server can access applications within the container.

## Lessons Learned
***
Through this project, several valuable lessons have been acquired:

1. **System Configuration and Virtualization**:
The project highlighted the significance of effectively configuring and utilizing Linux systems, emphasizing the Fedora 35 distribution. Furthermore, utilizing Oracle VM VirtualBox for virtualization proved essential in creating portable system images.

2. **Containerization with Linux Containers**:
Employing Linux Containers (LXC) provided a streamlined approach to application deployment. This allowed isolation of applications, optimizing resource utilization, and easing management. This experience showcased the adaptability of LXC in creating reproducible environments.

3. **Containerized Applications for Efficiency**:
Recognizing the benefits of keeping certain applications on local workstations due to resource limitations and reliance on servers for broader processing needs was a crucial insight. Containers housing applications such as Thunderbird for emails and Libre Word for word processing optimized the workstation's performance.

4. **Server Application Deployment**:
Deploying applications in server containers demonstrated the utility of this approach. Installing Samba to facilitate Windows client access to server files and Apache for web page creation underscored the versatility of containers in meeting various server-side requirements.

5. **User Management and Security**:
The project highlighted the importance of proper user management for security. Creating specialized users like "smb-user" and "ftp-user" with secure passwords ensured controlled and secure access to resources within containers and server functionalities.

6. **Networking and Firewall Configuration**:
Configuring firewalls for port openings and enabling port forwarding emerged as a crucial aspect. This experience enhanced understanding of networking configurations, enabling external users to access containerized applications securely.

7. **Troubleshooting and Collaborative Learning**:
The journey showcased the necessity of effective troubleshooting and collaborative learning. Dealing with challenges like misconfigured Linux Containers and learning firewall commands for port forwarding demonstrated the value of problem-solving skills and teamwork.

In summary, this project provided me comprehensive learning experience encompassing system configuration, containerization, application deployment, security practices, networking, and collaborative troubleshooting. These insights will undoubtedly contribute to the successful execution of future projects. I will not add new features to this project as I plan to continue working on new projects.
