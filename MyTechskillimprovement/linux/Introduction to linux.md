Before jumping to learn about linux, first let's learn some other fundamental concept related to linux.

### What is Operating System ?

- Operating system is an interface between user and the computer hardware. The hardware of the 
computer cannot understand the human readable language as it works on binaries i.e. 0's and 1's. Also it 
is very tough for humans to understand the binary language, in such case we need an interface which 
can translate human language to hardware and vice-versa for effective communication.

#### Types of Operating System:

1. Single User - Single Tasking Operating System<br>
2. Single User - Multitasking Operating System<br>
3. Multi User - Multitasking Operating System

**Single User - Single Tasking Operating System**

In this type of operating system only one user can log into system and can perform only one task at a 
time.
E.g.: MS-DOS

**Single User - Multi tasking operating System**

This type of O/S supports only one user to log into the system but a user can perform multiple tasks at a 
time, browsing internet while playing songs etc.
E.g.: Windows -98,Xp,vista,Seven etc.

**Multi User - Multi Tasking Operating System**

These type of O/S provides multiple users to log into the system and also each user can perform various 
tasks at a time. In a broader term multiple users can logged in to system and share the resources of the 
system at the same time.
E.g.: UNIX, LINUX etc

#### History of linux

To understand the linux we need to go back to 1984.

now we are in 1984, computer science was not very developed. Microsoft just launched MS-DOS. the operating system. is that means it is the only one , Absolutely no right ? yes, along with that we have another OS which is not famous as like as MS-DOS. i.e; UNIX

UNIX is little bit complicated when compared to MS-DOS.

##### GNU

GNU(GNU's not unix) Project is a free software, mass collaboration project, announced on sep 27, 1984 by richard stallman at MIT .

It's aim is to provide computer user's freedom and control in their use of computer devices, by collaborately developing and providing software that is based on the following

i.e; **freedom right :** users are free to run the software, share it(copy,distribute), study it, modify it.

GNU is an open operating system<br>
GNU should not only a free OS . But, it also has to be open

**what's the difference**

If it is free, it is about cost

If it is open, It is about cost and also any body can see, access,modify the source code of it.

**Linus torvalds , creator of LINUX**

Linus Torvalds, a student at the University of Helsinki (Finland), began creating his free own operating system. This system became known as Linux

well, **what the relationship b/w linux and GNU project.**

These two projects were complimentary. i.e; GNU project created a basic things of OS like program file copy, delete, file, text editor. but, linux started working on heart of it i.e; OS kernal

the combination of GNU (free programs) and Linux(OS kernal) project merged to create GNU/LINUX . But, due to uneasy to pronounce, we are Calling it as simply "LINUX"

Note : Mac OS and Linux are both based on UNIX, the ancestor of operating systems, while Windows, from MS-DOS is a separate branch. Overall, this is all you need to remember.

#### Linux distributions

linux distribution(in short distro) is an operating system made as a collection of software based around the linux kernel and often around a package management system.

The most well known distributions are RedHat, SUSE, Debian, Mandriva, Slackware and Ubuntu

To make life easier for users and allow them to make a choice, different Linux distributions were created. This is a concept that does not really exist in Windows.

Whichever distribution you install, you get a Linux compatible with others. Some distributions are just more or less easy to handle.

Linux is unix like and mostly POSIX complaint computer operating system assembled under the model of free and open source software development and distribution

Note :  POSIX stands for Portable Operating System Interface. It's a family of standards specified by IEEE for maintaining compatibility among operating systems.
linux is usually works as a server because of it's security feature and stability

so, ## why linux ?

- fresh implementation of UNIX API's
- Free and Open source development model
- Supports wide variety of hardware
- Supports mainly networking protocols and configurations
- It is fully supported worldwide community
- They are frequently updated with zero charge
- Highly secure

### Basic and essential commands in linux

**log into local & Remote graphical and text mode consoles**

Basic Concepts to Know :

- **Text Terminal**: text input/output environment
  - originally, They meant a piece of equipment through which you could interact with a computer. In early days of Unix, that meant a teleprinter-style device resembling a typewriter, sometimes called a teletypewriter, or "tty" in shorthand.
  - tty were used to establish a connection to a mainframe computer and share operating system provided by it.
  - A typical text terminal produces input and displays output and errors.

![image](https://user-images.githubusercontent.com/89054489/227131413-d6fe83d6-7c06-49f8-bf1f-f16fd33d1931.png)


**Console:** Terminal in modern computers that don't use mainframe but have an own operating system. it is the primary terminal directly connected to a machine.
  - The console appears to be operating system "like" a remote terminal
  - In linux and FreeBSD, the console, in realty, appears as several terminals(ttys) called Virtual Consoles.

**Virtual Consoles:** To provide several text terminals on a single computer.
- Multiple virtual consoles can be accessed simultaneously


![image](https://user-images.githubusercontent.com/89054489/227131659-e249744a-970e-4628-bdb5-b607977ed17b.png)

**Shell** Command line interface or CLI
- It is the primary interface that users see wwhen they log in, whose primary purpose is to start other programs.
- It is presented inside the console.
- There are manu different linux shells
- command line shells include flow control constructs to combine commands. In addition to typing commands at an interactive prompt, users can write shell scripts

In short,<br>
terminal = text input/output environment<br>
console = physical terminal<br>
shell = command line interpreter

For more information on terminal consose and shell, read below article 👇

https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line

To Summarize : A virtual console is a shell prompted in a non-graphical environment, accessed from the physical machine, not remotely
- **pseudo-terminal:** A terminal provided by programs called terminal emulators e.g. `ssh`, `tmux`
- **X windows System:** is a windowing system for bitmap displays.
  - X provides the basic framework for a graphical user interface(GUI) environment: drawing and moving windows on the display device and interacting with a mouse and keyboard.
  - It is considered "graphical terminal"
  - When it is executed it will substitute one of the text terminal provided by virtual console. In centOs the terminal will be 1, in other system could be 7.
  - some applications running inside X windows system provide pseudo-terminal e.g; Konsole, Gnome Terminal
  - if graphical environment is not started, you can run `startx` to execute it.
  
Log in :
- To log into local environment you must provide, when prompted, userID and password for both graphical and text mode
- To login into a remote text environment you can use command `ssh`
- To login into a remote graphical environment you can use command `ssh -X`

once logged command `w` can be used to show who is logged and what they are doing :
[root@localhost ~]# w
23:41:16 up 2 min,  2 users,  load average: 0.02, 0.02, 0.01
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
root     tty1                      23:40   60.00s  0.01s  0.01s -bash
root     pts/0    192.168.0.34     23:41    1.00s  0.02s  0.00s w

First column shows which user is logged into the system and the second one to which terminal.
- for Virtual console in terminal is showed tty1, tty2 etc
- for ssh remote sessions (pseudo-terminal) in terminal is showed pts/0, pts/1 etc.
- :0 is for X11server namely used for graphical login

Create, delete, copy, and move files and directories
You must be able to check results of activities.
| command  | Description |
| --- | --- |
|`ls` |list directory content |
|`ls -l` | long output. It will print more columns |

File Type+Permissions - Number of links - Owner - Group - Dimension - Creation date - Creation hour - Name

First letter of first column indicate file type:

- : file
d: directory
l: link

| | |
| --- | --- |
|`ls -la` | long output plus hidden files |
|`ls -lR`| long output recursive (show subdirectories content) |
|`ls -lt` | long output sorted by modification time |
|`ls -ld /etc` | show the directory properties and not its content |
|`du` | file show disk usage <brdu directory show space used by directory and each subdirectory. It is recursive |
|`du -s` | directory summarize space used by directory and subdirectory |
|`du *`| show space of each file in current directory |
|`pwd` | print current directory |
|`touch file` | It creates an empty file |
|`cp source destination`| copy source file to destination|
|`cp file1 file2 ./dest`| Copy file2 and file2 to directory dest |
|`cp * ./dest` | Copy all file of current directory to directory dest |
| `cp -r dir1 dir2` | Copy dir1 in dir2. -r recursive |
|`mkdir dir`| create directory dir |
|`mkdir -p dir/dir2`| Create a directory dir with a subdirecotory dir2 |
|`rmdir dir` | remove dir. Note: dir must be empty|
|`tree show`| directories tree|
|`yum -y install tree` | to install tree |
|`mv file file2` | rename file in file2 |
|`mv file dir` | move file in directory dir |
|`mv dir ..`| move directory dir at the upper directory level |
|`rm file` | delete file|
|`rm -f file` | remove read-only file |
|`rm -r dir` | remove directory dir and all subdirectories and files|

**Search for files**

- `find` is recursive without parameters
- Base syntax: find PATH PARAMETERS

| command | Description |
| --------- | ------------ |
|`find /etc -name "\*host*"`| search in /etc all file/directories with host in their name. * is wildcard<br> wildcard is a symbol or set of symbols representing other characters. In general, used in substituting any string or character. wildcards are mainly used to increase the effeciency and flexibility of searches in linux|
|`find . -perm 777 -exec rm -f '{}' \;`| search from current position all files/directories with permissions 777 and after remove them <br> `-exec` uses the result of find to do something<br>`{}` will be substitute with result of find <br>the exec's command must be contained between  `-exec` and `\;`<br>; is treated as end of command character in bash shell. For this i must escape it with \. if escaped it will be interpreted by find and not by bash shell.|
|`find /etc -size -100k`| search in /etc all files/directories with size less than 100kilobytes|
|`find . -maxdepth 3 -type f -size +2M`|search starting from current position, descending maximum three directories levels, files with size major of 2 megabyte.|
|`find . \( -name name1 -o -name name2 \)`|`-o` or, it is used to combine two conditions. \ is escape to avoid that ( or ) will be interpreted by bash shell |
|`find . -samefile file`| find all files that have same i-node of file|
|`find . \| -user owner`| It will show all files that  aren't owned by user owner. `|` means negation, but must be escaped by \ to not be interpreted by bash shell|
|`find . -iname name`| search for name ignoring case|
|`find . -perm 222`| find all files with permissions equal to 222.<br> EX: only files with permissions 222 will be showed. |
|`find . -perm -222`| find all files with at least permissions 222 <br> ex: 777 match as valid|
|`find . -perm /222`| find all the files with write for owner or write for group or write for others (atleast one)|
|`find . -perm -g-w`|find all the files with at least permissions write for a group|
|`find . -atime +1`|show all files accessed at least two days ago (more than 24 hours) |

#### compare and manipulate file content

| command | Description|
| --- | --- |
|`diff file1 file2`| compare file1 and file2|
|`diff -y file1 file2`| compare file1 and file2 with output in two columns|
|`uniq file`| Remove equal consecutive rows. |
|`uniq -w 2 file`|Remove equal consecutive rows comparing only first two characters|
|`uniq -c file`|Remove equal consecutive rows and show number of occurances|
|`sort file`|order file content|
|`sort -k 2 file`|order file content using as reference second word|
|`cut -d ' ' -f 1 file`|print first word of each line. Delimeter will be space |
|`cut -d ' ' -f 1,3 file`|print first and third word of each file. Delimeter will be space |
|`cat file`|print file content|
|`tail file`|print the last 10 lines |
|`tail -n 5`| print last 5 file lines |
|`tail -f file`| print last 10 file lines and append. Useful to monitor log files|
|`head file` | Print first 10 file lines |
|`head -n 2 file` | Print first 2 file lines|
|`tr SET1 SET2` | translate set of characters one to set of characters 2
|`cat file \| tr test sub` | It will replace all occurrences of test with sub |
|`cat file \| tr -s ' '` | It will replace all consecutive occurrences of space with one space |
|`file namefile`| print the type of namefile |

#### vi editor

vi visual display editor
vim visual display editor improved

This is the command mode editor for files. Other editors in linux are emacs, gedit

vi editor is most popular 

It has 3 modes :

1 command mode <br>
2 Insert mode <br>
3 Extended command mode

**Note** when you open the vim editor, it will be in the command mode by default.

- in the command mode the cursor's can be used as h/l/k/i to move cursor left/right/up/down

**Insert Mode:**
|command | Description |
| --- | --- |
|i | To begin insert mode at the cursor position |
|I | To insert at the begining of the line|
|A | To append at the end of the line |
|a | to apppend at the next word's letter |
|o | To insert new line below the cursor position |
|O | To insert new line above the cursor position |
**command mode**

|command | Description |
| --- | --- |
|gg | To go to the begining of the page |
|G | To go to the end of the page |
|w | To move the cursor forward, word by word |
|b | To move the cursor backward, word by word |
|nw | To move the cursor forward, word by word |
|nb | To move the cursor backward, word by word |
|u | To undo last change (word) |
|U | To undo the previous changes (entire line) |
|yy | To copy a line |
|nyy | To copy n lines (5yy or 4yy) |
|P | To paste line below the cursor position |
|p | To paste line above the cursor position |
|dw | To delete the word letter by letter (like backspace) |
|x | To delete the word letter by letter (like DEL key) |
|dd | To delete entire line |
|ndd | To delete n no.of lines from cursor position (5dd) |
|/ | To search a word in the file |

**Extended mode :**
- Extended mode is used for save and quit or save without quit using "ESC" key with ":"

|command | Description |
|--- | --- |
|ESC+:w   | To save the changes |
|ESC+:q | To quit (without saving)|
|ESC+:wq | To save and quit |
|ESC+:w! | To save forcefully|
|ESC+:wq! | To save and quit forcefully |
|ESC+:x | To save and quit |
|ESC+:X | To give password to the file and remove password |
|ESC+:20(n) |To go to the line no 20 or n |
|ESC+:se nu| To set the line numbers to the file |
|ESC+:se nonu | To remove the set line numbers |
- To open multiple files in vim editor
`#vim -o file1 file2` --To switch between the files use ctrl+w




#### User input output redirection
- All Unix based Operating systems provide atleat 3 different input and output channels - called `stdin`, `stdout` and `stderr` respectively.- That allows communication between a program and the environment in which it runs.
- In Bash each of this channels is numbered from 0 to 2, and takes the name of file descriptor, because it refers to a particular file. As it happens with any other file stored in the system. you can manipulate it, copy it, read it or write it .
- When bash environment is started, all three default descriptor files points to a terminal where the session was initialized. the input (stdin -0) correponds to what is typed in the terminal , both outputs -stdout(1) for traditional messages and stderr(2) for error messages - they are sent to the terminal. In fact, an open terminal in Unix based Operating system is usually itself a file, commonly stored in /dev/tty0; when a new session is opened in parallel with an existing one, the new terminal will be /dev/tty1 and so on. Therefore, initially the three file descriptor all point to the file representing the terminal in which they are executed.
- There are operator to redirect input, output and error.
  - < -redirect stdin
    - `wc < file` --Execute `wc` using the content of file as input
   - > and >> -recirect stdout
      -   `echo test > file1` -- write test in file1. The content of file1 will be replaced.
      -   `echo test >> file1` -- Append test in file1
   - 2> -redirect stderr
      - `find /proc -name "cpu" 2> /dev/null` -- find in /proc file/directory that begin with cpu and redirect all errors, like 'Permission Denied' to special file /dev/null (virtual file that discard all data)
    - |- stdout is transformed in stdin
      - `cat file | wc ` -- Use the output of `cat file` as input of WC
    - 2>&1 -redirect stderr to same place of stdout
    - All redirections can be combined
      - `find /etc -name '\*a\*' 2> /dev/null | less`

### Analyze text using basic regular expressions
- file globbing in linux

    file globbing is a feature provided by the UNIX/Linux shell to present multiple filenames by using special characters called "wildcards"  with a single file name. A wild card is essentially a symbol which may be used to substitue for one or more characters. Therefore, we can use wildcards, for generating the appropriate combination of file names as per our requirement.
    - | wild card symbol | Description | Example |
      | --- | --- | --- |
      |* | Every Character | `ls -l a*` - list of all files/directories that begin with a |
      |? | Every single character | `ls -l a?` - list all file/directories formed by two character that begin with a |
      |[ab] | list of characters | `ls -l a[ab]` --list file/directories called aa or ab |
      |[a-c] | list file/directories called aa, ab and ac |`ls -l a[a-c]` --list file/directories called aa , ab and ac|
      |**note:** wildcards can be combined | `ls -l a[a-c]*` --list all file/directories that begins aa, ab and ac |
- **grep pattern path/* **

- search pattern inside the strings of the files in path/*.  Show file name and row matching pattern
- it is no recursive and key sensitive. To have recursion -r must be added.
- pattern can be a regular expression. The regular expression must be surrounded by ' ' otherwise content could match bash globing.
- `grep -l patter path/*` --search pattern inside file in path/*. show only file name.
- `grep -lr patter path/*` --search pattern inside file in path/* and path subdirectories. show only file name 
- `grep -ilr patter path/*` --search pattern ignoring case inside file in path/* and path subdirectories. show only file name.

Regular Expression
| character | Definition | Example | Result |
| --- | --- | --- | --- |
| ^ | start of a string | ^abc | abs,abcd,abc1 |
| $ | end of a string | abc$ | abc, rasabc, 3aabc |
| . | Any character except new line | a.c | abc, acc, a1c |
|{...}| Explicit quantity of preceding character |ab{2}c | abbc |
|[...]| Explicit set of characters to match |a[bB]c | abc,aBc |
|[a-z0-9]| one lower case characters or number |a[a-z0-9]c | aac,a1c |
|(...)| group of characters | (abc)(2)| abcabc |
|* | Null or more of the preceding characters | a*bc | bc, abc, aabc, aaaabc |
|+ | one or more of the preceding character | a+bc |abc, aabc |
|? | Null or one of the preceding character | a?bc | bc, abc |
|^$ | empty string | |

- Not all regular expressions are supported by `grep`. As alternative can be used `egrep`

- sed stands for **stream editor**, which is used to search a word in the file and replace it with the word required to be in the output.

Note : It will only modify the output, but there will be no change in the original file.
|command | Description |
|--- | --- |
| `sed 's/source/target/' file` | In any row of ile, it will change first occurence of source to target, print all rows |
|`sed 's/source/target/g' file`| In any row of file, it will change all occurance of source to target. Pring all rows |
|`sed 's/source/target/gI'`|In any row of file, it will change all occurrences of source to target. Ignore case = case insensitive. Print all rows|
|`sed '10s/source/target/' file`| for row 10, it will change first occurance of source to target. print all rows |
|`sed -n 's/source/target/p'`|In any row of file, it will change first occurrence of source to target. Print only changed rows |
|`sed -n '/source/p' file` | It will print only rows that contain source <br> It is equal to grep source file |
|`sed -n 2,4p file` | it prints rows from 2 to 4 |
| `sed '/source/d' file`| It deletes rows with source |
|`sed -n 12d file`| Delete row 12 |
|`sed '11innewline' file`| It will insert newline as line 11 |
|`sed -i 's/source/target/g` file`| In any row of file, it will change all occurences of source to target. save result to file |
|`sed -i.orign 's/source/target/g' file`| In any row of file, it will change all occurences of source to target. save result to file but keep an copy of original file with name file.orign |

#### Archive, backup, compress, unpack, and uncompress files
`tar` save many files into a single file
- file permissions are maintained by default onlly for file users. For other user i must explicit say to maintain permission during decompression using `-p` parameter.

|command | Description |
|--- | --- |
|`tar gnc file.tar.bz2 *`| save all files of current directory in new bzip2 compressed file called file.tar.bz2 |
|`tar gnc file.tar.bz2` | Extract content of file.tar.bz2 |
|`tar tf file.tar`| show content of file.tar. note : the file.tar isn't compressed |
|`tar --delete -f test.tar file`| Delete file from test.tar Note : the test.tar isn't compressed |
|`tar --update -f test.tar file` | update file in test.tar. Note: the test.tar isn't compressed |
|`tar X<(command that generate list) -c -f file.tar *` <br> `tar X<(ls | filee -f - | grep -i MPEG | cut -d: -f 1) -c -f file.tar * ` | Exclude file MPEG from content of file.tar |
|`dd if=/dev/sda of=/system_images/sda.img`|:-- Backup a device <br> device must be unmounted |
|`dd if=/system_iimages/sda.img of=/dev/sda` | Restore device |
|`rsync` it is used to keep synchronized the content of two directories | |
|`yum -y install rsync` | install rsync command |
|`rsync -av source dest` | synchronize source with dest `-a` archive , provide a series of default option |
|`rsync -avz /tmp user@123.123.123.123:/dest`|Synchronize tmp with dest that it's contained in a remote machine with IP 123.123.123.123 <br> `-z` means that content will be compressed during transfer |
|`rsync -avzhe ssh source root@remote_host:/remote_directory/`|Synchronize source with remote_directory using ssh |

### create and manage hard and soft links
![image](https://user-images.githubusercontent.com/89054489/227713415-8f667c83-c133-4cd5-a70e-4c8a13ee9286.png)

- The i-node (index node) is a data structure in a Unix-style file system that describes a file-system object such as a file or a directory. Each i-node stores the attributes and disk block location(s) of the object's data.

- File-system object attributes may include metadata (times of last change, access, modification), as well as owner and permission data.

- Directories are lists of names assigned to i-nodes. A directory contains an entry for itself, its parent, and each of its children.

- Each i-nodes is identified by a unique i-node numbers

- To summarize: directory contains filenames, that is associated to i-node, that contains reference to data block.

Types of Files:

| Symbol | Type of File |
| --- | --- |
|- | Normal file |
|d  | Directory |
|l | Link file (shortcut) |
|b |Block file (Harddisk, Floppy disk) |
|c | Character file (Keyboard, Mouse) |

symbolic link : a symbolic link (also symlink or soft link) is a file whose purpose is to point to a file or directory (called the "target") by specifying a path thereto.

There are two types of links : 
|soft link | Hard link |
| --- | --- |
|size of link file is equal to no.of characters in the naem of original file | size of both files is same |
|can be created across the partition | can't be created across the partition |
| Inode number of source and link file is different |Inode number of both files is same |
|if original file is deleted , link is broken and data is lost | if original file is deleted tehn also link will contain data |
|it is a short cut file| it is a backup file|
|creation of symbolic link : `ln -s <source file> <destination file>` | creation of hardlink: `ln <source file> <destination file>` |

### file permissions
**Permissions are applied on three levels:-**

- Owner or User level
- Group level
- Others level

Access modes are of three types:-
 - r read only
-  w write/edit/delete/append
-  x execute/run a command

Access modes are different on file and directory:
| Permissions |Files | Directory |
| --- | --- |
|r | Open the file |'ls' the contents of dir |
|w | Write, edit, append, delete file| Add/Del/Rename contents of dir |
|x | To run a command/shell script | To enter into dir using 'cd' |
`[root@ec2-user ~]# ls -l charanfile` <br> `-rw-r--r--, 1 root root 0 mar 28 09:21 charanfile` <br>filetype+permission,links,owner,group name of the owner, size in bytes
Filetype+permission, links, owner, group name of owner, size in bytes, date of modification, file name

Permission can be set on any file/dir by two methods:-<br>
1 Symbolic method (ugo)<br>
2 Absolute methods (numbers)<br>

**symbolic method (ugo):**
- General form of symbolic mode is `# chmod [who] [+/-/=] [permissions] file`<br> who --> To whom the permissions to be assigned. <br> user/owner (u); group (g); others(o)
- Assigning different permissions to the file (user=rwx, group =rw and others=r) <br> `chmod u=rwx,g=rw,o=r charanfile`

- Assigning full permission to the file i.e; rwx to all `chmod ugo=rwx <file name>`
|command | Description |
|--- |--- |
| `chmod u+x charanfile`| Adding execute permission to user only |
|`chmnod go-wx charanfile`| Removing write and execute permissions from group and other |
|`chmod go+wx charanfile`| Adding write and execute permissions from group and other |
|`chmod go=r charanfile`| Giving only read permission to group and other |
**Absolute methods (numbers) ** :

In absolute method we use numbers instead of using symbols i.e;
- Read=4
- Write=2
- Execute=1

- Assigning different permissions to the file (user=rwx, group=rw and others=r ) `chmod 784 charan file`(where 7 means rwx i.e; 4+2+1, rw=6 i.e; 4+2 and 1 indicate x)   
- Assigning full permission to the file i.e; rwx to all `chmod 777 charanfile`
- Removing all permissions from others `chnod 770 charanfile `(where 0 indicates no permission)

**All the above permissions and procedure is same for files and directories**
**umask **
- when we create any file using touch, cat or vi commands. They get created with default file permissions as stored in umask(user file creation mask). **umask is a 4 digit octal number which tells unix which of the three permissions are to be denied rather than granted**. umask will decide that what should be the default permissions for a file and directory when it is created .

**The default umask value is 0022**
- for any file by default there is no execute permission.The maximum full permission for a file at that time of creation can be 666, whereas a directory can have full permissions i.e; 777 

**Advanced permissions **

There are other special permissions that can be granted to file/directories
|| file | Directory |
| --- | --- | --- |
| suid (4) | Run as owner of file | N/A |
| sgid(2) | Run as group owner | Inherit directory group when a file is created |
| sticky bit(1) | N/A | A file can be deleted only by owner or by directory's owner |

Suid: When a file with setuid is executed, the resulting process will assume the effective user ID given to the owner class. This enables users to be treated temporarily as root (or another user). E.g passwd has suid setted

Sgid: When a file with setgid is executed, the resulting process will assume the group ID given to the group class

Sticky bit is applied to /tmp

Suid cannot be applied to Bash scripts

**Relative Mode :**
- `chmod u+s file` set suid
- `chmod g+s file` set guid
- `chmod +t dir` set sticky bit

### Read and use system documentaion

| command | Description |
| --- | --- |
|`command --help`| show help of a command<br> `man -k keyword` search a manual for provided keywork <br> `sudo mandb` create database used by `man -k` command|
|`/usr/share/doc`| it contains configuration file examples |
|`info command`|it shows info document|
|`yum -y install bash-completion`|Must be installed for bash completion.|

### Manage access to the root account

- `root` is the system administrator
- when logged as root, shell prompts `#` character. Otherwise `$`
-`su` used to become root. It will continue to use the current session with user and group id substituted.
  - it will ask root password
 -`su -`used to become a root. It is same as logging into a fresh session on terminal
  - It will ask root password
 - `su - user` login as user
  - it will be required user password
  - if command is executed by root, password won't be required
 - `sudo` command to allow an ordinary user to execute commands as a different user (usually super user)
 - In default configuration, group `wheel` is authorized to act as root. if a user is member of `wheel` can execute all command as root with this syntax:
 
 `sudo command` user password must be provided.
 `usermod -aG wheel username` -- To add user to the wheel group
 `vi sudo` To modify the sudo configuration
 
- Basic configuration:
- demo ALL=(ALL:ALL) ALL​ The first field indicates the username that the rule will apply to.
- demo ALL=(ALL:ALL) ALL​ The first "ALL" indicates that this rule applies to all hosts.
- demo ALL=(ALL:ALL) ALL​ This "ALL" indicates that user demo can run commands as all users.
- demo ALL=(ALL:ALL) ALL​ This "ALL" indicates that user demo can run commands as all groups.
- demo ALL=(ALL:ALL) ALL​ The last "ALL" indicates these rules apply to all commands

`sudo -u user command` To execute a command with the identity of user
- if `-u` is not specified, this means that command will be executed as root.
`sudo su -` To open running root session

`%users localhost=/sbin/shutdown -h now` here % indicate group . The users in group users can execute command  /sbin/shutdown -h now on local host as root
- `Cmnd_Alias SOFTWARE =  /bin/rpm,/usr/bin/up2date,/usr/bin/yum` - To simplify configuration in sudo configuation can be used alias.

SOFTWARE  can be used in sudo configuration rows.


### Booting procedure and kernel parameters

press the power button on your system and after few moments, you can able to see the linux prompt

Have you ever wondered, what happens behind the scenes from the time you press power button until linux prompt will appear ?

The following are the 6 high level stages of a typical linux boot process

| Process | function |
| --- | --- |
|BIOS | Basic input/output system executes MBR |
|MBR | Master boot record execute GRUB |
|GRUB | Grand Unified boot loader executes kernel |
|Kernel | Kernel executes /sbin/init |
|init | It executes run level programs |
|Run level | Run level programs are executed from /etc/rc.d/rc*.d/|

1. BIOS

- BIOS stands for Basic input/output system
- Performs some system integrity checks
- Searches, loads, and executes the boot loader programs
- It looks for boot loader in floopy, cd-rom or harddrive. You can press a key (typically F12 or F2, but it depends on your system ) during BIOS startup to change the boot sequence
- Once the boot loader program is detected and loaded into the memory, BIOS gives the control to it.
- So, in short BIOS loads and executes the MBR Boot Loader

2. MBR

- MBR stands for Master Boot Record
- It is located in the first sector of the bootable disk. Typically /dev/hda or /dev/sda
- MBR is less than 512 bytes in size. This has three components 1) Primary boot loader info in 1st 446 bytes 2) Partition table info in 64 bytes 3) mbr validation check in last 2 bytes
- It contains information about GRUB(or LILO in old systems)
- So, In simple terms, MBR loads and executes GRUB loader

3. GRUB
- GRUB stands for Grand unified bootloader
- If you have multiple kernel images installed on your system, You can choose which one to be executed.
- GRUB displays a splash screen, waits for few seconds, if you don't enter anything it loads the default kernel image as specified in the grub configuration file
- GRUB has the knolwedge of file system
- GRUB configuration file is /boot/grub/grub.conf (/etc/grub.conf is a link to this)
- Inshort, GRUB just loads and exeecutes kernel and initrd images

4. Kernel

- mounts the root file system as specified in the   "root=" in grub.conf
- Kernel executes the /sbin/init program

Since, init was the first program to be executed by linux kernel, it has process id (PID) of 1. Do `ps -ef | grep init` and check the pid.

- initrd stands for initial RAM Disk
- Initrd is used by kernel as temporary root file system until kernel is booted and real root file system is mounted. It also contains necessary drivers compiled inside, which helps it to access the hard drive partitions, and other hardware.

5 init

- looks at the /etc/inittab file to decide the linux run level
- Following are the available run levels
    - 0-halt
    - 1-single user mode
    - 2-Multi user mode
    - 3. Full multiuser mode
    - 4. unused
    - 5. X11
    - 6 reboot
- Init identifies the default initlevel from /etc/inittab and uses that to load all appropriate program
- Execute `grep initdefault /etc/inittab` on your system to identify the default run level
- If you want to get into trouble, you can set the default run level to 0 to 6. Since you know what 0 and 6 means, probably you might not do that
- Typically you would set the default run level to either 3 or 5

6 Runlevel programs

- when linux server is booting up, you might see various services getting started, for example, it might say "starting sendmail... ok". Those are the run level programs, exactly executed from the run level directory as defined by your run level.

| command | Description |
| --- | --- |
| `uname -r` | To see the version of the kernel use |
| `uname -a` | To see samething as above but with more details |
|`arch` or `uname -m `| To check the architecture of the o/s |
|`cat /etc/release* `| To check the version of o/s in the system |
|`lsmod` | To list all the currently loaded modules |
|`lsmod |grep -i module-name`| To check whether a particular module is loaded or not |
|`modprobe -r <mod name>` | To remove the loaded module |
|`modprobe <mod name>`| To install /re-install a module |
|`modinfo <mod name>`| To see the information about the module |
|`lsmod |grep -i usb`| To disable USB/CD-ROM drive driver, first check whether a driver is loaded or not |
