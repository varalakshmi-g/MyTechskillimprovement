#### List, create, delete and modify physical storage partitions

|Command | Description |
| --- | --- |
|`lsblk`| list all available disk devices plus available partitions |
|`fdisk`| it is used to manage disk partitions in MBR modality <br> ex: `fdisk /dev/sda` This will open an interactive menu that will permit to show the current status of partitions or create a new partitions |
|`gdisk` | It is used to manage disk partition in GPT modality <br> Ex: `gdisk /dev/sda`|
|`gdisk /dev/sda`-> `x`(expert)-> `z` (zap)| Destroy all MBR partition on a disk |
|`gdisk /dev/sda`-> `w` -> `y` | Convert MBT to GPT |

**what is partition ?**
- Partitioning means divide a single harddrive into many logical drives. A partition is a contiguous(sharing a common border) set of blocks on a drive that are treated as an independent disk. A partition table is an index that relates sections of the hard drive to partitions.

** why have multiple partitions ?**

- **Encapsulate data** since file system corruption is local to a partition. you stand to lose only some of your data if accident occurs.
- **Increase disk effeciency** It is the ability to store and manage data while consuming the least amount of space on disk with little to no impact on performance, resulting in a lower overall cost.
- **Limit data growth** Runaway processes or maniacal users can consume so much disk space that the operating system no longer has room on the hard drive for it's book keeping operations. This will lead to disaster. By segregating space, you ensure that things other than the operating system die when allocated disk space is exhausted.

** Disk partition criteria & structure **
- on the disk where O/S is installed , will have the first partition as **MBR**
    - **MBR** is a Master Boot Record, which contains 2 important utilities. **IPL**(initial program loader) and **PTI**(partition table information)
    - **IPL** is responsible for booting the operating system, because it contains the **boot laoder** 
    - **PTI** (partition table information) is the information about the number of partitions on the disk, sizes of the partition and types of partitions.

![image](https://user-images.githubusercontent.com/89054489/227819585-330ffdbd-c62a-4e99-b387-364e68ad58ca.png)


- Every disk can have only 3 primary partitions

- **primary partition** Is a partition which usually holds the **operating system** only one among the 3 primary partitions can be active which will be booted by **MBR** to load the Operating system

- **Extended partition** is a special type of primary partition which can be sub divided into multiple logical partitions. As there can be only 3 primary partitions per disk.And if the user is required to make further partitions then all the space remaining on the disk should be allocated to extended partition. which can be used to create the logical partitions later. There can be **only one extended partition** per disk.
- **logical partitions** are the partitions which are created under extended partition, all the space in the extended partition can be used to create any number of logical partitions.


**Disk identifications**

Different types of disks will be having different initials in linux
- IDE (Integrated drive electronics ) drive will be shown as /dev/hda
- SCSI (Small Computer System Interface) drive will be shown as /dev/sda
- virtual drive will be shown as /dev/vda



![image](https://user-images.githubusercontent.com/89054489/227813585-0c248171-6524-4bfb-a11d-3e31fcf5a486.png)

![image](https://user-images.githubusercontent.com/89054489/227813631-bff03e1b-17cb-40b6-83c6-8c29576c9de2.png)

**file system**

- It is method of storing of data in an organized fashion on the disk. Every partition on the disk except MBR and Extended partition should be assigned with some file system in order to make them store the data. File system is applied on the partition by formatting it with a particular type of file system.

- The file system supported in linux are **ext2,ext3,ext4,vfat etc**.
-**Ext** file system is widely used file system in linux, whereas vfat is the file system to maintain a common storage between **linux and windows**(In case of multiple o/s )

|S.No. | EXT2 | EXT3 | EXT4 |
| --- | --- | --- |--- |
|1 |Stands for Second Extended File System | Stands for Third Extended File System | Stands for Fouth Extended File System |
|2. | It was introduced in 1993 |It was introduced in 2001 |It was introduced in 2008. |
|3.| Does not have journaling feature.|Supports Journaling Feature.|Supports Journaling Feature.|
|4.| Maximum File size can be from 16 GB to 2 TB|Maximum File Size can be from 16 GB to 2 TB| Maximum File Size can be from 16 GB to 16 TB|
|5. |Maximum ext2 file system size can be from 2 TB to 32 TB| Maximum ext3 file system size can be from 2 TB to 32 TB| Maximum ext4 file system size is 1 EB (Exabyte). 1 EB = 1024 PB (Petabyte). 1 PB = 1024 TB (Terabyte).|
|6. | Cannot convert ext file system to ext2.|You can convert an ext2 file system to ext3 file system directly (without backup/restore).| All previous ext file systems can easily be converted into ext4 file system. You can also mount an existing ext3 f/s as ext4 f/s (without having to upgrade it).|

To learn about ubuntu file system
https://manpages.ubuntu.com/manpages/trusty/man5/filesystems.5.html

**Mounting:**
- Attaching a directory to the file system in order to access the partition and its file system is known as mounting.
- The mount point is the directory (usually an empty one) in the currently accessible file system to which a additional file system is mounted.
- The /mnt directory exists by default on all Unix-like systems. usually its subdirectories (such as /mnt/floppy and /mnt/usb) are intended specifically for use as mount points for removable media such as CDROMs, USB key drives and floppy disks.

**files which is related to mounting in linux**
- `/etc/mtab` is a file which stores the information of all the currently mounted file systems. It is dynamic and keeps changing
- `/etc/fstab` is the file which keeps information about the permanent mount point. If you want to make your mount point permanent. so that it will be mounted even after reboot, then you need to make an appropriate entry in the file.

|command | Description |
| --- | --- |
|`fdisk -l or parted -l`| To view the existing partitions|
|`fdisk <diskname>` EX: `fdisk /dev/sda` | To enter into disk utility <br> use`m` to list out various options that can be used in fdisk |
|`fdisk /dev/sda`| To Enter into disk utility <br> `n` to create new partition <br>`p` to list out the partition information <br>`d` to delete a partition and specify the device name<br>**Note:** Never delete the system partitions i.e; 1-7 <br> `w` to save the partition <br> `q` to quit the partition screen |
|`partprobe /dev/sda` <br> `partx -a /dev/sda` <br> `kpartx /dev/sda`|updating the partition table without restarting the system. |
|`mkfs.<file system type> <partition name>`<br> `mkfs.ext4/dev/sda7`(where sda7 is new partition)| formatting a partition with ext4 file system.<br> After creating a file system we need to assign some file system to it. So that we can start storing the data into it. |

##### Mounting a partition
- Mounting a procedure where we attach a directory to the file system. There are two types of mounting which will be used in linux or any UNIX
    
    - Temporary Mounting
    - Permanent Mounting

**Temporary Mounting**
- In a temporary mount point we will create a directory and mount it, but this mount will last only till the system is up, once it is rebooted the mounting will be lost.
- `mount <device-name> <directory-name(mount point)>` <br> ex: `mount /dev/sda7/<folder-name>`
- `mount` - To view mounted partitions
- `unmount <mount point directory` For unmounting a partition.
**permanent mounting**
- permanent Mounting procedure is exactly same like temp mounting, but here we will update the /etc/fstab file with the mounting details, so that it will be mounted even after the system is reboot. 

**steps to make a permanent mount point**
- make a directory  or use an existing directory
- Add entry in `/etc/fstab` file. use `vi /etc/fstab`
- use `mount -a` command to check it is mounting.

- sometimes a directory reflects error while unmounting, the possible causes for it are 
    - you are in the same directory and trying to unmount it. check with `pwd` command
    - some users are present in the directory and using the contents in it.
    - check with `fuser -cu /dev/sda7`
    - check for the files which are open with `lsof /dev/sda7`
    - Kill the open connections using `fuser -ck /kernel/hello` where hello is the file which is open.
    - Now you can use `umount` command to unmount the file system.
    - `df -h` To view the usage information of mounted partition
    - `du -h` To view the size of a file or directory
    
- Assigning label is giving some name to the partition. To assign label to the partition `e2label` command is used.
- `e2label <partition name> <label>` to check the label<br> EX: `mount LABEL=ktdisk /kernel` Mounting /dev/sda7 partition with its label ktdisk, verify it with mount command.
- `mount -l` To list all the mounted partition along with their labels, use `mount -l` command.

**Mounting a partition permanently with its block id (UUID)**
- To check the uuid of a partition use `blkid /dev/sda7` command.
- copy the uuid
- Make an entry in `/etc/fstab` using UUID
- verify it with `mount -a` option

##### swap partition
- swap space in linux is used when the amount of physical memory (RAM) is full. if the system needs more memory resources and the RAM is full, inactive pages in memory are moved to the swap space. 
- while swap space can help machines with a small amount of RAM, it should not be considered as a replacement for more RAM.  swap space is located in harddrives, which have slower access time than physical memory.

**commands used in maintaining swap spaces**
|command | Description |
| --- | --- |
|`free -m`| To see the memory size and swap space size |
|`swapon -s`|To see the swap usage use|
|`mkswap <partition name>`|To format the partition with swap filesystem use |
|`swapon <partition name>`| To activate the swap space use |
|`swapoff <partition name>`| To deactivate the swap space use |
- create a normal partition using `fdisk` and change hex code to make it swap partition. The hex code for SWAP is '82'(To change use `t` in fdisk and list all the hex code use `l`.

**Encrypting a partition using LUKs(Linux Unified Key SetUp**

- LUKs is a standard format for device encryption
- LUKs ensures the date protection inside the partition, especially against the data breach.
- It encrypts the partition or volume, which will decrypt only by providing correct password.
- The partition must be decrypted before the system in it can be mounted.
- once it is open (decrypted) you can work with the partition normally i.e; mounting and adding the data to the partition
- After the completion of work the partition has to be closed. i.e; encrypted so that it cannot be mounted nor can be accessible by others, unless you lose password.

**Steps to Encrypt the partition: **
    - create a normal partition using `fdisk`
    - format the partition using `LUKs` and assign the passphrase
    - Decrypt the partition
    - Now format again using normal ext4 formatting.
    - Mount the partition, Make a permanent mount
    - Access the partition and add the data
    - Unmount the partition and close the partition i.e; encrypt back.
    
|command |Description|
| --- | --- |
|`fdisk <disk folder>` <br> Ex; /dev/sda| create a normal partition|
|`cryptsetup luksFormat`| To format the partition with encryption, and assigning the password|
|`cryptsetup luksOpen`| To open or decrypt the partition.(password is required ) and you need to assign some **name** to it, which will be used for further operation as `/dev/mapper/name`|
|`cryptsetup luksClose`| To close or encrypt back the partition after use|
|`cryptsetup luksAddkey`| To add the key(password) to the configuration to automatically decrypting the partition |


### Manage and configure LVM Storage

##### Logical volume management

- The linux Logical Volume Manager (LVM) is a mechanism to virtualize the disks. it can create "virtual" disk partitions out of one or more physical hard drives, allowing you to grow, shrink or move those partitions from drive to drive as your needs change. 
- It also allows you to create larger partitions than you could achieve with a single drive.
- Traditional uses of LVM have included databases and company file servers.
- LVM is also convenient ways to gain redundancy without sacrificing flexibility

![image](https://user-images.githubusercontent.com/89054489/228176809-a3c23901-d1ab-449a-9dd4-af1129b08d95.png)

- Above picture shows the structure of LVM. LVM consists of **physical volume, volume group, logical volumes and file system**. 
- The physical partition is also called as **physical extents(PE)** and logical partitions are known as **logical extents(LE)**

#### components of LVM in Linux :
- Physical Volume (pg)
- Physical Extent (PE)
- Volume Group (VG)
- Logical Volume (LV)
- Logical Extent (LE)

###### Physical Volume (PV)
- It is the standard partition that you add to the LVM. Normally, a physical volume is a standard primary or logical partition with the hex code `8e`

###### Physical Extent (PE)
- It ia a chunk of disk space. Every PV is divided into a number of equal sized PEs

###### Volume Group (VG)
- It is composed of a group of PV's and LV's. It is the organizational group for LVM.

###### Logical volume (LV)
- composed of group of LEs. you can format and mount any file system on an LV. The size of these LV's can easily be increased or decreased as per the request.

###### Logical Extent (LE)
- It is also a chunk of disk apce. Every LE is mappet to a specific PE.

| LVM command | Function |
| --- | --- |
|`pvs` | Displays all the physical volumes|
|`vgs` | Displays all volume groups in the system |
|`lvs` | Displays all the logical volumes in the system|
|`pvdisplay`| Displays detailed information on physical volumes|
|`vgdisplay`| Displays detailed information on volume groups |
|`lvdisplay` | Displays detailed information on logical volumes |
|`pvcreate` | create a new physical volume |
|`vgcreate` | create a new volume group |
|`lvcreate` | create a logical volume |
|`vgextend` | Add a new physical disk to a volume group |
|`lvextend` | extends a logical volume |
|`lvresize`| resizes a logical volume |
|`lvreduce`|Reduces a logical volume |
|`pvmove`| Moves/migrates data from one physical volume to another |
|`vgremove`| Remove/Delete a volume group |
|`lvremove`| Remove/Delete a logical volume |

**Creating a physical volume (pv) **
- create a partition using fdisk, change the hex code to `8e`
- save and exit the fdisk and update the partition table using `parted-a` command
- create a PV on newly created partition i.e; /dev/sda7
- verify it by `pvs` or `pvdisplay` command EX: `pvcreate <partition name>`

**creating a volume group**
- After creating a `pv`, the next step is to create a `volume group or VG` 
- To create a VG the syntax is 
`vgcreate <name for the VG> <partition name>`
- verify it by using `vgs` or `vgdisplay <vgname>`
- To check all the VGs detail you can also use the command `vgdisplay` - It willl list ist out all the VGs in the system in detail.

**Logical Volume Creation**
- once we are ready with a **volume group** then it's the time to create a **logical volume LV**
- The syntax for creating an **LV** is `lvcreate -L <size of LV> -n <name for LV> <VG name>
- verify the **LV** by using the following commands
- **lvs or lvdisplay** to display all the LVs available in the system
- **lvdisplay <VG name> ` to display the LVs of a particular **volume group** 

**Adding file system to the LV and Mounting it**
- As per now we have our VG created so is our LV. In order to make it accessible we need to format it with a file system like ext4 or ext3 or vfat
- The syntax for formatting an LV is exactly like formatting a normal partition, Instead of /dev/partition name we use the path of `LV` that will be something like `/dev/vg/lv`
- `mkfs.ext4 /dev/ktvg/ktlv`

**Mounting **
- Mounting an LV is exactly same like a normal partition, again the path for mounting will be `/dev/vg/lv`
- Create a directory over which the LV should be mounted `mount <dev/vgname/lvname> /directory name
- verify the mounting with `mount` command
- Make it a permanent mount  by making an entry in `/etc/fstab`

**Extending a volume group**
- Extending a volume group is actually adding a new PV to the volume group. 
- To extend a volume group we need to create a new partition using `fdisk`. Don’t forget to 
change its hex code to `8e` and update the partition table using `partx –a` command
- Create a PV on the newly created partition using `pvcreate` command
- Add the partition to the VG using vgextend command, the syntax for it is
- `vgextend <VG name> <partition name>`
- `#vgextend ktvg `/dev/sda8`
-  Verify it `pvs` command

**Increasing the size of logical volume**
- Sometimes the file system size may be full, so we need to increase the size of the LV to 
continue adding the data in it.
- The size of LV can be increased online, no downtime is required.
- Check the current size of the LV by using `df –h` command.
- Increase the size of the LV by using `lvextend` or `lvresize` command, the syntax for it is
- `lvextend –L <+addition size> </dev/vg/lv name>` (syntax for lvresize is also same)
- `lvextend –L +200M /dev/ktvg/ktlv`
- Update the file system by using `resize2fs` command
- `resize2fs /dev/vg/lv name`
- `resize2fs /dev/ktvg/ktlv` 
- erify the change by using `df –h` command

**Reducing the size of an LV **
- Reducing the size of an LV is a bit complicated task, there are few things which you need to 
keep in mind before reducing the size of an LV.
- LV size cannot be reduced online, it requires a down time i.e. unmounting the file 
system.
- Organized the data before reducing the size of LV.
- Update the file system about the size. I.e. what its size will be after reduction.
- Finally reduce the size. Huh….! Lots of things to do!!!!
- If any of the above things are missed then it will be a mess, you may corrupt the file system and LV.

Let’s start the steps carefully

- Check the size of the lv using `df –h` command
- Unmount the LV using umount command
- Organize the data in LV by using `e2fsck` command
- `e2fsck -f /dev/ktvg/ktlv`.
- Update the file system by using `resize2fs` command
- resize2fs /dev/ktvg/ktlv 300M (where 300M is the approximate total size of LV after reduction)
- Now reduce the size by using # lvreduce -L -200M /dev/ktvg/ktlv command
- We know the size of LV is around 500MB, from previous picture in case of extending the size of LV.
- Or else you can run `df –h` and verify it again.
- Umount the LV by using umount command

**MOving or Migrating the LV (date) from one pv to another**

- There might be a situation where `pv` might be failing and it is reequired to be replaced, in such case, we need to migrate or move the data from such `pv` to other and isolate the `pv`

**Steps to migrate the pv are **

- Access the mount point of failing PV and check the data in it,
- Verify the size of the PV by `pvs` command or pvdisplay command. 
- Unmount the file system on that PV.
- Add new PV, which should be of the same size or higher than that of the replacing 
PV to the volume group.
- Migrate the PVs contents to the new PV using following command
- #pvmove <Old PV> <New PV>
- Mount back the `LV`, access the mount point and verify the data in it.
- Remove the faulty PV from Volume Group.

**Remove the faulty PV from Volume Group**
- As the data moved safely, now let's remove the faulty `pv` from the volume group
- the syntax to remove a `pv` from a vg is `vgreduce <vg name> <PV name>`

**Deleting/Removing an LV:**

- To Delete/Remove an LV, first unmount the file system.
- Remove the entry from `/etc/fstab`.
- Use the command `lvremove` i.e.
- `lvremove <LV name>`
- #lvremove ktlv ( it will prompt to you to continue, press y to continue)
- Verify it by using `lvdisplay` command

**Deleting a volume group**

- To delete the volume a group, make sure that if there is any LV in it, it should not be 
mounted. Because while removing a vg it will also remove LV’s inside it. In our case we have 
no LV in our volume group, so we will not be concerned about it.
- To delete a VG, use the following command.
- `vgremove <vgname>`

**Deleting a physical Volume**

- Deleting a PV is very simple. The only thing we should check that the PV we are going to 
delete should not belong to any volume group. We can only delete a PV which is free.
- The syntax to delete a PV is 
- `pvremove <PV name>`
- `pvremove /dev/sda(6,7)` (To remove multiple PVs in one command)

**Creating a VG by specifying the PE size**
- To create a VG with specifying an PE size
- First create a partition and also create a PV
- To create a vg with custom PE size use
` vgcreate <name for the vg> -s <size of PE(1-128)> <pv names>
- verify the PE size using `vgdisplay` command

**creating an LV of 400 MB, specifying no.of LE instead of giving size in MB or GB**

- To create an LV using LE, the things to keep in mind are `size of LE=size of PE`
- In command we are specifying the no.of LE not the size of LE, as the size of LE is based on size of PE
- For ex: if the size of PE is 16, then the size of Le will also be 16.
- The formula for calculating no. of LE is <br>
<size of LV required, in MB> divided by Size of PE
- if the size of LV is to be 2 GB then first we need to convert GB into MB and then calculate 2x1024 / 16 =128
- You can use `bc` command to do all the calculations. Use `ctrl+d` or `ctrl + c` to quit the calculator.
- So now we got the calculation done and we came to know that 25 LEs are required to 
create 400MB of LV.
- The syntax to create an LV with no. of LE is
`lvcreate –l <no. of LE> -n <name for the LV> <volume group name>` <br>
`lvcreate –l 25 –n ktlv2 ktvg2`

- Now check the size of the LV “ktlv2” using lvdisplay command
 `lvdisplay ktvg`
 
