# The Command Line


## Command Line Basics

* A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.
* The shell: Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called bash which stands for Bourne again shell.
* I confirmed that the shell I am using is zsh (Z shell), but typing the following command into my terminal: echo $SHELL.
  * [Z shell background](https://en.wikipedia.org/wiki/Z_shell): The Z shell (Zsh) is a Unix shell that can be used as an interactive login shell and as a command interpreter for shell scripting. Zsh is an extended Bourne shell with many improvements, including some features of Bash, ksh, and tcsh.
* Shortcut: When you enter commands, they are actually stored in a history. You can traverse this history using the up and down arrow keys. 
  * So don't bother re-typing out commands you have previously entered, you can usually just hit the up arrow a few times. 
  * You can also edit these commands using the left and right arrow keys to move the cursor where you want.


## Basic Navigation

* Basic commands:
  * *pwd* -- Print Working Directory - ie. Where are we currently.
  * *ls* -- List the contents of a directory.
  * *cd* -- Change Directories - ie. move to another directory.
* Two types of paths:
  * Relative path: a file or directory location relative to where we currently are in the file system.
  * Absolute path: a file or directory location in relation to the root of the file system.
* Paths highlights:
  * . (dot): This is a reference to your current directory, e.g. ./Documents would specify that you are currently in Documents.
  * .. (dotdot)- This is a reference to the parent directory. You can use this several times in a path to keep going up the hierarchy. eg if you were in the path /home/ryan you could run the command ls ../../ and this would do a listing of the root directory.
* Shortcuts:
  * cd / ~:  If you run the command cd or ~ without any arguments then it will always take you back to your home directory.
  * Tab completion: When you start typing a path (anywhere on the command line, you're not just limited to certain commands) you may hit the Tab key on your keyboard at any time which will invoke an auto complete action. 


## More About Files

* file: obtain information about what type of file a file or directory is.
  * In other systems such as Windows the extension is important and the system uses it to determine what type of file it is. 
  * Under Linux the system actually ignores the extension and looks inside the file to determine what type of file it is. 
  * So for instance I could have a file myself.png which is a picture of me. I could rename the file to myself.txt or just myself and Linux would still happily treat the file as an image file. As such it can sometimes be hard to know for certain what type of file a particular file is.
  * Luckily there is a command called *file* which we can use to find this out.
* file[path]
  * Why is the command line argument above specified as a path instead of file.
  * Whenever we specify a file or directory on the command line it is actually a path.
  * Also because directories are actually just a special type of file, it would be more accurate to say that a path is a means to get to a particular location in the system and that location is a file.
* Spaces in names, e.g. a directory name of *Holiday Photos*:
  * Can be handled with quotes: cd 'Holiday Photos'
  * Can be handled with an escape character: cd Holiday\ Photos
* ls -a: list the contents of a directory, including hidden files.
* Everything is a file under Linux, even directories.
* Linux is an extensionless system -- files can have any extension they like or none at all.
* Linux is case sensitive -- beware of silly typos.


## Manual Pages

* man pages are your friend -- instead of trying to remember everything, instead remember you can easily look stuff up in the man pages.
* man <command>: Look up the manual page for a particular command.
* man -k <search term>: Do a keyword search for all manual pages containing the given search term.
* /<term>: Within a manual page, perform a search for 'term'.
* n: After performing a search within a manual page, select the next found item.


## File Manipulation

* mkdir: Make Directory - ie. Create a directory.
* rmdir: Remove Directory - ie. Delete a directory.
* touch: Create a blank file.
* cp: Copy - ie. Copy a file or directory.
* mv: Move - ie. Move a file or directory (can also be used to rename).
* rm: Remove - ie. Delete a file.


## Cheat Sheet

* [Link to Linux CLI Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
