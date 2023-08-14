### Architecture of UNIX/LINUX

- The architecture of Linux can be divided into 3 levels of functionality. They are 1. kernel 2. Shell 3. utilities

The lowest level is **Kernel**, It schedules tasks, manages resources, and controls security.

The next level is **Shell** , It acts as the user interface, Interpreting user commands and starting applications.

The Highest level is **Utilities**, which provides utility functions. In other words, It is the user level, as user is the one who operates the utilities

![image](https://user-images.githubusercontent.com/89054489/227128032-4461e522-0b47-47c2-b9b4-9a1a112d20c6.png)

## Linux FileSystem Hierarchy

- Linux uses single rooted, inverted tree like file system hierarchy

| Name/value | Description |
| --- | --- |
|/ | This is top level directory <br> It is parent directory for all other directories <br>It is called as root directory <br> It is represented by forward slash (/) <br> c:\ of windows |
|/root | It is home directory for root user (super user)<br> It provides working environment for root user <br> c:\Documents and settings\Administrator |
|/home | It is the home directory for other users <br> it provides working environment for other users (other than root) <br>c:\Documents and Settings\username |
|/boot | It contains bootable files for linux <br> like GRUB(grand unified boot loader), boot,initrd (INITial Ram Disk) |
|/etc | It contains all configuration files <br> like - /etc/passwd.. user info<br>- /etc/resolv.conf prefered DNS <br> c:\Windows\system32\drivers\ |
|/usr | By default all the softwares are installed in /usr directory. <br> usr - Unix Sharable Resources <br> c:\program files |
|/opt | It is an optional directory for /usr <br> It contains third party softwares <br> c:\program files |
|/bin | it contains commands used by all users (binary files ) |
|/sbin | It contains commands used by only super user (root) (super user's binary files)|
|/dev | It contains device files <br> like /dev/hda --for hard disk <br> /dev/cd rom --for cd rom <br> simmilar to device manager of windows |
|/proc | It contains process files <br> It's contents are dynamic meaning keep on changing <br> it is also called as Virtual Directory <br> Its file contain useful information used by OS like /proc/meminfo -- information of RAM <br> /proc/cpuinfo -- information of CPU |
|/var | It contains variable data like mails, log files |
|/mnt | It is default mount point for any partition <br> It is empty by default |
|/media | It contains all of removable files like CD-ROM, pen drive |
|/lib | It contains library files which are used by OS <br> It is simmilar to dll files files of windows <br> library files in linux are SO (shared object ) files |

Boot, Reboot and shutdown a system :

`shutdown -h now ` To shutdown a system

`shutdown -r now` To reboot a system

**Boot or change system into different operating modes**

Boot sequence :
- POST (PowerOn self Test ) -> find disk -> Inside disk there's bootloader -> boot loader load kernel -> kernel load init process

- sysstemd is the default init process in centos

- Systemd starts services. Last service started will be a shell

systemd

- Previous versions of Red Hat Enterprise Linux, which were distributed with sysV init or Upstart, implemented a predefined set of runlevels that represented specific modes of operation. These runlevels were numbered from 0 to 6 and were defined by a selection of system services to be run when a particular runlevel was enabled by the system adminstrator. In CentOs and Red Hat Enterprise Linux 7, the concept of run levels has been replaced with **systemd targets**

- systemd targets are represented by target units. Target Units end with .target file extension and their only purpose is to group together other systemd units through a chanin of dependencies.

- systemd units are the objects that systemd knows how to manage. These are basically a standardized representation of system resources that can be managed by the suit of daemons and manipulated by the provided utilities.

- systemd units in someways can be said to simmilar to services or jobs in other init systems. However, a unit has a much broader definition, as these can be used to abstract services, network resources, devices, filesystem mounts, and isolated resource pools.

- systemd was designed to allow for better handling of dependencies and have the ability to handle more work in parallel at system startup.

systemd commands :

|command | Description |
| --- | --- |
| `systemctl get-default` |It shows default target |
|`systemctl list-units --type target -all`| It shows all available targets |
|`systemctl set-default multi-user.target`| set multi-user target as default |

change target at boot timne

- if during boot ESC is pressed the grub2 prompt will be showed
- Highlight a voice and press 'e'
- Now it is posssible to modify the boot parameter used to load the kernel.

NOTE : the changes are not persistant

Ex: `systemd.unit=emergency.target` can be added to boot system in emergency mode. 
Note: In this modality disk is mounted read only. to mount it read/write, after reboot eecute `mount -o remount,rw /`
- when parameter change is end, press 'ctrl+x' to boot system.

**Install , configure and troubleshoot bootloaders **

**Diagnose and manage processes **

**Background processes**

**process priority**

signals

**locate and analyze log files **

**Schedule tasks to run at a set date and time **

cron syntax :

**verify completion of scheduled jobs **

**Update software to provide required functionality and security **


**Verify the integrity and availability of resources and key processes**

**Change kernel runtime parameters, persistent and non-persistent**

**Use scripting to automate system maintenance tasks**

Manage the startup process and services (In Services Configuration)

List and identify SELinux/AppArmor file and process contexts

Manage Software

Identify the component of a Linux distribution that a file belongs to



