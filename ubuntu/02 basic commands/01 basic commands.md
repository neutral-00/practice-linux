# Basic Commands

## Shutdown And Reboot
- poweroff command issues: shutdown -h
- reboot command issues: shutdown -r
- example: $ sudo shutdown -h 10:00 "shutting down for scheduled maintenance"
- will schedule a shutdown at 10:00 am.

## Locating Programs
- normally executible programs and scripts should live in 
- /bin, /usr/bin, /sbin, or somewhere under /opt or /usr/local/bin or /usr/local/sbin or user account space like /home/student/bin
- if you find out where the diff program resides in the file system type: which diff
- if which doesn't find whereis is a good alternative. It searches in brodader range of system directories
- type: whereis diff
- assignment : find where the ip utility program resides?

## Accessing Directories
- normally home is the default directory in the terminal
- you can find by: $ echo $HOME
- some revelant commands in directory navigation
	- pwd : displays present working directory
	- cd ~ : change directory to home directory
	- cd .. : change directory to parent directory
	- cd - : change directory to previous working directory
	
## Absolute And Relative Paths
- absolute path name begins with the root directory i.e. /
- and follows the tree, branch by branch until it reaches the desired directory or file.
- relative path starts with present working directory
- extra slashes in the path are ignored by the system
- ///usr//bin is allowed and seen by the system as /usr/bin
- you can use shortcuts: . is present working directory, .. is parent directory, ~ is home.


## Exploring The File System
- use tree command to get a bird's eye view of the file system
- add -d to list just the directories
- hidden files and directories starts with .
- here are some of the commands to view directories
	- ls : list the contents of the present working directory
	- ls -a : list all contents including hidden ones
	- tree : displays a tree view of the file system
	
- to see the directories and its contents you can use: df -h
- -h means give the size in human terms.


## Hard Links And Soft Links
An easy way to create a shortcut from your home directory to long pathnames is to create a symbolic link.

Unlike hard links, soft links can point to objects even on different filesystems, partitions, and/or disks and other media, 
which may or may not be currently available or even exist. In the case where the link does not point to a currently available 
or existing object, you obtain a dangling link.

## Navigating the Directory History
The cd command remembers where you were last, and lets you get back there with cd -. 
For remembering more than just the last directory visited, use pushd to change the directory instead of cd; 
this pushes your starting directory onto a list. Using popd will then send you back to those directories, 
walking in reverse order (the most recent directory will be the first one retrieved with popd). 
The list of directories is displayed with the dirs command.