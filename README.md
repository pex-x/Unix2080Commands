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
