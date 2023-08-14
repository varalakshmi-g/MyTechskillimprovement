
## User Administration

- In Linux/Unix  user is one who uses the system. There can be at least one or more than one users in the linux at a time. 
- Users on a system are identified by a username and a userid. The username is something that users would normally refer to, but as far as operating system is concerned this is refered to using the user id (or uid) 
-  The username is typically a user-friendly string, such as your name, whereas the userid is a number. 
- The words username and userid are often (incorrectly) used interchangeably . 
- The user id numbers should be unique (one number per user) 
- if you had two usernames with same user id, effectively there permissions would be the same and the files that they create would appear to have created by the same user.
-  This should not be allowed and the useradd command will not allow usernames to share 
the same userid.

**some important points related to users :**

- Users and groups are used to control access to files and resources
- users login to the system by supplying their username and password
- Every file on the system is owned by a user and associated with a group
- Every process has an owner and group affiliation, and can only access the resources that it's owners or group can access.
- Every user of the system is assigned to a unique user id number (UUID)
- Users name and UID is stored in `/etc/passwd`
- User's password is stored in `/etc/shadow` in encrypted form.
- user's are assigned a `home directory` and a program that is run when they login (usually a shell)
- Users cannot read,write or execute each other's files without permission

#### Types of users in Linux and their attributes :

|Type | Example | User id (UID) | Group ID (GID) | Home Directory |Shell |
| --- | --- | --- | --- | --- |---|
|ROOT | 0 | 0 | /root | /bin/bash |
|ftp,ssh,apache nobody | 1 to 499 | /var/ftp, etc | /sbin/nologin |
|visitor, ktuser, etc | 500 to 60000 | 500 to 60000 | /home/user name | /bin/bash |

In linux there are 3 types of users.

**1. super user or root user**
- Super user or the root user is the most powerful user. He is administrator user.
**2. system user **
- system users are the users created by the softwares or applications. For ex: if we install apache it will create a user apache. These kinds of users are known as system users.
**3. Normal User**
- Normal users are the users created by root user. They are normal users like charan, teja etc. only the root user has the permission to create or remove user.

Whenever a user is created in linux below things created by default :
- A home directory is created (/home/username)
- A mail box is created (/var/spool/mail )
- A unique UID and GID are given to user.

There are two important files a user adminstator should be aware of 

1. "/etc/passwd"
2. "/etc/shadow"

`$ compgen -u` to list the users
1. `/etc/passwd`
2. 
3. ![image](https://user-images.githubusercontent.com/89054489/228425946-3c7dae40-29d8-4c57-a6d5-d0a57b3d6a39.png)

2.`etc/shadow`


![image](https://user-images.githubusercontent.com/89054489/228426093-08ecc7ee-56c3-4e0c-883b-fb2cd5a16a0a.png)


**Password Complexity Requirements :**

- A root user can change password of self and of any user in the system, there are no rules for 
root to assign a password. Root can assign any length of password either long or short, it 
can be alphabet or numeric or both. On the whole there is no limitation for root for 
assigning a password.
- A normal user can change only its password. Valid password for a normal user should adhere to 
the following rules
- It should be at least 7 characters but not more than 255 characters.
- At least one character should be Upper case
- At least one character should be Lower case
- At least one character should be a symbol, and one character should be a number.
- It should not match the previous password.
- It cannot have a sequence (ex: 123456 or abcdef )
- The login name and the password cannot be same.  

- In linux whenever a user is created it has its own primary group. EX: if a user is created with the name 'charan'. then a primary group for that user will be 'charan' only.

##### creating a user
- the syntax for creating a user in linux is `useradd <option> <username>`
  - -u userid
  - -G secondary group id
  - -g primary group id
  - -d home directory
  - -c comment
  - -s shell

let's create a user with attributes as name = charan, uid = 30, home dir = /home/learner, comment = teaching

`useradd charan -u 30 -g 30 -d /home/learner -c teaching`

- `passwd` to assign password to current user ( the one with which you to logged in, if it is root then root's password will be changed `
- `passwd <user name>` to assign a password to a specific user, only root can assign password to other user.

##### Modifying the user's attribute

- After creating a user if we need to modify the attributes of user like changing uid, changing secondary group id or adding a comment, locking or unlocking the user account, can be done by following the command.
- `usermod <options> <username>`
options are :

-l to change login name
-L to LOCK account
-U to Unlock account

Note : when account is locked it will show (exclamation mark !) in /etc/shadow file

##### The password parameters
- For any user we can set the parameters for the password, like min and max password age, password expiration warnings and a/c expiration date etc.
- To view the advanced parameters of the user, use `chage -l <user name>`

- The second method to change the particular field of password is

`chage <option> <value> <username>`
- The options which can be used are as follows :

  - -m for Min password age
  - -M for Max password age
  - -d for last time the password is changed
  - -W password expiration warnings
  - -I password inactive [-1 means inactive]
  - -E A/C expiration date

##### Deleting a user :
- `userdel <username.` It will delete only the user but home directory will be there. To delete the user with its home directory use the following command.
- `userdel -r <user name>` 

### Group Administration

**Groups **
  - Users are asssigned to groups with unique group ID number (GID)
  - The group name and GID are stored in /etc/group
  - Each user is given their own private group
  - They can also be added to their groups to gain additional access
  - All users in a group can share files that belong to the group.

- Each user is a member of at least one group, called primary group. In addition, a user can be a member of an unlimited number of secondary groups. Group memberships can be used to control the files that a user can read and edit. 
- EX: if two users are working on the same project you might put them in the same group so they can edit a particular file that other users cannot access.

- user's primary group is defined in the `/etc/passwd` file and secondary groups are defined in the `/etc/group` file
- The primary group is important because files created by this user will inherit that group affiliation

`groupadd <name of the group>` To create a group
<br>`groupadd <option> <name for the group>` ex: `groupadd -g 483 charangroup`

we can verify it in `/etc/group`

`groupmod <options> <arguments> <group name>`

Here the `options` are -g to change the group id
- - o to override the previous assigned id, if it matches with the new one
- - n to change the group name

`usermod -G <group name> <user name>` -To add the single user to the group

`gpasswd <option> <arguments> <group name>`

options

- -M for adding multiple users to the group
- -A for adding a group administrator
- -a For adding a single user to the group
- -d removing a user from a group

`gpasswd -M <u1>,<u2>,<u3> <group>


### Controlling Access to files

1. Special permissions or advanced permission <br>
2. Access control list (ACL)

**1. Special Permissions or advanced permission**

- There are three special permissions that can be assigned to a file or directory apart from basic file permissions (rwx), they are 
  - SUID - set user id
  - SGUID - set group id
  - Sticky bit

|Permission | Symbolic form | Numeric form | syntax |
| --- | --- | --- | --- |
|SETUID | s or S | 4 | `chmod u+s or chmod 4766` |
|SETGID | s or S | 2 | `chmod g+s or chmod 2766` |
|Sticky bit | t or T | 1 | `chmod o+t or chmod 1766` |

**Note : ** where s= setuid + execute permission and S = setuid only. Same is for SGID and also for sticky bit.

**SUID - Set User ID**
- if SETUID bit is set, when the file be executed by a user, the process will have the same rights as the owner of the file being executed. Many of the system commands are best example for SUID, basically the owner of the commands will be root but still, a normal user can execute it.

EX : By default, ping command is having suid, so all users can run that command but if suid is removed and normal user wants to  execute it, it will show 'operation not permitted'

`chmod u-s /bin/png`

**SGUD - set group id**

- set group ID, user on executable files to allow the file to be run as if logged into the group. 
- SGID can also be used on a directory so that every file created in that directory will have the dierctory group owner rather than the group owner of the user creating the file.

Note : when a file is created by any user it will get the group as primary group of the owner which is usually owner's private group with same name.

**Sticky bit**
- If sticky bit is applied to a file / directory, then only  root and owner of that file or directory can delete it. Even if the others having full permissions the cannot delete the file/directory.

**Access Control List (ACL)**

- Define more fine-grained discretionary access rights for files and directories.
- often, you want to share files among certain groups and specific users. It is a good practice to designate a directory for that purpose. You want to allow those groups and users to read, and write files in that directory, as well as create new files into the directory. Such special permission can be given using ACL.
- ACL can be applied on ACL enabled partition that mean you need to enable ACL while mounting the partition.

**steps to implement ACL**
- create a partition and format it with ext4 file system.

`parted -l <file/folder path>`

- Mount a file system with ACL
`mount -o acl <file location> <directory>`

If your partition is already exists, then just add an `acl` after defaults as shown above and use the following command.
`mount -o remount <file path>EX: /dev/sda7`
- apply ACL on it.

To check the acl permission syntax is `getfacl <option> <dir/file name>`

**Options:**

-d -- Displays the default ACL

-R -- Recurses into subdirectories

The syntax to apply acl is `setfacl <option> <argument> <file or directory name>`

The options are,

-m Modifies an ACL <br>
-x Removes an ACL <br>
-R Recurses into subdirectories

The possible arguments are U: user, g:group and o:others

**Note**: whatever ACL permisssions assigned to a user or group or others, it will be treated as Normal Permissions minus ACL

TO assign **read and execute** permissions to a particular user the syntax could be
`setfacl -m u: <username>:<permissions> <file or dir name>`
- verify it by using `getfacl` command









