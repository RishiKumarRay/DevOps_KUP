**Que-1 -> What is GNU Project ?**

The name of the GNU project is derived from the recursive acronym "GNU's Not Unix." Unix was a very popular operating system in the 80s, so Stallman designed GNU to be mostly compatible with Unix so that it would be convenient for people to migrate to GNU.

Stallman established the Free Software Foundation in October 1985 to assist administrative, legal, and organisational aspects of the GNU project and also to spread the use and knowledge of Free Software. The main licences of the GNU project are the GNU General Public License (GPL) and the GNU Lesser General Public License (LGPL, originally called GNU Library General Public License). Over the years they have become established as the most widely used licences for Free Software.

**Que -2 -> What is the difference between UNIX and Linux?**

  Linux ->

Linux is freely distributed,downloaded, and distributed through magazines also. And priced distros of Linux are also cheaper than Windows, As it is open source, it is developed by sharing and collaboration of codes by world-wide developers. Linux provides two GUIs, KDE and Gnome. But there are many other options. For example, LXDE, Xfce, Unity, Mate, and so on. also the community support in the case of linux is very strong here Threat recognition and solution is very fast because Linux is mainly community-driven. So, if any Linux client posts any sort of threat, a team of qualified developers starts working to resolve this threat.

UNIX -

Unix was developed by AT&T Labs, different commercial vendors, and non-profit organizations. It is an operating system which can be only utilized by its copywriters. Unix clients require longer hold up time, to get the best possible bug fixing patch.It also supports file system however lesser than Linux.

**Que -3 -> How to do the Integrity Check in BIOS?**

The system integrity test performed by BIOS is called POST(Power On Self Test). POST include routines performed by the firmware once the device is switched on to verify if the hardware is performing as expected otherwise return error messages and beeps. The harware checked include RAM, processors, peripheral devices etc.

**Que -4 ->  What is the difference between UEFI and BIOS?**

BIOS stands for Basic Input/Output System, It is stored on an EPROM (Erasable Programmable Read-Only Memory), allowing the manufacturer to push out updates easily. It provides many helper functions that allow reading boot sectors of attached storage and printing things on screen. 

UEFI - UEFI stands for Unified Extensible Firmware Interface. It does the same job as a BIOS, but with one basic difference: it stores all data about initialization and startup in an .efi file, instead of storing it on the firmware.

This .efi file is stored on a special partition called EFI System Partition (ESP) on the hard disk. This ESP partition also contains the bootloader.

UEFI was designed to overcome many limitations of the old BIOS, including:

1. UEFI supports drive sizes upto 9 zettabytes, whereas BIOS only supports 2.2 terabytes.

2. UEFI provides faster boot time.

3. UEFI has discrete driver support, while BIOS has drive support stored in its ROM, so updating BIOS firmware is a bit difficult.

4. UEFI offers security like "Secure Boot", which prevents the computer from booting from unauthorized/unsigned applications. This helps in preventing rootkits, but also hampers dual-booting, as it treats other OS as unsigned applications. Currently, only Windows and Ubuntu are signed OS (let me know if I am wrong).

5. UEFI runs in 32bit or 64bit mode, whereas BIOS runs in 16bit mode. So UEFI  is able to provide a GUI (navigation with mouse) as opposed to BIOS which allows navigation only using the keyboard.

    

   **Que-5 -> What are Various Linux Distributions and their uses?**

   Ubuntu - It came into existence in 2004 by Canonical and quickly became popular. Ubuntu is a next version of Debian and easy to use for newbies. It comes with a lots of pre-installed apps and easy to use repositories libraries.
   
   Debian - Debian has its existence since 1993 and releases its versions much slowly then Ubuntu and it is much more stable than ubuntu.
   
   RHEL - It is known as red hat enterprise linux and it is commercial and it always provides support since it is paid.
   
   Centos:- CentOS is a community project that uses red hat enterprise Linux code but removes all its trademark and make it freely available. In other words, it is a free version of RHEL and provide a stable platform for a long time.
   
   Fedora - It is a project that mainly focuses on free software and provides latest version of software. this project is supported by red hat

   **Que- 6-> What are various operating system and their uses?**

   The three most common operating systems for personal computers are **Microsoft Windows, macOS, and Linux**. 

   Windows is a graphical operating system developed by Microsoft. It allows users to view and store files, run the software, play games, watch videos, and provides a way to connect to the internet. Later, it was released on many versions of Windows as well as the current version, Windows 10.

   Linux is used in smart devices, Servers and Mainframes, Telecommunication, Security.

   mac OS - this  os is made by apple and easy generally known for easy to use. That's because it's designed specifically for the hardware it runs on — and vice versa. 

   **Que- 7-> What does systemd.unit(5) means?**

   1. User Commands : Commands that can be run from the shell by a normal user

   2. System Calls: Programming functions used to make calls to the Linux kernel

   3. C Library Functions: Programming functions that provide interfaces to specific programming libraries.

   4. Devices and Special Files: File system nodes that represent hardware devices or software devices.

   5. File Formats and Conventions: The structure and format of file types or specific configuration files.

   6. Games: Games available on the system

   7. Miscellaneous: Overviews of miscellaneous topics such as protocols, filesystems and so on.

   8. System administration tools and Daemons:Commands that require root or other administrative privileges to use.

   9. Ques - What Uname command?
   
      Uname Command- Uname Command is used for displaying the information about this system.
      SYNTAX- uname [option]
      OPTIONS-      
   
      1. -a: It prints all the system information in the following order: Kernel name, network node hostname, kernel release date, kernel version, machine hardware name, hardware platform, operating system
         Syntax: $uname  -a
         
      2. -s: It prints the kernel name.
         Syntax: $uname  -s
      
      3. -n: It prints the hostname of the network node (current computer).
         Syntax: $uname  -n
      
      4. -r:  It prints the kernel release date.
         Syntax: $uname  -r
      
      5. -v:  It prints the version of the current kernel.
         Syntax: $uname  -v
      
      6. -m: It prints the machine hardware name.
         Syntax: $uname  -m
      
      7. -p:  It prints the type of the processor.
         Syntax: $uname  -p
      
      8. -i:   It prints the platform of the hardware.
         Syntax: $uname  -i
      
      9. -o:  It prints the name of the operating system.
         Syntax: $uname  -o
         
         
         
         **Que- 8 > What is getty command?**
      
      getty, short for "get tty", is a Unix program running on a host computer that manages physical or virtual terminals (TTYs). When it detects a connection, it prompts for a username and runs the 'login' program to authenticate the user.
      
      
   
    **Que 9 - What are unit and install?**
   
   Units are basically the objects that systemd knows how to manage , this is the primary object that the systemd tools know how to deal with. these resources are defined using configuration files called unit files. These are basically a standardized representation of system resources that can be managed by the suite of daemons and manipulated by the provided utilities.
   
   
   
   **Que 10- Private Tmp = yes meaning ?**
   
   This means a file system namespace is set up for the process and a private /tmp directory is mounted inside it which is not shared by the other processes outside the namespace. This is useful to secure access to temporary files of the process, but makes sharing between processes via /tmp impossible.
   
   

​      **Que 11 - Forking in [service ] meaning?**

This service type is used when the service forks a child process, exiting the parent process almost immediately. This tells systemd that the process is still running even though the parent exited. So the promt returns but the process executes in background.