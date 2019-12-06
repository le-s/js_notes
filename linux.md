# linux notes

## General
- Linux is not Unix
- Linux is an OS; some of the fastest computers run on some part of Linux

## Directory Structure
### Root Directory
- ROOT 
  - Administrator of windows
     - can read write or run any program
- BIN 
  - contains essential command binary 
- SBIN
  - contains essential system binary
- ETC 
  - contians configuration files like password and shadow which have your account information
- HOME
  - contains user's home dir
- LIB (Library)
  - contains common libaries used by the system
- MNT (Mount)
  - any temporary file systems like a UBS drive come under mount directory
- PROC (Procedure)
  - contains virtual file system
- TMP (Tempoary(
  - contains temporary data; gets deleted when you reboot your system
= USR
  - contains user program and other data
- VAR
  - where system must be able to write during operation; like system logs

## Reading command lines
### Account
- $ and #
  - $ means you're logged in as a normal user
  - # means you're logged on as a root user
- su or su {login name} (super user)
  - will prompt you to enter a password
  - use this command to switch between users
- whoami
  - to check what type of user you are or who you're logged in as
- passwd OR passwod {user account}
  - change pw of login
- id
  - show you user id  

## Ubuntu
### CLI Commands
- pwd command: print working directory/shows your current directory
```shell 
pwd
```
- ls command: list contents of current directory
```shell 
ls
```
- ls -a command: will show you hidden files
- cd command: use for navigation between directories and folders
```shell 
cd
```
- cd .. takes you back a directory
- cd / takes you to the root directory
- cp command: copies a file in the same directory under a new name
```shell
cp test testcopy
```
- to copy a file to a different directory
```shell
cp test /home/user/Downloads
```
- rm command: remove or deletes a file
```shell 
rm
```
- mkdir command: creates a new folder
```shell
mkdir NewFolder
```
- rmdir command: deletes folder only if folder is empty
```shell
rmdir NewFolder
```
- rm -r {folder name} command: to delete non empty folders
```shell
rm -r NewFolder
```
- man {command} command: gives you information about a command (press Q to quit)
```shell
man ls
```
- locate {filename} command: will locate any file within the system and show you where the file location is stored
- gedit {filename} command: will open a text editor for you to edit that particular file
- cat {filename} command: will display the contents of the file onto the terminal
- less {filename} command: when a file is pretty large and cannot fit the entire screen; you can go through the file one line at a time
- 'piping' command: combine two commands together
ex. will allow you to locate all files and scroll through them
```shell
locate {filename} | less
```
### Run a program
- $PATH
  - contains the list of folders that the system uses or checks when you type in a command
- ./{program name}
  - running a program
- ps aux
  -  give you all the processes running on your computer
- When a program is running
  - pressing CTRL-C will terminate the program
  - pressing CTRL-Z will pause the program; shifts to the background
- bg  
  - will show you programs in the background
- jobs
  - see if all programs are running correct in the background and their status
- fg {job number}
  - run program again

## Interview Questions
