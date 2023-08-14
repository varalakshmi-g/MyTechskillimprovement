
## Managing  installed services

There are 2 commands used to control services
<br>1. chkconfig and 2. service


## software Management

To manage the software in linux, two utilities are used,

1. RPM - Redhat Package Manager <br>
2. YUM - yellowdog updater modified

**Red hat package manager**

- RPM is a package management system ( collection of tools to manage software packages ). RPM is a powerful software management tool for installing, uninstalling, verifying, querying and updating software packages.
- RPM is a straight forward program to perform the above software management tasks

Features :

- RPM can verify software packages
- RPM can be served as a powerful search engine to search for software's
- components, software's etc can be upgraded using RPM without having to reinstall them
- installing, reinstalling can be done with ease using RPM
- During updates RPM handles configuration files carefully, so that the customization is not lost

`rpm -qa` -- to list/check all the installed packages in the system. where q stands for query and a stands for all

`rpm -qa <package name>` or `rpm -q <package name>` -- To check a particular package is installed or not

`rpm -qa | grep -i <package name>` -- To ignore case sensitivity of a package

`rpm -ivh --test <package name>` -- To check the package's consistency here i=install, v=verbose view h=hash progress

`finger <username>` -- check the installed package by using finger command. Finger is used to check user's details

`rpm -e <package name>` To remove a package 

`rpm -qip <package name>` --To see the info of a package where q is query, i is install and p is package

`rpm -qi <package name>` -- To see the information or details about the installed package 

`which <command name>` --To  check the installed location of a command

- `rpm -qf <path of the command>` -- To check the package of a particular command 

- `rpm -ivh <package name> --force` - To force install a particular package

-`rpm -qlc <package name>` -- To see the configuration files of the installed package 

`rpm -qld <package name >` -- To see the directory with which a program is associated

`rpm -ivh <package name> --nodeps` - To install a package without dependencies

`rpm -uvh <package name>` -To update a package

**yellowdog updater modified**

## Backup and restore

![image](https://user-images.githubusercontent.com/89054489/233556181-8ab1c5cc-e8b1-4f5c-9340-5102c407a856.png)

| command | Description |
| --- | --- |
|`tar -cvf <destination and name to be> <source file>` | To backup the file using tar |
| `du -h <file name>`| To check the size of the tar file |
|`gzip <file name>` | Apply gzip on tar file and check the size |
|`scp <source file> <destination file>`| To transfer the file to other system using scp |
|`gunzip <file-name>` | To gunzip a file |
|`tar -xvf <file-name>`| To untar a file |


## Job Automation


##### Automation with cron and at
- In any Operating system, it is possible to create jobs that you want to reoccur, This prcess is known as **Job Scheduling** is usually done based on user-defined jobs. For all linux distros, this proces is handled by a cron service or daemon called **crond**

- The importance of the job scheduling is that the critical tasks like taking backups, which the clients usually wants to be taken in nights, can easily performed without the intervention of the administrator by scheduling a cron job. if cron job is scheduled carefully then the backup will be taken at any given time of the clinet and there will be no need for the administrator to remain back at night to take the backup.

**Important files related to cron and at**
- **/etc/crontab** is the file which stores all the scheduled jobs
-**/etc/cron.deny** is the file used to restrict the users from using the cron jobs.
- **/etc/cron.allow** is used to allow only users whose names are mentioned in the file to use cron jobs. (This file doesn't exist by default)
- **/etc/at.deny** same as cron.deny for restricting at jobs
-**/etc/at.allow** same as cron.allow for allowing user to use at jobs.

**crontab format**
- To assign a job in the crontab file the format used is the following

![image](https://user-images.githubusercontent.com/89054489/230766565-aafde0f2-a2e9-4d6c-9f1d-68cf9b6f4b4d.png)

| options | Explanation |
| ---- | ---- |
| * | Is treated as a wild card, Meaning any possible value |
|*/5 | Is treated as every 5 minutes, hours,days, or months. Replacing 5 with another numerical value will change this option |
| 2,4,6 | Treated as an OR, so if placed in the hoours, this could mean at 2,4 or 6 o clock |
| 9-17 | Treats for any value between 9 and 17 . so, if placed in the day of month this would be days 9 through 17 or if put in hours it would be between 9 and 5. |

crontab commands
| command | Explanation |
| --- | ---|
| `crontab -e` | Edit your crontab file, or create one if it doesn't already exist |
|`crontab -l` | Display your crontab file |
|`crontab -r` | Remove your crontab file |
|`crontab -u` | if you combine with -e , edit a particular user's crontab file and if combined with -l, display a particular users crontab file. if combined with -r, deletes a particular user's crontab file |

`tty` -- To check the console on which you are working

`service crond restart`  -- Restart the cron services

**schedule a job to run the backupscript "bkpscript.sh" on every "saturday 12.30 pm"**

- in order to schedule above job the steps are
- Check the location of script and also check whether it is having execute permission or not. If not then add the execute permission to all user on it.

`ls`--> `pwd` ----> `ls -l bkpscript.sh` --> `chmod a+x bkpscript.sh` --> `ls -l bkpscript.sh`

`!ser` --> is the command to restart the last restarted service

**AT jobs**

- "at" is used to schedule a job for a particular time or interval, in other words, it is used for one time or only for one interval

The advantages at jobs are :

- It can be modified like cront jobs
- It cannot be reused
- The content cannot to viewed in normal human readable format

`tty` --> to schedule at job to display current date on current console "now"

**schedule at jobs to get a mail at 11.30 AM regarding meeting `at 11.30 pm`

`at -l` or `atq` --> To check the list of at jobs.

`at -c <job-id> ` --> To check what is scheduled
`atrm` --> to remove the job

- Restricting a user from using at jobs :

- To restrict a user from using at jobs it is exactly same like crontab.
- if both at.allow and at.deny etc, then at.allow will have higher priority


## Administrating Remote system

**Remote shell access using SSH**

** what is SSH ? **
- There are a couple of ways that you can access a shell (command line) remotely on most 
Linux/Unix systems. 
- One of the older ways is to use the telnet program, which is available on 
most network capable operating systems. Accessing a shell account through the telnet method 
though poses a danger in that everything that you send or receive over that telnet session is 
visible in plain text on your local network, and the local network of the machine you are 
connecting to.
- So anyone who can "sniff" the connection in-between can see your username, 
password, email that you read, and command that you run. For these reasons you need a more 
sophisticated program than telnet to connect to a remote host.
SSH, which is an acronym for Secure SHell, was designed and created to provide the best 
security when accessing another computer remotely. Not only does it encrypt the session, it 
also provides better authentication facilities.

![image](https://user-images.githubusercontent.com/89054489/232980699-a15da624-96fc-4fa6-837c-46e708782f27.png)

- These two diagrams above show how a telnet session can be viewed by anyone on the network 
by using a sniffing program like Ethereal (now called Wireshark) or tcpdump. It is really rather 
trivial to do this and so anyone on the network can steal your passwords and other information. 
The first diagram shows user jsmith logging in to a remote server through a telnet connection. 
He types his username jsmith and password C0lts06! which are viewable by anyone who is 
using the same networks that he is using. 

- The second diagram shows how the data in an encrypted connection like SSH is encrypted on 
the network and so cannot be read by anyone who doesn't have the session-negotiated keys, 
which is just a fancy way of saying the data is scrambled. The server still can read the 
information, but only after negotiating the encrypted session with the client. 

- SSH configuration file is **/etc/ssh/sshd_config**
- SSH demon or service is **sshd**


| command | Description |
| -------- | --------- |
| `ssh <ip address/hostname of remote machine>` <br> Note : hostname can only be used when the hostname is saved in /etc/hosts file or if DNS is configured | To access the remote machine using ssh |

**Password less login using SSH Keys**

- As a system administrator, one person will be assigned to manage many systems, for 
example one person has to manage more than 10 systems at a time. In this situation admin 
has to transfer some files from one system to another 9 systems or vice versa, for every 
login on remote system it will prompt for password. Even for transferring files for every 
transfer we need to enter the password.
- Above situation will be very annoying for system admin to type password for every step. 
Therefore SSH provides a best way to escape password prompting every now and then.
 By generating SSH keys, a public key and a private key, an admin can copy the public key 
into other system and done, it will work as authorized access from the admin’s system. Now 
whenever we are logging from admin’s system to other system in which we have stored the 
public key of admin’s system, it will not prompt us for password and we can login to that 
system as many time as we want without being prompt for the password.
- SSH keys are an implementation of public-key cryptography. They solve the problem of 
brute-force password attacks by making them computationally impractical.
- Public key cryptography uses a public key to encrypt data and a private key to decrypt it .

steps involved in it :

--> Generate SSH keypair by using `ssh-keygen` <br> It will prompt above to mention the file where these keys shoud be stored, to keep its default 
directory just press “Enter”. The default location will be /root/.ssh/ directory

Now it will ask for passphrase, which will be used instead of password. The passphrase will only 
be asked once per session. Enter your desired passphrase twice as shown on next page, and 
press enter.

--> Now our keys are successfully generated, go to /root/.ssh/ directory and check for the keys using `cd /root/.ssh`

the id_rsa is a private key and id _rsa.pub is the public key which will be used later to make 
password less login.

--> **Copying the public key on client system** by using `#ssh-copy-id –i <public key location> <clients IP address> (or user @ client IP`

- Enter the password of the client to proceed, check it on client side whether it is copied or not<br>
Move to client system and check whether the key is copied properly or not
<br>To check the key navigate to /root/.ssh/ directory and check for authorzed_keys file which 
will hold all the system which are authorized and will not be asked for password..<br>
`#cd /root/.ssh/`<br>
`#cat authorized_keys`

- Try login to the client machine using SSH, check whether it is asking for password
<br> For logging into client machine the procedure is same as shown earlier. But as we have 
assigned a passphrase it will ask us for it. Once you enter a passphrase it will last until you 
logged out of server’s session. Let’s see it practically.<br>
#ssh 192.168.10.95 <br>
It will prompt for the passphrase as shown below, enter the passphrase and press Enter

 Exit the client session and login again. Notice the change <br>
While we logout the client session and re-login again it will not ask us for passphrase

- Logout of client session and completely logoff the server, login once again in server and 
connect the client using SSH.
- As we log off completely from the server then login once again and try to connect the client, 
it will prompt for passphrase.

| command | Description |
| --- | --- |
|`ssh-keygen` | To generate SSH key pair <br> The default location of keys storage is /root/.ssh/ directory <br> **id_rsa** is a private key and **id_rsa.pub** is the public key |
| `ssh-copy-id -i <public key location> <client's IP address> or user @ client IP )` | copying the public key on client system |

**Remote file transfer with SCP and RSYNC **

**SCP(Secure copy)**

-  scp stands for secure cp (copy), which means that you can copy files across an ssh 
connection that will be encrypted, and therefore secured. As scp will be using ssh protocol 
to transfer the data, hence it is termed as the safest method of transferring data from one 
location to another.

To copy a file using SCP to remote machine from source location
- We are having a file ktfile in “/” directory, in the server ktlinux.kt.com who’s IP is 
192.168.10.98, and we need to copy the same in other server’s i.e. ktcl5.kt.com with an IP 
192.168.10.95, /root directory. Then,
- The syntax for SCP a file from source location.
#scp <file name > <remote hosts IP >:/<location to copy the file >
#scp /ktfile 192.168.10.95:/root/
- Now log in to destination system and check whether if the file is there.
To copy a file using SCP from a remote machine being in destination’s location
- Let’s reverse the previous task, login to ktcl5 machine whose IP is 192.168.10.95, and 
transfer a file from ktlinux machine whose IP is 192.168.10.98
- Let’s first remove the earlier copied file ktfile, then copy it again from destination’s location.
- The syntax for SCP a file from destination location.
#scp <source system’s IP>:/<location of file to be copied> <destination location to copy>
Note: Password will be asked for every transfer if public key is not saved on both locations, in 

  our case we have already generated and copied the key, hence there is no password prompts.

To copy a directory using SCP to remote machine from source’s location
- We are having a directory ktdir in“/” directory, in the server ktlinux.kt.com who’s IP is 
192.168.10.98, and we need to copy the same in other server’s i.e. ktcl5.kt.com with an IP 
192.168.10.95, /root directory. Then,
- The syntax SCP a directory from source’s location, the syntax is
#scp <option> <dir name > <remote hosts IP >:/<location to copy the directory >
#scp -r /ktdir 192.168.10.95:/root/
To copy a directory using SCP from a remote machine being in destination’s location
- Let’s reverse the previous task, login to ktcl5 machine who’s IP is 192.168.10.95, and 
transfer a directory ktdir from ktlinux machine whose IP is 192.168.10.98
- Let’s first remove the earlier copied directory ktdir, then copy it again being in destination’s 
location.
- The syntax for SCP a file from destination location.
#scp <option> <source system’s IP>:/<location of file to be copied> <destination location 
to copy>
#scp –r 192.168.10.98:/ktdir /root/


**RSYNC (REMOTE SYNCHRONIZATION)**
  
- rsync is a very good program for backing up/mirroring a directory tree of files from one 
machine to another machine, and for keeping the two machines "in sync." It's designed to 
speed up file transfer by copying the differences between two files rather than copying an entire file 
every time.
- For example, Assume that we are suppose to take the backup of a system and copy the same to 
another system. For first time we will copy entire directory, but every day if we copy entire directory 
it will kill lots of time. In such situation if rsync is used it will only copy the updated files/directories 
rather than copying all files/directories inside main directory, which saves lots of time and speedup 
the transfer
- If rsync is combined with ssh it makes a great utility to sync the data securely. If rsync is not used 
with ssh, the risk sniffing will always be there

  Copy a directory using SCP, then update it and try rsync with SSH and check if the data is 
synced.
 As we have already copy a directory earlier using SCP from ktlinux to ktcl5 system, let’ s use 
it for rsync.
 Update the directory with some files in ktlinux system
 Check the content of same directory in ktcl5
 Use rsync to sync the directory on ktcl5 machine, with the one in ktlinux machine
 The syntax to rsycn a directory is 
#rsync <options> <encryption> <source dir> <destination IP>:/<location of destination 
dir>
#rsync –rv -e ssh /ktdir 192.168.10.95:/root/
Observe that it is only copying the files which are not there in destination’s folder.

  
Note: If you don’t want to use ssh just remove –e option from above syntax, but the drawback 
of it is there will be no encryption
 To compress the data and send it in archive mode use -avz instead of -rv in rsync
Sync a file using rsync with ssh 
 Let’s check the file called ktfile1 on both ktlinux and ktcl5 machines
 
 Update the file ktfile1 in ktlinux, sync it with rsync to ktcl5 and check the file again.
 The syntax for syncing a file is 
#rsync –avz –e ssh <source file> <destination ip>:/<location of file >
  
   `/etc/sudoers` this is where all the rules that users has to follow when using sudo command
 `visudo` to edit rules
  `/var/log/secure` --all commands executed by sudo users 
  
  
DNS configuration
Virtual hosting
