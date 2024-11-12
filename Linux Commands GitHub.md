## Terms discussed in class:
**Operating System**: The OS is a resource  
manager, software that sits between the user and the hardware, the housekeeper of the machine,  
or an extension of the hardware.

**Process**: A process is formally described as an executing program, process inherits a UID.

**UID**: The User ID. Each User has one as an identifier

**Group**: Grouping Users with separate permissions.

**Superuser**: The highest group users can be a part of! 

**BASH**: The Bourne Again Shell, the most common shell flavors.

**Shell**: A Shell is the interpreter in UNIX that allows programming a set of actions. The Shell is accessed through the Command Line Interface. 

**Session**: A session in a Terminal Application, is an instance of the terminal program. They are isolated from one another.

Cloud: A network of computers that allows users the freedom to not have a single point of failure.
## Basic Commands:
``cd``  - Changes directory, you can use this to traverse almost anywhere on the filesystem.
Manual Page: https://man7.org/linux/man-pages/man1/cd.1p.html
- ``cd DIRECTORY`` > Moves into this directory.
- ``cd ..`` > Moves back a directory.
- ``cd /etc/ssh/ssh_config.d/`` > Moves into ssh_config.d directory

``ls`` - Lists the files within a specific directory. 
Manual Page: https://man7.org/linux/man-pages/man1/ls.1.html
- ``ls`` > shows files in your Current Working Directory.
- ``ls -la`` > shows all files, including hidden ones, with their permissions.
- ``ls -a`` > shows all files, without permission types.
- ``ls -la`` /home/user > shows all files in the /home/user directory.

``clear`` - Clears the whole terminal
Manual Page: https://man7.org/linux/man-pages/man1/clear.1.html
- Basic Syntax: ``clear``

``cat`` - Prints out the contents of a file to a terminal
Manual Page: https://man7.org/linux/man-pages/man1/cat.1.html
- Basic Syntax: ``cat FILENAME``

``sudo`` - Acts as root, not root. Allows different commands to be run.
Manual Page: https://man7.org/linux/man-pages/man8/sudo.8.html
- Basic Syntax: ``sudo apt update``

``less`` - prints first 10 lines of a file.
Manual Page: https://man7.org/linux/man-pages/man8/sudo.8.html
- Basic Syntax: ``less FILENAME``

``grep`` - Grabs Text
Manual Page: https://man7.org/linux/man-pages/man1/grep.1.html
- Basic Syntax: ``grep TEXT FILENAME``

``cp`` - The Copy Command. Copy's content of file into another location/file.
Manual Page: https://man7.org/linux/man-pages/man1/cp.1.html
- Basic Syntax:  ``cp Nicholas.txt Nicholas2.txt``

``rm`` - Removes a file.
Manual Page: https://man7.org/linux/man-pages/man1/rm.1.html
- Basic Syntax: ``rm FILENAME``

``pwd`` - Prints the current directory you are in.
Manual Page: https://man7.org/linux/man-pages/man1/pwd.1.html
-  Basic Syntax: ``pwd``

``|`` - Pipe, runs commands sequentially. A special character, aka an operator. After it detects this symbol, command1 is over, command2 is then executed, and creates a pipeline as an input output.
Manual Page: https://www.redhat.com/sysadmin/pipes-command-line-linux
- Basic Syntax:  ``COMMAND1 | COMMAND2 ``

``chmod`` - Changes the permissions of a file. There are 3 categories, read write and execute, for User Group, Guest Group, and Other. This can be represented with numbers, and letters. A very complex command. 
Manual Page: https://www.man7.org/linux/man-pages/man1/chmod.1.html
- ``chmod +600 FILENAME`` - This gives read and write to user groups.
- ``chmod +r-x FILENAME`` - Read and execute permissions are applied to all groups with this command.
- ``chmod -rwx FILENAME`` - Removes permissions from all groups.


``echo`` - Can do so much! It either will put the contents of echo into a file or print the content onto the terminal.
Manual Page: https://man7.org/linux/man-pages/man1/echo.1.html
- ``echo "X" > file.txt`` > inserts X, getting rid of everything else in the file
- ``echo "X" >> file.txt``  > appends X to the existing file.
- ``echo 'blah' > example.txt | cat example.txt`` > Echo's blah into a new file, example.txt, it then opens using cat and prints content of file to a terminal.

``printenv`` - Printing environment variables for your Unix Shell
Manual Page: https://man7.org/linux/man-pages/man1/printenv.1.html
- Basic Syntax: ``printenv``

``ps`` - A command that shows processes that are executing in the system. (Particularly in the PCB)
Manual Page: https://man7.org/linux/man-pages/man1/ps.1.html
-  Basic Syntax: ``ps``

-------------------------------------------------------------------------

## VIM Basics:
There are a few modes total in Vim, Replace, Command, Insert, Normal, and Visual Mode. It all  
is fairly straightforward, as they do mostly what their names suggest.  

``Normal``: Normal is the default mode of Vim. There are commands specific to normal that we  
can execute to!  
	- ``r`` replaces characters  
	- ``x`` deletes characters  
	- ``u`` undos edits  
	Shortcut - Normal: ``ESC`` 
 
``Insert``: Characters typed in will be put on the file like a text editor.  
	Shortcut - Insert: ``i`` OR ``ESC + i``  

``Command``: Write, and exit are found here. Allows us to execute Vim Commands.  


``Visual``: Works as a highlighter, makes selections of text. 
	Shortcut - ``v`` OR ESC + ``v``  

``Replace``: Replace text by writing over it.  
	Shortcut - ``R`` OR ``ESC + R `` 

By default, Vim starts in Normal Mode.


### Basic Commands for VIM
**You must be in Normal Mode to run these commands.**
Cut: ``dd`` or ``D``. The difference is one goes to the end of line  
Copy: ``yy``
Paste: ``p`` 
Delete: ``dd`` 
Up: ``k`` OR ``Up Arrow`` 
Down: ``j`` OR ``Down Arrow``  
Sideways Left: ``h`` OR ``Left Arrow``  
Sideways Right: ``l`` OR ``Right Arrow`` 
Page Up: ``CTRL + B``  
Page Down: ``CTRL + F `` 
Top: ``gg``  
End: ``G`` 
Line Number: ``1G`` (First Line)
Start Of Line: ``0``  
End Of Line: ``$``  

**You must be in Command Mode to run these commands.**
Write: ``:w`` OR ``:w NAME_OF_FILE`` (if first time saving.)  
Quit: ``:q`` OR ``:q!`` OR ``:qa!``  
Line Number: ``:set nu``  
Search Text: ``/WORD_TO_SEARCH``

https://vimsheet.com/

-------------------------------------------------------------------------------  
## Midterm 1 Prep
OS - Operating System
OSS - Open Source Software
FOSS - Free Open Source Software
FLOSS - Free/Libre Open Source Software.
GNU - Gnu's not Unix.
PCB - Process Control Block
MMU - Memory Management Unit
CLI - Command Line Interface
AWS - Amazon Web Services
RTT - Round Trip Time
Distro - Distribution

Top Down:
**User Space:** All user Libraries Live Here. GNOME, the windowing system/GUI interface, lives here
	**Application Layer**:
		Command Interpreter: Uses Utilities, such as Libraries, Utilities, and and all other User Programs / Modules. GNU provides functionality.  I.E, BASH 
		**Library Calls** makes calls directly from the user program to Library, Util, and User Programs. AKA, deals with Libraries.
**Kernel Space**:
	**System Calls** or Sys Calls make calls by requesting something from the Kernel.
		File System, Memory Management, Schedulers, Device Drivers. These deal with the Lower Layer.
**Hardware Layer**:
		Disc, Peripherals, RAM
			Virtual Memory.

Practice VIM!

What is a Cloud System:
A virtualized computer that operates over the internet to provide computing services.

How does AWS provide us something without Privacy Issues.
- Virtualized Cloud Partition, Memory Isolation, Disk Isolation, Secure Communication Protocols for Users, and device encryption.

What is SSH? How does it relate to remote/cloud computing?
- Secure Shell. A protocol for communication with a remote computer system.
	- Some Examples: PuTTy, OpenSSH.

**Virtual Memory:**
Virtual Memory is an Abstraction for the main memory which is a scrambled memory block that contains Page Frames, and extends the main memory space. When main memory is full, Overloading is an issue, but swapping and virtual memory is the solution.
	- Swapping it takes the entire memory block related to a process and puts it in the disk.
	- Virtual Memory slices the memory into Pages (Fixed size block of memory that can pick up or store in disk if needed.)

Process:
- Process comes with a PID. A process is identified with a PID, and with permissions, a GID, and UID. GID and UID are inherited from the User Profile that is executing the commands. If the process creates another process, it inherent from its parent process.
- Inside of Virtual Memory, and Processes, they are stored in the Address Space.
- The GID, UID, PPID, PID, and Address Space is stored in the Process Control Block (PCB).

IPC:
- Pipes, Message Queues, Shared Memory, Semaphores.
- Pipes are where the exam focuses the most on. Pipes are:
	- Unstructured: A stream of data. (As opposed to MQ)
	- Uni-Directional: If P1 has to communicate with P2, P1 Writes, P2 Reads.

BASH, or Shell, is the interpreter of commands from the Terminal. Session Variable is specific to one instance of a terminal, an Environment Variable will not inherent all  Session Variable.
- ``export var="Something"``
- Options are long short.
  
-----------------------------------------------------------------------------
  
## File Systems:
**Why Use Unix?**: Customizable, familiar to developers, portable, gives more control! 

**Unix Filesystems**: You can customize, but 
different filesystems can change differently! 

**Files In Unix?**: Any stream of Data, A sequence of Bytes.

**Organized File System:** Unix has a hierarchical system, it starts from root directory, a special file partition /, /bin, /home, /usr, /bin.  

**But what is a File System?**: A data structure that manages the entire disk. An abstraction of a Disk. A Kernel Module! It does this according to Metadata of each files. 

**Directory**: Collection of File/Collection of Bytes. If you decide to vim a directory, it will treat it as a file. 

All Files have specific meta data, and Magic Numbers, which is the first few bits in Hex of the type of File.

Permissions are asking about read, write, and execute for users.

4 - Read
2 - Write
1 - Execute

**Why are Permissions Needed?:** There can be multiple users in a system, and can allow access to a specific set of files.

**How are files represented in ACLS?**: Users Groups, and Others! U, G, O 

But there isn't just R W X, there is S, which is the SUID Flag! It helps us execute file with User Permissions. 

Sticky Bits: At a directory level restricts file deletion. Only Owner can delete! 
- At a File Level, it tells OS to retain Main Memory even after it's execution is over! t is the character flag to show a sticky bit.

Super User!
- Super User or the username root has special privileges and can override any file permissions in the system. Assign them to the Sudoers group!

File Systems are implemented in Unix by: (EXAM QUESTION)
**Boot Block -> Super Block -> INodes -> Data**.

How is this defined file system defined?: The more dynamic way of doing this is the first instruction, the starting address will tell you where to go next, and the next address will tell you how big it is. Once it is given an address, it will assume its the first address of a file system and finds out what file system it is, and based on that every file system will have a conf format. Inside binary data, you will see all the metadata built into the blocks of memory, finds the size of each block, and the location of the next block. All of it is stored and parsed using a data structure, can be stored using Tree, a self balanced tree, a binary tree.


**File Systems: What is FS, How FS Work, Few Pop FS - Selecting FS**

**Functions of a File System**: Stores Data, Organizes Files, Manipulate Data, Access Control to specific types of data. 

**Size Based Categorization:** Bigger files gets priority

**Hierarchy:** Can store many different sets of Data based on boxes, inside of boxes, inside of boxes. Root would be a room to store it in, each of the nodes are smaller bins, for example, home can hold many other things. 

A filesystem also provides the how to, such as Algorithms, the file systems will have an algorithm to go through and traverse those specific boxes. Remember how we talked about trees? It will help traverse these trees algorithmically.

-rw-r--r--  1 pex pex    47 Oct  7 13:13 permissions.txt

We have our permission, then that number is a Hard Link: 
File systems are organized by Super Block, iNodes, and the data! There are two types of links, Hard and Soft. Hard Links, file1 and file2. Lets assume file1 has a hard link to file2. A hard link points to the same iNode/Data. 

Symbolic link or Soft Link is when file1 points to file2, where file2 has an iNode connected. File1 will have no content if file2 is deleted, because file2 is the only one hanging on the node. 

The issue with sym links is that if you create another file2 with the same name in the same directory, it will point to the new file regardless, this is called **Hanging Links**


Total is the number of data blocks it contains. It has a boot block, which is a basic thing of UFS. A super block (with a cape) which is the size of the entire data section, size of the iNodes, where to register data, and more (Meta Data of the entire filesystem)

iNodes are 1 to 1 mapped metadata for each file in the File System. 

The 'registry' is our iNodes. For example Device Info, INode Number, FIle Mode (Permission String), Link Count (Number of Hard Links/Pointers that point to this file to where it is located in the physical disk) , User Id, Group Id, Size, Timestamps.  

Commands: 
``stat``:  Stat will produce many different fields, but mainly the focus on creation date. A regular command looks like:
```
 File: permissions.txt
  Size: 47              Blocks: 8          IO Block: 4096   regular file
Device: 8,32    Inode: 9887        Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/     pex)   Gid: ( 1000/     pex)
Access: 2024-10-07 13:14:01.552348501 -0600
Modify: 2024-10-07 13:13:52.282353296 -0600
Change: 2024-10-07 13:13:52.282353296 -0600
 Birth: 2024-10-07 13:13:52.282353296 -0600
```
The device field will tell you the hard drive where this is stored. Inode is the pointer to the Inode Index. The Link shows the number of Hard Links. There is also our access, UID, GID, access, modify, change, when it was made, and more! Change deals with the modification of file metadata (like permissions), modify deals with the actual contents of the file.

``lsblk``:  Will list all current blocks of mem/disks.
```
NAME MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
sda    8:0    0 388.4M  1 disk
sdb    8:16   0     4G  0 disk [SWAP]
sdc    8:32   0     1T  0 disk /mnt/wslg/distro/
```
sda stands for storage device a. RM and RO stand for Read Modify and Read Only.

``lsblk -f`` will show specific info on specific types.
```
NAME FSTYPE FSVER LABEL UUID FSAVAIL FSUSE% MOUNTPOINTS
sda
sdb                                         [SWAP]
sdc                           950.7G     0% /mnt/wslg/distro
```

By default ubuntu ships with an EXT4 filesystem. The reason why you don't hit the number of files you can create, EXT4 allows unlimited subdirectories/unlimited depth.  If you have to many files, a device may run out of iNodes.

``debugfs /dev/DRIVE`` will allow you to do disk analysis on a file system.

``df -T`` does the same thing as ``logdump`` in debugfs.

``file -sL /dev/sdc`` will show other information regarding type of File System.

XFS is a journaling file system. EXT4 vs. XFS? XFS will support larger file systems (for something like Data Science) by the way the data is stored and traversed. BTRFS will be Better FS and uses B-Nodes/B-Tree File System. IMFS is a file system that is not on the disk, but entirely on the ram. If data is sensitive, you want a journaling file system.

Data At Rest: When your data is stored inside a cloud server (or multiple cloud servers) all files have to be protected. When nothing is happening with the data, how do we protect it? Encryption is the normal way, but many of the data blocks have multiple layers of encryption to avoid Single Points Of Failure. 

Life of Storage Device: Defined as the max read write cycles it can handle without data corruption. Different Algos, have different implications of the Life of SD's. For example, BTRFS will put more Read Write Cycles on your device. 

exFAT/FAT - exFAT evolved from FAT, interesting if you are working with Windows because it is one of the most portable File Systems. 

Journaling File Systems have a system called Journals, when a Data Transaction is happening inside a system, there are many middle systems, it is heavier on the RW Cycles again, and SSDs are better for any journaling file systems. 

EXT4 for many files.
EX-FAT for multiple different types of systems/portability. Problem is that it doesn't have journaling implications. 
XFS is for Data Science.

What do Cloud Systems tend to use/How do the cloud systems use these drives for many user and prevent the amount of Storage Device.

./ is a reference to a current directory. The way terminal works is it needs to know where the file is, and have an executable file. Look for a specific file name and try to execute it. 

When a command is executed it knows where in the file system is located. For example /usr/sbin/useradd is located by ``which <command here>`` which locates commands.

Commands:
``chown`` changes the owner of the file. 
``sudo -u USER`` will write using whatever user is executing the command! 
``df`` and ``lsblk`` gets all info from iNodes, basically the same thing, and ``df -T`` will show in human readable format.

File System is to keep a file organized.

-----------------------------------

**Exam Question:**
How does a user access/create FS?
Disk -> Partitions in the disk (Two types, Physical/Where Registers and shit are and Logical/A simplified version so that it is easier to access) -> File System -> and a Mount Point (Points to Logical Address) -> Mount the Filesystem -> cd into it and Mount Write.

``disk``: The disk is the physical disk, has an ID, the hardware you have, where the data is written. Physical Partitioning happens here. 
``deivce``: An abstraction on top of the disk, allows us to communicate with the disk. The user communicated with the disk through the device. Logical Partitioning happens here
``mountpoint``: Link between device and disk.
``volume``: This is also the Partition, the length of addresses, and an abstraction of a partition. Volumes also come with additional metadata. 
``partition``: Splits the disk, 2 types, Physical l/Where Registers and shit are and Logical/A simplified version so that it is easier to access. 

Syntax of Bash is no space between =, for example, loopdevname=~/blah wont execute! loopdevname = ~/blah

-----------------------------------

Virtual FileSystem vs Logical?: Virtual would be held entirely on RAM. 

For DD: ``if`` is input, ``of`` is output file. Each Block size is 1024 (1KB), 51200 (Random Num). 

``losetup`` will show the next free Loop Node. 

``loopback device`` communicates with itself! 

---------------------------------------------------------- 

## Text Stream Editing:
**What is a Stream**?: A stream is a non-segmented and not fixed length, it is also serial. 

``grep``, unlike ``sed`` is a search tool! If we need to have a search with regular expression, use grep. grep works by 
```
grep [options] [pattern] [file]
```

``awk`` is a more robust scripting interface that is based off of the c programming language.
```
awk [pattern] [file]
```

**When to use sed**?: When you have unstructured data, and each line is undefined characters, spaces, literals, and more for each line.

**When to use awk?**: When data is structured (like .csv files), data that's mapped into a row column structure, or a matrix-based structure. It also uses delimiters like commas, spaces, etc. 

Syntax of sed: ``sed [options] "[some sort of microscript / define mode]" [filename] 

**Exam Question**
sed is also a 'modal text editor'. Different modes of sed are insert, search & replace, command, delete, and print mode.

Print the 52nd Line of the File (the -n will limit to only this line aka making it quieter): ``sed "52p" [filename] -n ``

A `` `sed "52p" [filename] -n` `` will run the command in a separate bash script, and it will evaluate in our terminal.

----------------

For loop in bash: ``for i in {1..1024}; do echo "hay" >> haystack; done``

``

CS2080: Bash
Creating Users, Files, Creating files in filesystems.

Discussed 2- 3 Important Things:
#!/usr/bin/env bash
Copyright Notice
#* Means Comment.

File Operations, how we can use all the file operations, using a loop, invoking a variable. Invoke a variable of an array. Used For Loops

All Scripts are in scope, don't copy.
Use while loop

varName="something"
If there was spaces, shell would interpret as command. "" Interprets as a string.

which bash will tell you where the shebang goes

echo ${varName}
echo "Here is the Val: ${varName}"

echo "Here is the Directory: $(pwd)"

The use of special symbols to manipulate the variables is called shell expansion. Interpreted as command.

```bash
printit(){
    echo "my name is $1" #Taking the first parameter passed
    echo "Our names are  $*" #Taking all parameters
}
printit alice bob
```

**Version Control:** Git is the most popular one, authored by the same person who wrote the first Linux Kernel. 

**Source Code:** Strings/Programs that is capable of running in an isolated individual system as long as the dependences are met, image files are okay with this definition

**Repository (Repo)**: A repo is a place where you put many source code, can store versions, changelog, and more. Shared and Distributed. Can fork the repository without dealing with the initial branch it was taken from. A really good place for source code.

**Diff between repo and directory?**: You give people permission through ACLs in Directories. For Repos, each node that has access to the Repo, has entire control, and this is called a local copy.

The server plays an important part. A repo may or may not be linked to a server. Github, BitBucket, GitLab are all examples of this type of server. Git is interpreted by Git Version Control Software, all the servers run git servers behind them and run all related commands. 

**Upstream:** The original or main reference of a repository, often the first instance of a repo. Generally put into a server, and this upstream node will be where machines copy it from. The other nodes that copy it are called downstream nodes.

**Check In/Out (Fork?):** Making your own local copy of a file. You check out from a repository, and you check in from a repository. Check In is **Pushing**, Check Out is **Pulling** Downstream.

Make Change -> Check In/Commit -> Push the Changes only -> Check Out (Pull New Changes)

**Fork:** Relates to the server only. A server function/feature. Checks Out, Pulls, and copy's the version of the repo. Allocating own copy of an upstream in the server. Allocate write permissions, these are requirements for pushing changes into remote repo.
 
**Delta:** The change in a repo. (Triangle)

**Remote:** Uploaded, becomes upstream, can be on Github, and then allow users to copy.

**Local:** Local On you machine. Called Downstream. Make change here, then you check it in, to your local, then you **PUSH** to the remote repo. Anytime we check in or check out, we only deal with the "change"

**Pull:** Deals with only the changes.
**Merge:** Adds changes, and change metadata. Contains Authorship, Related Comments, Timestamps, and more! 

Don't push into Mirror Repo. Mirror Repos act as a median, read only.

**Fetch:** Pulls the changes since the last pull.

Licenses:
**No Blanket Licenses** instead **Make a License for each file**
**Year/Time** make sure that all the years line up, and include death! 
**Restrictions** mention any additional ones, and use them if need be. 
We can do GPL with exceptions!