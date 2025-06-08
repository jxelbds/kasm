# install Kasm Workspaces on your server
**What is Kasm?**

Kasm is an open-source, web-based virtual desktop infrastructure (VDI) platform that allows users to access remote desktops and applications from any device with a web browser. It provides features such as multi-user support, secure connections, and easy management of desktop environments. With Kasm, administrators can create and manage multiple virtual desktops, assign users to specific desktops, and monitor user activity in real-time.

One way to run Kasm is by installing it on top of Proxmox, a popular Linux-based virtualization platform 
Kasm.docx
. Proxmox offers a robust set of features for managing virtual machines (VMs), including high availability, live migration, and storage management. By combining Kasm with Proxmox, administrators can create a comprehensive VDI solution that meets the needs of large-scale organizations.

However, when installing Kasm on top of Proxmox, there is one important consideration: you will need to set the system type to 'host' during installation [2]. This allows Kasm to utilize the underlying hardware resources provided by Proxmox, enabling it to run as a standalone application rather than as a traditional VM.

Setting the system type to 'host' during installation will also allow Kasm to take advantage of Proxmox's advanced features, such as live migration and high availability. This means that you can easily move desktops between nodes in your Proxmox cluster, or even create redundant systems to ensure continuity in case of hardware failures.

By combining the strengths of both Kasm and Proxmox, administrators can build a robust and scalable VDI solution that meets the needs of demanding users and organizations. Whether you're looking to deploy virtual desktops for remote workers, or need a highly available platform for critical applications, Kasm on Proxmox is an excellent choice.

Kasm Workspaces also provides additional features such as:

Web-native Access: Users can access their workspaces from any device with a web browser, eliminating the need for client software.
Containerization: Each workspace runs in an isolated container, enhancing security and simplifying management.
Desktop as a Service (DaaS): Kasm enables the delivery of virtual desktops on demand, supporting Windows and Linux environments.
Application Streaming: Individual applications can be streamed to users' browsers, providing access to specific tools without a full desktop environment.
These features make Kasm an excellent choice for organizations looking to deploy remote workspaces that are easy to manage, secure, and scalable.



***Hardware Requirements:***
```bash
-CPU Architecture: Amd64 or Arm64
-CPU Cores: min. 2 Cores
-RAM: mind. 4GB
-Storage: min. 50GB
```

-You can install Kasm on an Raspberry Pi but i dont recommend it!




-**How to install Kasm:**
-install Linux Operating System:
```bash
-Ubuntu 20.04 / 22.04 / 24.04 (amd64/arm64)
-Debian 11 / 12 (amd64/arm64)
-Oracle Linux 8 / 9 (amd64/arm64)
-Red Hat Enterprise Linux 8 / 9 (amd64/arm64)
-Raspberry Pi OS (Debian) 11 / 12 (arm64)
-AlmaLinux 8 / 9 (amd64/arm64)
-Rocky Linux 8 / 9 (amd64/arm64)
```
-update the Server (example: Ubuntu Server 24.04):
```bash
  sudo apt update && sudo apt upgrade -y
```

-install Kasm:

  
```bash
sudo cd /tmp
curl -O https://kasm-static-content.s3.amazonaws.com/kasm_release_1.16.1.98d6fa.tar.gz
tar -xf kasm_release_1.16.1.98d6fa.tar.gz
sudo bash kasm_release/install.sh
```

-go in your browser and go on:

  ```bash
  https://IP-ADDRESS/
```

-log in with the credentials that are in the terminal

-enjoy Kasm Workspaces and stay Safe
