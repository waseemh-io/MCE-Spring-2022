# Notes #2
Topics to Cover:
- Introduction to operating systems
- Linux file system and directories
- Important linux commands
- The Internet and Networking
	- TCP/IP - HTTP

### Introduction
An Operating System (OS) is an interface between a computer user and computer hardware. An operating system is a software which performs all the basic tasks like file management, memory management, process management, handling input and output, and controlling peripheral devices such as disk drives and printers.

Some popular Operating Systems include Linux Operating System, Windows Operating System, VMS, OS/400, AIX, z/OS, etc.

### Definition
An operating system is a program that acts as an interface between the user and the computer hardware and controls the execution of all kinds of programs.

Conceptual view of an Operating System
Following are some of important functions of an operating System.

		Memory Management
		Processor Management
		Device Management
		File Management
		Security
		Control over system performance
		Job accounting
		Error detecting aids
		Coordination between other software and users
		Memory management refers to management of Primary Memory or Main Memory. Main memory is a large array of words or bytes where each word or byte has its own address.

Main memory provides a fast storage that can be accessed directly by the CPU. For a program to be executed, it must in the main memory. An Operating System does the following activities for memory management −

		Keeps tracks of primary memory, i.e., what part of it are in use by whom, what part are not in use.

		In multiprogramming, the OS decides which process will get memory when and how much.

		Allocates the memory when a process requests it to do so.

		De-allocates the memory when a process no longer needs it or has been terminated.

### Processor Management
		In multiprogramming environment, the OS decides which process gets the processor when and for how much time. This function is called process scheduling. An Operating System does the following activities for processor management −

		Keeps tracks of processor and status of process. The program responsible for this task is known as traffic controller.

		Allocates the processor (CPU) to a process.

		De-allocates processor when a process is no longer required.

### Device Management
		An Operating System manages device communication via their respective drivers. It does the following activities for device management −

		Keeps tracks of all devices. Program responsible for this task is known as the I/O controller.

		Decides which process gets the device when and for how much time.

		Allocates the device in the efficient way.

		De-allocates devices.
		
### File Management
A file system is normally organized into directories for easy navigation and usage. These directories may contain files and other directions.

An Operating System does the following activities for file management −

		Keeps track of information, location, uses, status etc. The collective facilities are often known as file system.

		Decides who gets the resources.

		Allocates the resources.

		De-allocates the resources.

### Other Important Activities
		Following are some of the important activities that an Operating System performs −

		Security − By means of password and similar other techniques, it prevents unauthorized access to programs and data.

		Control over system performance − Recording delays between request for a service and response from the system.

		Job accounting − Keeping track of time and resources used by various jobs and users.

		Error detecting aids − Production of dumps, traces, error messages, and other debugging and error detecting aids.

		Coordination between other softwares and users − Coordination and assignment of compilers, interpreters, assemblers and other software to the various users of the computer systems.

Above taken from: https://www.tutorialspoint.com/operating_system/os_overview.htm

### Other Notes
- I2C, UART, SPI are examples of serial communication protocols. This is the way in which sensors communicate with microcontrollers and microprocessors
- Inertial Measurement Unit (IMU): a sensor that measures a body's specific force, angular rate, and the orientation of the body, using a combination of accelerometers, gyroscopes, and sometimes magnetometers. The combination of these sensors capture data about the a bodies movement.
- Single Board Computers Used in Robotics: 
		- Nvidia Jetson
		- Raspberry Pi
		- Odroid

Hardware <-- Library to Interface with IMU <-- ROS Package <-- YOUR CODE

### Linux Commands
##### pwd command
Use the pwd command to find out the path of the current working directory (folder) you’re in. The command will return an absolute (full) path, which is basically a path of all the directories that starts with a forward slash (/). An example of an absolute path is /home/username.

##### cd command
To navigate through the Linux files and directories, use the cd command. It requires either the full path or the name of the directory, depending on the current working directory that you’re in.

Let’s say you’re in /home/username/Documents and you want to go to Photos, a subdirectory of Documents. To do so, simply type the following command: cd Photos.

Another scenario is if you want to switch to a completely new directory, for example,/home/username/Movies. In this case, you have to type cd followed by the directory’s absolute path: cd /home/username/Movies.

There are some shortcuts to help you navigate quickly:

cd .. (with two dots) to move one directory up
cd to go straight to the home folder
cd- (with a hyphen) to move to your previous directory
On a side note, Linux’s shell is case sensitive. So, you have to type the name’s directory exactly as it is.

##### ls command
The ls command is used to view the contents of a directory. By default, this command will display the contents of your current working directory.

If you want to see the content of other directories, type ls and then the directory’s path. For example, enter ls /home/username/Documents to view the content of Documents.

There are variations you can use with the ls command:

ls -R will list all the files in the sub-directories as well
ls -a will show the hidden files
ls -al will list the files and directories with detailed information like the permissions, size, owner, etc.

##### cat command
cat (short for concatenate) is one of the most frequently used commands in Linux. It is used to list the contents of a file on the standard output (sdout). To run this command, type cat followed by the file’s name and its extension. For instance: cat file.txt.

Here are other ways to use the cat command:

cat > filename creates a new file
cat filename1 filename2>filename3 joins two files (1 and 2) and stores the output of them in a new file (3)
to convert a file to upper or lower case use, cat filename | tr a-z A-Z >output.txt
5. cp command
Use the cp command to copy files from the current directory to a different directory. For instance, the command cp scenery.jpg /home/username/Pictures would create a copy of scenery.jpg (from your current directory) into the Pictures directory.

##### mv command
The primary use of the mv command is to move files, although it can also be used to rename files.

The arguments in mv are similar to the cp command. You need to type mv, the file’s name, and the destination’s directory. For example: mv file.txt /home/username/Documents.

To rename files, the Linux command is mv oldname.ext newname.ext

##### mkdir command
Use mkdir command to make a new directory — if you type mkdir Music it will create a directory called Music.

There are extra mkdir commands as well:

To generate a new directory inside another directory, use this Linux basic command mkdir Music/Newfile
use the p (parents) option to create a directory in between two existing directories. For example, mkdir -p Music/2020/Newfile will create the new “2020” file.

##### rmdir command
If you need to delete a directory, use the rmdir command. However, rmdir only allows you to delete empty directories.

##### rm command
The rm command is used to delete directories and the contents within them. If you only want to delete the directory — as an alternative to rmdir — use rm -r.

Note: Be very careful with this command and double-check which directory you are in. This will delete everything and there is no undo.

##### touch command
The touch command allows you to create a blank new file through the Linux command line. As an example, enter touch /home/username/Documents/Web.html to create an HTML file entitled Web under the Documents directory.

##### nano or vim command
terminal editors

Above taken from: https://www.hostinger.com/tutorials/linux-commands

### Running Multiple Operating Systems
Partioning Computer
Virtual Machine (hardware dependent)
Container - Docker (software)

### Linux Directory
The following are directories that come with Linux. For SOME of these directories there is no set in stone definition for what is inside these folders. The follow is a convention is generally followed throughout the Linux Community.

#### / - The Root Directory
Everything on your Linux system is located under the / directory, known as the root directory. You can think of the / directory as being similar to the C:\ directory on Windows.
When you run the `cd` command you move to the root directory (or by running `cd /` on mac).

#### /bin - User Binaries
Contains essential user programs(binaries). Applications such as FireFox/Google Chrome will be located here. Other essential programs will also live here.

#### /boot – Static Boot Files
The /boot directory contains the files needed to boot the system.

#### /dev - Device Files
Linux exposes devices as files, and the /dev directory contains a number of special files that represent devices. These are not actual files as we know them, but they appear as files – for example, /dev/sda represents the first SATA drive in the system. If you wanted to partition it, you could start a partition editor and tell it to edit /dev/sda.

#### /etc – Configuration Files
The /etc directory contains configuration files, which can generally be edited by hand in a text editor. Note that the /etc/ directory contains system-wide configuration files – user-specific configuration files are located in each user’s home directory.

#### /opt – Optional Packages
The /opt directory contains subdirectories for optional software packages. It’s commonly used by proprietary software that doesn’t obey the standard file system hierarchy – for example, a proprietary program might dump its files in /opt/application when you install it.

[[Linux-Directory-Structure.jpeg]]

https://www.howtogeek.com/117435/htg-explains-the-linux-directory-structure-explained/
https://www.linode.com/docs/tools-reference/basics/introduction-to-linux-concepts/

```
/bin : All the executable binary programs (file) required during booting, repairing, files required to run into single-user-mode, and other important, basic commands viz., cat, du, df, tar, rpm, wc, history, etc.
/boot : Holds important files during boot-up process, including Linux Kernel.
/dev : Contains device files for all the hardware devices on the machine e.g., cdrom, cpu, etc
/etc : Contains Application’s configuration files, startup, shutdown, start, stop script for every individual program.
/home : Home directory of the users. Every time a new user is created, a directory in the name of user is created within home directory which contains other directories like Desktop, Downloads, Documents, etc.
/lib : The Lib directory contains kernel modules and shared library images required to boot the system and run commands in root file system.
/lost+found : This Directory is installed during installation of Linux, useful for recovering files which may be broken due to unexpected shut-down.
/media : Temporary mount directory is created for removable devices viz., media/cdrom.
/mnt : Temporary mount directory for mounting file system.
/opt : Optional is abbreviated as opt. Contains third party application software. Viz., Java, etc.
/proc : A virtual and pseudo file-system which contains information about running process with a particular Process-id aka pid.
/root : This is the home directory of root user and should never be confused with ‘/‘
/run : This directory is the only clean solution for early-runtime-dir problem.
/sbin : Contains binary executable programs, required by System Administrator, for Maintenance. Viz., iptables, fdisk, ifconfig, swapon, reboot, etc.
/srv : Service is abbreviated as ‘srv‘. This directory contains server specific and service related files.
/sys : Modern Linux distributions include a /sys directory as a virtual filesystem, which stores and allows modification of the devices connected to the system.
/tmp :System’s Temporary Directory, Accessible by users and root. Stores temporary files for user and system, till next boot.
/usr : Contains executable binaries, documentation, source code, libraries for second level program.
/var : Stands for variable. The contents of this file is expected to grow. This directory contains log, lock, spool, mail and temp files.
```

Important FIles and their Locations:
```
/boot/vmlinuz : The Linux Kernel file.
/dev/hda : Device file for the first IDE HDD (Hard Disk Drive)
/dev/hdc : Device file for the IDE Cdrom, commonly
/dev/null : A pseudo device, that don’t exist. Sometime garbage output is redirected to /dev/null, so that it gets lost, forever.
/etc/bashrc : Contains system defaults and aliases used by bash shell.
/etc/crontab : A shell script to run specified commands on a predefined time Interval.
/etc/exports : Information of the file system available on network.
/etc/fstab : Information of Disk Drive and their mount point.
/etc/group : Information of Security Group.
/etc/grub.conf : grub bootloader configuration file.
/etc/init.d : Service startup Script.
/etc/lilo.conf : lilo bootloader configuration file.
/etc/hosts : Information of Ip addresses and corresponding host names.
/etc/hosts.allow : List of hosts allowed to access services on the local machine.
/etc/host.deny : List of hosts denied to access services on the local machine.
/etc/inittab : INIT process and their interaction at various run level.
/etc/issue : Allows to edit the pre-login message.
/etc/modules.conf : Configuration files for system modules.
/etc/motd : motd stands for Message Of The Day, The Message users gets upon login.
/etc/mtab : Currently mounted blocks information.
/etc/passwd : Contains password of system users in a shadow file, a security implementation.
/etc/printcap : Printer Information
/etc/profile : Bash shell defaults
/etc/profile.d : Application script, executed after login.
/etc/rc.d : Information about run level specific script.
/etc/rc.d/init.d : Run Level Initialisation Script.
/etc/resolv.conf : Domain Name Servers (DNS) being used by System.
/etc/securetty : Terminal List, where root login is possible.
/etc/skel : Script that populates new user home directory.
/etc/termcap : An ASCII file that defines the behaviour of Terminal, console and printers.
/etc/X11 : Configuration files of X-window System.
/usr/bin : Normal user executable commands.
/usr/bin/X11 : Binaries of X windows System.
/usr/include : Contains include files used by ‘c‘ program.
/usr/share : Shared directories of man files, info files, etc.
/usr/lib : Library files which are required during program compilation.
/usr/sbin : Commands for Super User, for System Administration.
/proc/cpuinfo : CPU Information
/proc/filesystems : File-system Information being used currently.
/proc/interrupts : Information about the current interrupts being utilised currently.
/proc/ioports : Contains all the Input/Output addresses used by devices on the server.
/proc/meminfo : Memory Usages Information.
/proc/modules : Currently using kernel module.
/proc/mount : Mounted File-system Information.
/proc/stat : Detailed Statistics of the current System.
/proc/swaps : Swap File Information.
/version : Linux Version Information.
/var/log/lastlog : log of last boot process.
/var/log/messages : log of messages produced by syslog daemon at boot.
/var/log/wtmp : list login time and duration of each user on the system currently.
```

Taken From: `https://www.tecmint.com/linux-directory-structure-and-important-files-paths-explained/`