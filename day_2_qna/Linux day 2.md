**Que - 1: What is squashfs file system?**

When creating tiny-sized and embedded Linux systems, every byte of the storage device (floppy, flash disk, etc.) is very important, so compression is used everywhere possible. Also, compressed file systems are frequently needed for archiving purposes. For huge public archives, as well as for personal media archives, this is essential. It is a read-only file system that lets you compress whole file systems or single directories, write them to other devices/partitions or to ordinary files, and then mount them directly (if a device) or using a loopback device (if it is a file).

**Que - 2: What are /dev/loop and /dev/tty?** 

/dev/tty stands for the controlling terminal (if any) for the current process (the process that uses "/dev/tty" in a command). To find out which tty's are attached to which processes use the "ps -a" command at the shell prompt (command line).

**Que -3 What are Linux signals?**

A signal is a notification to a process that an event has occurred. Signals are sometimes described as software interrupts, because in most cases, they interrupt the normal flow of execution of a program and their arrival is unpredictable.

**Que -4 What is the purpose of hidden files ?**

The purpose of the hidden files are to prevent it from getting deleted accidently that doesn't mean we cannot delete that.

**Que -5 How ext4 fs is faster ?**

It is faster because it supports delayed allocation that means a file which is written , the appended part is stored in the memory like cache and RAM and after a time it is written in harddisk and it is also called as writeback time.

**Que -6 What is swap and swap memory?**

Swap is hard disk space used as RAM. It is (relatively speaking) very slow, but stops computers from crashing when they are trying to deal with more data then their RAM can handle.

Swap space is a space on a hard disk that is a substitute for physical memory. ... It is also called a swap file. This interchange of data between virtual memory and real memory is called swapping and space on disk as “swap space”.  

swap memory is the dedicated amount of hard drive that is used whenever RAM runs out of memory. 

**Que -7 How to mount a file system?**

To mount a file system we can make use of this command :

mount -t Type Device MountPoint 

here mount point can be created by mkdir

**Que -8 Zfs use case ?**

It has pooled storage i.e ZFS combines the features of a file system and a volume manager. This means that unlike other file systems, ZFS can create a file system that spans across a series of drives or a pool. Not only that but you can add storage to a pool by adding another drive. 

It  has also copy on write  i.e On ZFS, the new information is written to a different block. Once the write is complete, the file systems metadata is updated to point to the new info. This ensures that if the system crashes (or something else happens) while the write is taking place, the old data will be preserved while in other system it lost forever.

 It also has data integrity verfication which means Whenever new data is written to ZFS, it creates a checksum for that data. When that data is read, the checksum is verified. If the checksum does not match, then ZFS knows that an error has been detected. ZFS will then automatically attempt to correct the error.

The main reason why people advise ZFS is the fact that ZFS offers better protection against data corruption as compared to other file systems. It has extra defences build-in that protect your data in a manner that other free file systems cannot and it provies facility to increase storage.

**Que - 9 Revisit Linux Directory Structure and each directory ?**

/ - Everything on your Linux system is located under the / directory, known as the root directory.

**/bin** : All the executable binary programs (file) required during booting, repairing, files required to run into single-user-mode, and other important, basic commands **viz.**, cat, ls

/boot : Holds important files during boot-up process , including Linux Kernel.

/dev: Contains device files for all the hardware devices on the machine.

**/etc** : all the machine specefic configuration files should be located in /etc.

**/home** : Home directory of the users. Every time a new user is created, a directory in the name of user is created within home directory which contains other directories like **Desktop**, **Downloads**, etc.

**/lib** : Binaries found in /bin and /sbin often use shared libraries located in /lib.

**/media** : Temporary mount directory is created for removable devices.

**/mnt** : Temporary mount directory for mounting file system.

**/opt** : Optional is abbreviated as opt. Contains third party application software. Viz., Java, etc.

**/proc** : A virtual and pseudo file-system which contains information about running process with a particular pid.

**/root** : This is the home directory of root user and should never be confused with /

**/sbin** : Contains binary executable programs to configure operating system , required by System Administrator , here s refers to sudo or super

**/srv** : Service is abbreviated as ‘**srv**‘. This directory contains server specific and service related files.

**/tmp** :System’s Temporary Directory, Stores temporary files for **user** and **system**, till next boot.

**/usr** :  stands for User System Resources. This directory contains most commands and executables files, libraries and documentation.

**/var**: Stands for variable. The contents of this file is expected to grow. This directory contains logs.

Que -10 How to check which process is running on which port ?

We can check using netstat -anp 

here - a is for all  and n is for numeric address and p is for process name

**Que - 11 What is the difference between sbin and usr/bin?**

sbin - This is similar to the /bin directory. The only difference is that is contains the binaries that can only be run by root or a sudo user. You can think of the ‘s’ in ‘sbin’ as super or sudo.

usr/sbin - It contains same binaries but these are user specific.

**Que -12 - What are Control groups?**

cgroups is a Linux kernel feature that limits, accounts for, and isolates the resource usage of a collection of processes. Engineers at Google started the work on this feature in 2006 under the name "process containers".

**Que- 13 Examples of awk, grep, sed ?**

*Grep* command is used for finding particular patterns in a file and to display all the fields matching that pattern. 

Suppose we want to find a word manager common in a file then we can do this by

grep -i "manager" example.txt  (here i is used as to ignore case senstivity)

likewise we can use this grep command with different options 

**Awk** command is more of scripting language used in manipulating data and generating reports. 

When using ‘awk’ we enclose patterns in curly braces. Both pattern and action form a rule and the entire awk program is enclosed in single quotes.

awk '{print}' example.txt  (here since pattern is not specified it will print all)

awk '/manager/ {print}' example.txt

it wil print containing managers.

awk ‘NR==3, NR==6 {print NR,$0}’ example.txt

  It will display from line number 3 to number 6.

**SED** is short for stream editor. It can be used to perform different functions such as searching.

sed 's/manager/operations/g' test

To replace only on a specific line, specify the file line as below where we are replacing on the third line.

sed '3 's/manager/operations/g'  test 

here we wil also use i flag to save the file 

sed -i 's/manager/operations/g' test
