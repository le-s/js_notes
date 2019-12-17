# linux notes

## General
- Linux is not Unix
- Linux is an OS; some of the fastest computers run on some part of Linux
- Command line is also known as shell
- root has two meanings
  - the directory
  - the user access

## Reading a file
- rwxrwxrwx
  - first rwx means user that owns the file
  - second rwx means the group that ownss the file
  - third rwx means all other users that are not in the group that owns the file
- rwx
  - r: read => see contents of file but not make changes
  - w: write => can make changes but not read file
  - x: execute => someone can run the file without loading the script into another program
### Setting file permissions
- chmod command
  - ex. chmod 644 test.sh ; chmod a-x test.sh
  - two methods to change: octal and symbolic
    - octal
      - read => 4
      - write => 2
      - execute => 1
      ex. 777 => all users have read write execute permission; 755 => user has all permissions, group & other has read and execute permission; 644 => user has read and write permission, group and other has read permission; 700 => user has all permission, group and other have no permission
    - symbolic
      - u => user
      - g => group
      - o => other
      - a => all
      - + => adds permission
      - = => adds specific permission but removes all others
      - - => removes permission
      ex. u+rwx => adds all permissions to user; g=r => adds read permission to groups, but removes write and execute permission; o-rwx => removes all permissions to others
        
## Links
- Hard Link => points to data on the disk
  - command ln (file name) (new file name)
  - can move files around and holds reference
- Soft Link => points to a file on the disk
  - command ln -s (file name) (new file name)
  - if you move either or files, the link will break
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

## Searching texts in a file
- grep command
- use grep -E for RegEx

## Manipulate text
- awk command => 

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
- chown => change ownership of file
- apropos {"description of command" in quotations} => returns possible commands that describe the description provided
  - ex. apropos "list"
- sudo ls /root => to gain access to root user * will give you access to super user priveleges temporarily
  - sudo -k => to give up priveleges 
  - sudo -s => gives you super user privs until you give it up
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
### How can you see which kernal version a system is currently running?
- uname command => prints out system information
  - uname -a => prints all system info
### How can you check a current system's ip address?
- old way: ifconfig
  - look for inet for ip address
- new way: ip addr show
  - can be more specific and do command: ip addr show eth0
### How do you check for free disk space?
- df (display free)
  - df -ah => display all human readable
    - to see how much is available; see what is mounted to the root "/"
### How do you manage services on a system?
- old way(system c) => command: service {service name} argument
  - service name could be udev, nginx, mysql
  - ex. service udev status ; service nginx start
- new way(system d) => command: systemctl argument {service name} 
### How would you check the size of a directory's contents on disk?
- command: du -sh {directory name} 
  - du => disk usage
### How would you check for open ports or listening network sockets or service listening on tcp or udp ports or sockets?
- command: netstat 
  - netstat -tulpn => for most cases
### How do you check CPU usage for a process?
- command: ps aux | grep {process name}
  - ex. ps aux | grep nginx
- command: top or htop
### Dealing with mounts (like plugging in usb stick)
- command: mount {absolute path to} {mount point}
  - ex. mount /dev/sda2 /mnt
  - mount command will check for existing mounts
### How do you look up something you don't know?
- commmand: man
### What do you do when you can find something using man?

## About Nginx
- Nginx uses Master-Slave architecture by supporting event driven, asynchrous and non-blocking model
- Features
  - ease of installation/maintainence
  - Improves performance
  - Scalable
  - Reduces wait time for users
  - Load balancing
  - upgradable

## Configuring Linux servers Nginx
- all configuration files are located in /etc/nginx/
  - main config file is /etc/nginx/nginx.conf
  - configuration options are called directives
  - directives are organized into groups called blocks or contexts
- http block
  - contain directives for handling web traffic
  - contains a 'include' directive which tells NGINX where the website configuration files are located 
    - file contains the SERVER block
- server block
  - listen directive => tells NGINX the hostname IP and the TCP port where it should listen for HTTP connections
