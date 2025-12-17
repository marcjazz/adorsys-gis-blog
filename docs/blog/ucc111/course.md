# Course Information Sheet

## UCC111-2: Linux Installation and Package Management
This course is part of the Teaching Unit (TU): UCC111 - Linux Foundational (LPIC-101).

### Preamble
*   **Purpose**: To provide the essential basics for installing, managing startup, and maintaining software on Linux systems, which are fundamental skills for working on servers and in cloud environments.
*   **Target audience**: Students in the Professional Bachelor's Degree in Cloud Computing (Semester 1).
*   **Type of access**: Paid (UoM Standard).
*   **Hours**: 12
*   **Teaching mode**: CS (Synchronous Chat), CA (Asynchronous Chat) (UdM Standard).

### Teaching team
*   **Teaching supervisor**: Teaching team:

### Institution
This course is offered at the UNIVERSITY OF THE MOUNTAINS (UdM), within the INSTITUTE OF SCIENCE AND TECHNOLOGY (ISST).

### Prerequisites
None

### Summary
This course covers the key concepts necessary for setting up a functional Linux system. It addresses storage preparation (disk design), boot system installation, and, above all, effective management of software packages and libraries for the main Linux distribution families (Debian/RPM).

# Glossary

*   **Linux distribution**: A coherent set consisting of the Linux kernel, a package manager, and a set of tools and applications (e.g., Ubuntu, Debian, Fedora).
*   **Kernel**: The core of the operating system that manages hardware resources, processes, memory, and peripherals.
*   **CLI (Command Line Interface)**: Command line interface, used to administer the system without a graphical interface.
*   **ISO**: Installation image of an operating system containing the files necessary for installation.
*   **Bootloader**: Program loaded when the PC starts up, allowing the operating system to be launched.
*   **GRUB (GRand Unified Bootloader)**: Bootloader widely used on Linux systems, configurable and multi-OS.
*   **UEFI (Unified Extensible Firmware Interface)**: Modern replacement for BIOS, enabling advanced boot management and GPT disk support.
*   **BIOS (Basic Input/Output System)**: Legacy firmware that manages hardware initialization at startup.
*   **Dual-Boot**: Configuration allowing multiple operating systems to coexist on the same machine.
*   **MBR (Master Boot Record)**: Old partitioning scheme limited to 2 TB and 4 primary partitions.
*   **GPT (GUID Partition Table)**: Modern partitioning scheme supporting large disks and an unlimited number of partitions.
*   **Partition**: Logical division of a disk used to store systems or data.
*   **Swap**: Disk space used as an extension of RAM.
*   **Mount point**: Directory in which a partition or external disk is integrated into the Linux tree structure.
*   **fstab**: File containing the configuration of file systems to be mounted automatically.
*   **Shared library (.so)**: File containing code that can be reused by several programs simultaneously, avoiding duplication.
*   **ldconfig**: Command that updates the shared library cache.
*   **ld.so.conf**: File listing the paths containing dynamic libraries.
*   **Dependency**: A package or file required for another program to function properly.
*   **Package**: File containing a program, its data, and metadata, managed via a manager.
*   **dpkg**: Low-level package manager on Debian/Ubuntu that allows you to install or remove .deb files.
*   **apt (Advanced Package Tool)**: High-level manager that automatically resolves dependencies and manages repositories.
*   **Repository**: Server containing software packages accessible via APT.
*   **sources.list**: File containing the list of repositories used by APT.
*   **RPM (Red Hat Package Manager)**: Package format and low-level manager used on RHEL, CentOS, Fedora.
*   **YUM (Yellowdog Updater Modified)**: Former high-level manager for RPM systems allowing automatic installation of dependencies.
*   **DNF (Dandified Yum)**: A modern replacement for YUM, faster and more reliable.
*   **Package group**: A set of related software programs that can be installed together (e.g., web server, graphical environment).
*   **Log**: File containing system events and actions, useful for diagnosing errors.
*   **Broken package**: A package that is partially installed or contains unmet dependencies.
*   **Package manager lock**: Situation where another process (e.g., automatic update) prevents the installation of new packages.
*   **APT/YUM cache**: Folder containing metadata and previously downloaded packages.
*   **Checksum (SHA256)**: Fingerprint used to verify the integrity of a downloaded ISO image.
*   **GPG (GNU Privacy Guard)**: Encryption tool used to verify the authenticity of repositories and packages.
*   **lsblk / fdisk / parted**: Commands for inspecting and managing disks and partitions.
*   **mount / umount**: Commands used to mount or unmount a file system.
*   **systemctl**: Command for managing services, useful for checking whether an installed service is working correctly.

# Learning objectives

By the end of this course, students should be able to:

1.  **Master the installation of a Linux system**
    *   Prepare installation media (ISO, bootable USB drive).
    *   Choose and configure an appropriate partitioning scheme (MBR/GPT).
    *   Understand and apply the file system hierarchy
2.  **Configure and manage system startup**
    *   Understand the role of the bootloader (GRUB).
    *   Install, repair, and customize GRUB.
    *   Manage multi-boot environments.
3.  **Manage system libraries and dependencies.**
    *   Identify shared libraries (.so).
    *   Manipulate the library cache via ldconfig.
    *   Resolve issues related to missing dependencies.
4.  **Install, update, and remove packages.**
    *   Use low-level tools (dpkg, rpm).
    *   Master high-level managers (apt, yum/dnf).
    *   Configure software repositories and manage GPG keys.
5.  **Diagnose and maintain a functional Linux system.**
    *   Detect and repair broken packages.
    *   Read the logs related to package installation.

# Learning materials
Types of resources available: audio, video, source files (Word, PDF, PPT, links), Google Meet.

# Assessment
Teaching strategies adopted:
The specific assessment method is: Continuous assessment, Practical work, Final exam.

Standard school protocol:
- Continuous assessment (CC) accounts for 30% of the overall mark, broken down as follows: (Participation in tutorials 20%, Completion of activities 20%, Attendance/presence in class 20%, Completion of practical work 40%)
- The written exam accounts for 70%.

# Course outline (detailed content)

## CHAPTER 1 - Introduction to Linux installation
### 1.1. Understanding Linux distributions
*   Definition of a distribution
*   Differences between distributions (Debian, Ubuntu, RHEL, CentOS, Fedora, etc.)
*   Package management models according to families
### 1.2. Life cycle of a Linux system
*   Installation
*   Configuration
*   Maintenance
*   Updates and upgrades
### 1.3. Preparing for installation
*   Choosing a distribution based on context
*   ISO download and integrity check (SHA256, GPG)
*   Creating bootable media (Rufus, Balena, dd)

## CHAPTER 2 — Disk design and organization
### 2.1. Partitioning types
*   MBR vs. GPT
*   Comparison and limitations
*   Primary, extended, and logical partition tables
### 2.2. Partition types
*   System partition
*   Swap partition
*   /home partition
*   /boot partition
*   EFI partition (ESP)
### 2.3. Linux file systems
*   Ext2, Ext3, Ext4
*   XFS, Btrfs
*   FAT32, NTFS (compatibility)
### 2.4. Mount points
*   Role of the mount point
*   File system hierarchy (FHS)
*   Automatic mounting: /etc/fstab
*   Mount options (rw, ro, noexec, etc.)

## CHAPTER 3 - Installation and management of bootloaders
### 3.1. How a bootloader works
*   Definition and role
*   BIOS/UEFI interaction
*   Linux boot chain
### 3.2. GRUB2 - Installation and configuration
*   GRUB structure: grub.cfg, scripts
*   Menu customization
*   Modifying boot options
*   Recovery modes
### 3.3. Bootloader troubleshooting
*   Reinstalling GRUB
*   Handling common errors (error 15, no such device, etc.)
*   Backup and restore
### 3.4. Special case: Multi-boot
*   Dual-boot with Windows
*   Automatic detection via os-prober
*   Boot order

## CHAPTER 4 — Shared Library Management
### 4.1. Understanding shared libraries
*   .so files
*   Dynamic links
*   Application dependencies
### 4.2. Library identification and configuration
*   The `ldd` command
*   Configuration file /etc/ld.so.conf
*   Standard library directories
### 4.3. Library cache management
*   ldconfig function
*   Creating symbolic links
*   Cache update

## CHAPTER 5 — Package management in Debian and derivative distributions
### 5.1. Basic package management with dpkg
*   Local installation of a .deb
*   Removal and purging
*   Inspection with dpkg -l, -s, -c
### 5.2. Advanced package management
*   Manipulation of configuration files
*   Status and partial installation of packages
*   Troubleshooting incomplete installations
### 5.3. Managing repositories with APT
*   /etc/apt/sources.list
*   Adding repositories and GPG keys
*   Updating lists: apt update
### 5.4. Common operations with APT
*   Installation, upgrade, removal
*   Search and diagnostics
*   Major upgrade (dist-upgrade, full-upgrade)
### 5.5. Meta package management
*   Tasksel
*   Functional groups

## CHAPTER 6 - Package management in RedHat, Fedora, and derivatives
### 6.1. Basic management with RPM
*   Installing an .rpm
*   Signature verification
*   Querying RPM packages
### 6.2. Using YUM/DNF
*   Manager architecture: repositories, cache, metadata
*   Essential commands: installation, removal, update
### 6.3. Advanced management
*   Package groups
*   Cache cleanup
*   Conflict and broken dependency management
### 6.4. Repository configuration
*   Creating a local repository
*   Adding an external repository
*   Temporary activation/deactivation

## CHAPTER 7 - System maintenance and diagnostics
### 7.1. Updating the system
*   Security
*   Critical patches
*   Automatic Updates (cron, systemd timers)
### 7.2. Diagnosing package-related problems
*   Missing dependencies
*   Broken packages
*   Packet manager locking
### 7.3. Logging and logs
*   dpkg.log
*   yum.log / dnf.log
*   journalctl for issues related to installed services

## CHAPTER 8 - Practical exercises
*   8.1. Lab 1: Complete installation of Linux on a VM
*   8.2. Lab 2: Manual MBR and GPT partitioning
*   8.3. TP 3: Installation and configuration of GRUB
*   8.4. TP 4: Installing packages on Debian and RedHat
*   8.5. TP 5: Creating a local repository (Debian or RPM)

# Activities
*   Learning activity (tutorials), Assessment activity (tutorials + corrected assignments), Self-assessment activity (self-assessment test or multiple-choice questions), Summative activity (problem situation).

# Bibliographies and list of links
*   Provide a list of resources for further study of the course content. (UdM standard)
---
marp: true
theme: gaya
size: 16:9
paginate: true
header: 'UCC111-2: Disk Design and Organization'
footer: 'Simplified Introduction'
---

<style>
/* Global styles for a dark theme */
section {
  background-color: #202124;
  color: #e8eaed;
}
h1, h2, h3, h4, h5, h6 {
  color: #e8eaed;
}
a {
  color: #8ab4f8;
}
/* Adjust lead class for dark theme */
section.lead {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
}
</style>

<!-- _class: lead -->

# **Disk Design and Organization**
## The Foundation of Linux

Understanding how to arrange your storage.

---

## What is Disk Organization?

Imagine your computer's hard drive is a big, empty library.

-   **Disk Organization** is how you decide to divide that library into rooms (partitions) and how you store books (files) inside those rooms using different shelving systems (filesystems).

Why is this important? It helps your computer:
-   Store different types of information separately.
-   Run multiple operating systems.
-   Work efficiently.

---

## Partitions: Dividing Your Disk

A **partition** is like a separate room in your library. You carve up the entire hard drive into smaller, manageable sections.

### **Why Partition?**
-   **Organization:** Keep your system files separate from your personal files.
-   **Security/Stability:** If one partition gets corrupted, others might be safe.
-   **Multi-Boot:** Install Windows and Linux on the same computer.

---

## MBR vs. GPT: The Blueprint

These are two different ways to draw the "floor plan" for your partitions.

-   **MBR (Master Boot Record):**
    -   **Older:** Like an old-school blueprint.
    -   **Limits:** Only works well for disks up to 2TB. Can only have 4 main sections (primary partitions).

-   **GPT (GUID Partition Table):**
    -   **Modern:** The new, flexible blueprint.
    -   **No Limits:** Works with very large disks (terabytes and beyond). Can have many, many sections (partitions).
    -   **Needed for UEFI:** Most new computers use GPT with a modern startup system called UEFI.

---

## Partition Types (MBR Specific)

If using MBR, you have specific types of "rooms":

-   **Primary Partitions:** The main rooms. You can have up to 4.
-   **Extended Partition:** A special type of primary partition that acts like a hallway. You can only have one.
-   **Logical Partitions:** Smaller rooms *inside* the extended partition. You can have many of these.

*(GPT doesn't use "extended" or "logical" – it's simpler, almost all partitions are "primary" in concept)*

---

## Common Linux Partitions

On a Linux system, we often set up specific partitions for different purposes:

-   **`/` (Root Partition):**
    -   **The Main Brain:** This is where the operating system itself lives (all your Linux core files).
    -   Every other directory is under `/`.

-   **`/boot` Partition:**
    -   **The Starting Blocks:** Contains the Linux kernel and files needed to start your computer.
    -   Often kept separate, especially when using advanced storage like LVM.

---

## Common Linux Partitions (Continued)

-   **`swap` Partition:**
    -   **RAM's Backup:** Used by the system when your computer runs out of physical RAM. It's like a temporary overflow area on your hard drive.

-   **`/home` Partition:**
    -   **Your Personal Space:** This is where all your user accounts store their files, documents, pictures, etc.
    -   Good to keep separate, so you can reinstall the operating system without losing your personal data.

-   **EFI System Partition (ESP):**
    -   **For Modern Boots:** If your computer uses UEFI (and most new ones do), this small partition stores files needed by the UEFI firmware to boot the operating system.

---

## Filesystems: How Data is Stored

A **filesystem** is the method your computer uses to organize and manage files on a partition. It's like the shelving system *inside* your library rooms.

-   **What it Does:** Keeps track of where files begin and end, their size, who owns them, etc.

### **Common Linux Filesystems:**
-   **Ext4:** (Extended Filesystem 4)
    -   **The Popular Choice:** The most common and recommended filesystem for Linux today. It's reliable and efficient.
-   **XFS, Btrfs:**
    -   **For Big Jobs:** More advanced filesystems, often used in servers for better performance, data integrity, or special features (like snapshots).

---

## Filesystems: Compatibility

-   **Talking to Windows:**
    -   **FAT32, NTFS:** Filesystems mainly used by Windows. Linux can usually read and write to these, which is handy for sharing files.

---

## Mount Points: Connecting Everything

A **mount point** is an empty directory where a partition (or another storage device) is "attached" and made accessible to the system.

-   **Analogy:** You build a room (partition) in your library, but it's empty. A mount point is like putting a door on that room and giving it a name (e.g., `/home`). Now, when you go through the `/home` door, you enter that specific partition.

-   **`/etc/fstab`:** This special file tells your Linux system which partitions to automatically attach (mount) to which directories (mount points) every time the computer starts.

---

<!-- _class: lead -->

## Summary: Key Takeaways

-   **Disks are Divided:** Hard drives are split into **partitions**.
-   **MBR vs. GPT:** Old vs. new ways to manage partitions.
-   **Linux Uses Specific Partitions:** (`/`, `/boot`, `swap`, `/home`, EFI).
-   **Filesystems Organize Data:** (`Ext4` is common, `XFS/Btrfs` are advanced).
-   **Mount Points Connect:** Partitions are made accessible via **mount points**, configured automatically with `/etc/fstab`.

---

<!-- _class: lead -->

# **Understanding the Foundation**
## Empowers Your Linux Journey
### **Lab 1: The Phoenix Server - From Ashes to Automation**

**Scenario:**

Welcome back, specialists. A critical, minimalist web server has suffered a catastrophic failure. The only thing that remains is the client's requirement: a fast, secure, and minimal Debian system. Your task is to rebuild it from the ground up. This isn't just about getting a system running; it's about building it with intention, precision, and an understanding of the components, just like you would in a real-world data center. We will use the Debian `netinst` (network install) image, which is small and requires you to pull packages from the network, forcing a deliberate choice of what goes into our system.

**Prerequisites:**

*   A hypervisor (VirtualBox, KVM/QEMU, VMware) installed.
*   [Debian 12 Network Install ISO](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-12.5.0-amd64-netinst.iso) downloaded.

**Core Concepts Refresher:**

Your LPIC-101/102 knowledge is sound, but a year is a long time. Refresh your memory on:

*   **Logical Volume Management (LVM):** Why it's superior to standard partitions for server environments (flexibility, snapshots).
*   **debootstrap:** A tool to install a basic Debian system into a subdirectory of another, already-installed system.
*   **chroot:** (change root) A way to run commands and an interactive shell within a different root directory. Essential for system recovery and custom builds.

---

### **Level 1: The Foundation (Standard Complexity)**

**Goal:** Build a minimal, functional Debian server using the expert guided installer and LVM for a flexible disk layout.

**Instructions:**

1.  **VM Creation:**
    *   Create a new VM. Name it `phoenix-server`.
    *   Assign it: 2 vCPUs, 2048 MB RAM, and a new 20 GB virtual disk.
    *   Mount the Debian `netinst` ISO and boot the VM.

2.  **Expert Installation:**
    *   From the boot menu, select **Advanced options > Expert install**. This mode exposes every step of the installation process. Proceed through the initial steps (language, location, keyboard).

3.  **Partitioning with LVM (The Core Task):**
    *   When you reach the partitioning step, choose **Manual**.
    *   Create a new partition table on your virtual disk.
    *   Create a small 512MB primary partition at the beginning of the disk. Set its "Use as" type to **Ext4** and its mount point to `/boot`.
    *   Create a second, larger primary partition using the remaining space. Set its "Use as" type to **physical volume for LVM**.
    *   Now, navigate to the "Configure the Logical Volume Manager" menu.
    *   Create a **Volume Group** (VG) named `vg_phoenix`.
    *   Inside `vg_phoenix`, create three **Logical Volumes** (LVs):
        *   `lv_root`: 10 GB, to be used for the root filesystem (`/`).
        *   `lv_home`: 5 GB, to be used for user data (`/home`).
        *   `lv_swap`: 2 GB, to be used for swap space.
    *   Finish the LVM configuration and assign each LV its filesystem type (Ext4 for root/home, swap for swap) and mount point.

4.  **Minimal Package Installation:**
    *   Proceed with the base system installation.
    *   When you reach "Software selection," **deselect everything**, especially the "Debian desktop environment."
    *   The only two options that should be checked are:
        *   **SSH server**
        *   **standard system utilities**
    *   This ensures our server is lean and has no unnecessary graphical components.

5.  **Finalize and Verify:**
    *   Install the GRUB bootloader to the primary drive (e.g., `/dev/vda`).
    *   Finish the installation and reboot. The system will boot to a command-line interface.
    *   From your host machine's terminal, SSH into the new server (`ssh user@<vm_ip_address>`).
    *   **Verification Commands:** Run the following to confirm your setup. What does each one tell you?
        *   `lsblk` (Should show your LVM layout)
        *   `df -h` (Should show your filesystems mounted)
        *   `free -m` (Should show your swap space is active)
        *   `dpkg --get-selections | wc -l` (How many packages are installed? A minimal system is a happy system.)

---

### **Level 2: The Optimization (Advanced Complexity)**

**Goal:** Harden the base installation, automate package deployment, and prepare it for a "production" role.

**Instructions:**

1.  **SSH Hardening:**
    *   Modify `/etc/ssh/sshd_config` on `phoenix-server` to enhance security.
        *   Disable root login (`PermitRootLogin no`).
        *   Disable password-based authentication (`PasswordAuthentication no`).
    *   On your host machine, generate an SSH key (`ssh-keygen`) if you don't have one, and copy the public key to the server (`ssh-copy-id user@<vm_ip_address>`).
    *   Restart the SSH service (`systemctl restart sshd`) and verify you can still log in (it should now be passwordless).

2.  **Firewall Configuration:**
    *   Install the Uncomplicated Firewall: `apt install ufw`.
    *   Configure it to deny all incoming traffic by default.
    *   Explicitly allow SSH traffic. What port does SSH use?
    *   Enable the firewall. Verify its status.

3.  **Create a Personal Package Repository:**
    *   On the server, install `nginx`: `apt install nginx`.
    *   Create a simple dummy Debian package. You don't need to write code; the goal is to create the package structure.
        ```bash
        # Install packaging tools
        sudo apt install build-essential devscripts debhelper
        # Create a project
        mkdir ~/dummy-pkg-1.0 && cd ~/dummy-pkg-1.0
        dh_make --native -s -y
        # Build the package (ignore warnings)
        debuild -us -uc
        ```
    *   You will find a `.deb` file in the parent directory.
    *   Create a directory in the `nginx` web root (`/var/www/html/debian`) and copy your `.deb` file there.
    *   Configure `nginx` to serve this directory.
    *   On the server itself, add your own `nginx` server as an APT repository in `/etc/apt/sources.list`.
    *   Run `apt update` and then install your `dummy-pkg`.

---

### **Level 3: The Recovery & Deep Dive (Expert Complexity)**

**Goal:** Simulate a catastrophic failure and rebuild the system without the installer, using only command-line tools. This is the ultimate test of system understanding.

**Instructions:**

1.  **Simulated Disaster: GRUB is Gone!**
    *   On your working `phoenix-server` from Level 1, simulate a bootloader overwrite:
        `sudo dd if=/dev/zero of=/dev/vda bs=446 count=1`
    *   Reboot the VM. It will fail to boot, likely with a "No bootable medium" error. The server is dead. Or is it?

2.  **Manual System Rescue:**
    *   Boot the VM using the Debian `netinst` ISO again.
    *   From the main menu, select **Advanced options > Rescue mode**.
    *   The rescue environment will try to find your existing installation. Let it guide you to mount your LVM `root` partition under `/target`. If it fails, you must do it manually using the provided shell.
    *   The key step: **`chroot /target`**. You are now inside your broken system, with the tools from the live CD.
    *   **Your task:** From within the chroot, fix the system. What commands do you need to run?
        *   You'll need to mount `/boot`.
        *   You'll need to reinstall GRUB. (Hint: `grub-install /dev/vda`)
        *   You might need to update GRUB's configuration.
    *   Exit the `chroot`, reboot without the ISO, and watch your server rise from the ashes.

3.  **The `debootstrap` Challenge:**
    *   If you complete the rescue, the final challenge awaits. Destroy your VM and create a new one.
    *   This time, do not use the installer at all. Boot into Rescue Mode from the start.
    *   From the command line, perform a full manual installation:
        1.  Partition the disk (`parted` or `fdisk`).
        2.  Create the LVM structure (`pvcreate`, `vgcreate`, `lvcreate`).
        3.  Format the filesystems (`mkfs.ext4`, `mkswap`).
        4.  Mount everything under `/mnt` (e.g., root on `/mnt`, boot on `/mnt/boot`).
        5.  Use **`debootstrap`** to install the Debian 'bookworm' release into `/mnt`.
        6.  `chroot` into `/mnt` and manually install a kernel (`apt install linux-image-amd64`), GRUB (`apt install grub-pc`), configure `/etc/fstab`, set a root password (`passwd`), and create a user.
    *   If you can successfully boot this manually-built system, you have demonstrated a true mastery of the Linux installation process.
---
marp: true
theme: gaya
size: 16:9
paginate: true
header: 'UCC111-2: Linux Installation and Package Management'
footer: 'Lab 1: The Phoenix Server'
---

<style>
/* Global styles for a dark theme */
section {
  background-color: #202124;
  color: #e8eaed;
}
h1, h2, h3, h4, h5, h6 {
  color: #e8eaed;
}
a {
  color: #8ab4f8;
}
/* Adjust lead class for dark theme */
section.lead {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
}
</style>

<!-- _class: lead -->

# **Lab 1: Mission Briefing**
## The Phoenix Server: From Ashes to Automation

**Your mission, should you choose it...**

<!--
notes:
- Welcome everyone.
- Today, we're moving beyond basic theory. You all have the foundational knowledge from your LPIC certifications.
- Our goal today is to apply that knowledge under pressure and learn to build a server with the precision of a true sysadmin.
-->

---

## Your Mission: Build with Intention

Your goal is not just to "install Linux," but to construct a server with **precision, efficiency, and control.**

- **Scenario:** You will be rebuilding a critical server from scratch.
- **Method:** You will use the Debian `netinst` image for a minimal base.
- **Philosophy:** Every package and every configuration choice must be deliberate.

---

## Key Concepts You Will Master

1.  **Logical Volume Management (LVM)**
2.  **Post-Installation Hardening**
3.  **The `chroot` Environment**
4.  **Disaster Recovery (GRUB)**
5.  **`debootstrap` for Manual Installation**

<!--
notes:
- We're going to touch on five key areas today.
- Some of this will be a refresher, but we'll be going deeper than standard textbook examples.
- We'll start with the foundation: the filesystem layout.
-->

---

## 1. Logical Volume Management (LVM)

LVM adds a flexible abstraction layer between your physical disks and your filesystems. It is the **industry standard** for servers.

<style>
.lvm-diagram { display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 5px; font-family: monospace; }
.lvm-box { border: 2px solid #999; padding: 10px; text-align: center; border-radius: 5px; color: #e8eaed; }
.vg-pool { border: 2px dashed #999; padding: 10px; margin-top: 5px; }
.lv-pool { display: flex; gap: 10px; }
</style>

<div class="lvm-diagram">
  <div class="lvm-box" style="background-color: #4a2d2d;">/dev/vda2 (Physical Disk Partition)</div>
  &darr;
  <div class="lvm-box" style="background-color: #2d3a4a;">Physical Volume (PV)</div>
  &darr;
  <div class="vg-pool">
    <strong>Volume Group (VG) - "vg_phoenix" (A Pool of Storage)</strong>
    <div class="lv-pool">
      <div class="lvm-box" style="background-color: #2d4a3a;">LV: root</div>
      <div class="lvm-box" style="background-color: #2d4a3a;">LV: home</div>
      <div class="lvm-box" style="background-color: #2d4a3a;">LV: swap</div>
    </div>
  </div>
</div>

<!--
notes:
- Think of it like this: You give raw disk space to LVM to create a "Physical Volume".
- You then pool one or more PVs into a "Volume Group", which is just a big bucket of storage.
- From that bucket, you can carve out "Logical Volumes" of any size you want. These are your actual partitions.
- The magic is that you can resize these LVs later without having to repartition the physical disk.
-->
---

## LVM in Lab 1: Your Target Layout

This is the professional disk layout you will build. Note the separation of `/boot`.

<!-- _class: spot -->
```
/dev/vda
  ├─ /dev/vda1  (512M, ext4, mounted on /boot)
  └─ /dev/vda2  (19.5G, LVM Physical Volume)
      └─ vg_phoenix (Volume Group)
          ├─ lv_root (10G, ext4, mounted on /)
          ├─ lv_home (5G, ext4, mounted on /home)
          └─ lv_swap (2G, swap)
```

**Why is `/boot` separate?** The bootloader (GRUB) runs very early in the boot process. It needs to read the kernel and initramfs directly from a simple, standard filesystem. It doesn't understand LVM, so `/boot` must be outside of it.

---

## 2. Post-Installation Hardening

A fresh install is a vulnerable install. In Level 2, you will be challenged to harden the server:

- **SSH Hardening:** You will disable direct root login and enforce the use of secure SSH keys.

- **Firewall (`ufw`):** You will implement a "default-deny" policy and explicitly allow only the services you need.

- **Custom APT Repository:** You will practice deploying your own software by creating a local package repository with `nginx`.

---

## The Professional's Superpower:
# `chroot`

---

## The `chroot` Environment

`chroot` (Change Root) creates a temporary "bubble." When you `chroot` into a directory, that directory becomes the `/` root for all commands you run.

**Why this is a superpower:**
- **System Recovery:** You can boot from a live CD, `chroot` into your broken system, and run commands to fix it *as if you were actually logged in*. You can reinstall kernels, fix configs, and manage packages.
- **Custom Builds:** You can install a new system into a folder (`debootstrap`), `chroot` in, and configure it before it ever boots for the first time.

---

## 4. Your Mission: Disaster & Recovery

In the lab, you will intentionally break your server by wiping the bootloader, then bring it back to life.

**Your recovery mission will be:**

1.  **Boot** from a Live ISO (the `netinst` CD).
2.  **Mount** the broken system's partitions into a temporary location.
3.  **`chroot`** into the mounted root filesystem.
4.  **Re-install GRUB** using `grub-install`.
5.  **Reboot** the resurrected server.

This is a fundamental, resume-worthy skill.

---

## The Expert Challenge:
# `debootstrap`

---

## 5. The `debootstrap` Challenge

For those who finish early, `debootstrap` is the ultimate tool for control. It allows you to install a complete Debian base system into a directory **without needing an installer.**

**You will be challenged to:**
1. Manually partition disks from a live CD.
2. Mount them to a temporary directory.
3. Run `debootstrap` to create the system files.
4. `chroot` into the new system to install a kernel and configure it from scratch.

This is how custom Linux images and many automated deployments are born.

---

<!-- _class: lead -->

## Mission Briefing Complete.

**Focus. Be precise. Learn from failure.**

**Good luck.**
