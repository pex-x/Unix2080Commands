## Terms discussed in class:
**Main Idea of Open Source** 
The main idea behind open-source is to allow users to see the code they trust for their workflow.

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

## Intro Commands
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

``ps`` - A command that shows processes that are executing in the system.
Manual Page: https://man7.org/linux/man-pages/man1/ps.1.html
-  Basic Syntax: ``ps``

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


## Basic Commands for VIM
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

Start Of Line: ``0``  

End Of Line: ``$``  

**You must be in Command Mode to run these commands.**

Write: ``:w`` OR ``:w NAME_OF_FILE`` (if first time saving.)  

Quit: ``:q`` OR ``:q!`` OR ``:qa!``  

Line Number: ``:set nu``  

Search Text: ``/WORD_TO_SEARCH``

https://vimsheet.com/

### Midterm Prep
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

**What is a Cloud System:**
A virtualized computer that operates over the internet to provide computing services.

**How does AWS provide us something without Privacy Issues?**
- Virtualized Cloud Partition, Memory Isolation, Disk Isolation, Secure Communication Protocols for Users, and device encryption.

**What is SSH? How does it relate to remote/cloud computing?**
- Secure Shell. A protocol for communication with a remote computer system.
	- Some Examples: PuTTy, OpenSSH.

**Virtual Memory:**
Virtual Memory is an Abstraction for the main memory which is a scrambled memory block that contains Page Frames, and extends the main memory space. When main memory is full, Overloading is an issue, but swapping and virtual memory is the solution.
	- Swapping it takes the entire memory block related to a process and puts it in the disk.
	- Virtual Memory slices the memory into Pages (Fixed size block of memory that can pick up or store in disk if needed.)

**Process:**
- Process comes with a PID. A process is identified with a PID, and with permissions, a GID, and UID. GID and UID are inherited from the User Profile that is executing the commands. If the process creates another process, it inherent from its parent process.
- Inside of Virtual Memory, and Processes, they are stored in the Address Space.
- The GID, UID, PPID, PID, and Address Space is stored in the Process Control Block (PCB).

**IPC:**
- Pipes, Message Queues, Shared Memory, Semaphores.
- Pipes are where the exam focuses the most on. Pipes are:
	- Unstructured: A stream of data. (As opposed to MQ)
	- Uni-Directional: If P1 has to communicate with P2, P1 Writes, P2 Reads.

**What the Shell?** 
BASH, or Shell, is the interpreter of commands from the Terminal. Session Variable is specific to one instance of a terminal, an Environment Variable will not inherent all  Session Variable.
- ``export var="Something"``
- Options are long short.

**What is an OS?:**
An OS is an abstraction of the computer hardware. It manages the system
resources and provides an interface for end users to interact with the system without
knowing the specific implementation details

**What is the difference between a kernel module and a user program?**
A kernel module works in the kernel space and interacts with the hardware
directly. On the other hand, the user program does not have direct access to the hardware, and it
uses OS services by requesting the kernel for specific services through system calls. An end user
generally interacts with the user program only and does not need to know or interact with the
kernel modules directly

**What is Epoch Time?**
The midnight of January 1, 1970, is an important date for system engineers, and it is
known as the UNIX epoch time. This date was picked as the start of time in UNIX
systems, and all the time calculations in UNIX are based on the number of seconds
elapsed from the epoch. 