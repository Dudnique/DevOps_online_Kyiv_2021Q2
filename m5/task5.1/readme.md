## TASK 5.1
### Part 1
During the process of completing this part of the task all required points have been completed. 
#### Logged in to the system as root and used the passwd command to change the password.  Passwd command changes /etc/security/passwd:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/root%20and%20passwd.png)
#### Determined the users registered in the system, and commands they executed:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/registered%20users.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/commands%20history.png)

Additional information that could be gleaned: time of Login, Idle ,The JCPU time (the time used by all processes assigned to the tty. It does include background jobs currently running), 
The PCPU time (the time used by the current process specified in the "what" field).
#### Changed personal information about yourself:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/changing%20personal%20info.png)
#### Became familiar with the Linux help system and the man and info commands:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/--help.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/man%20usermod.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/w%20help%20and%20usage.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/passwd%20status.png)

Definition of the commands' options that were used are described on the screenshots.
#### Viewed the contents of files .bash* using commands more and less:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/more%20bash.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/bash_logout%20less.png)
#### Described in plans that I am working on laboratory work 1:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/finger%20.plan.png)
#### Listed the contents of the home directory using the ls command:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/ls%20command.png)
### Part 2
During the process of completing this part of the task all required points also have been completed. 
#### Examined the tree command:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/tree%20command.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/tree%20subdirectories.png)
#### Command used to determine the type of file:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/determine%20fyletype.png)
#### Mastered the skills of navigating the file system:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/cd.png)
#### Became familiar with the various options for the ls command:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/ls%20options1.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/ls%20options2.png)

- ls –a - list all files including hidden file starting with '.'
- ls -l	- list with long format - show permissions
- ls -la - list long format including hidden files
#### Performed the following sequence of operations:
- created a subdirectory in the home directory;
- in this subdirectory created a file containing information about directories
located in the root directory (using I/O redirection operations);
- viewed the created file;
- copied the created file to your home directory using relative and absolute
addressing.
- deleted the previously created subdirectory with the file requesting removal;
- deleted the file copied to the home directory.
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/creating%20deleting.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/deleting%20with%20request.png)
#### Performed the following sequence of operations:
- created a subdirectory test in the home directory;- copy the .bash_history file to this directory while changing its name to
labwork2;
- created a hard and soft link to the labwork2 file in the test subdirectory;
- changed the data by opening a symbolic link. What changes will happen and
why
- renamed the hard link file to hard_lnk_labwork2;
- renamed the soft link file to symb_lnk_labwork2 file;
- deleted the labwork2.

![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/CREATING%20SOFT%20AND%20HARD.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/rename%20links%20and%20deleting.png)
#### A soft link
- can cross the file system,
- allows you to link between directories,
- has different inodes number and file permissions than original file,
- permissions will not be updated,
- has only the path of the original file, not the contents.
#### A hard Link
- can’t cross the file system boundaries,
- can’t link directories,
- has the same inodes number and permissions of original file,
- permissions will be updated if we change the permissions of source file,
- has the actual contents of original file, so that you still can view the contents, even if the original file moved or removed.

Soft link is just a link that points to the original file. The softlink is like a shortcut to a file. If you remove the file, the shortcut is useless. If you remove the soft link, the original file will still present. 
As you can see above, even if I deleted the source file, I can view contents of the hardlink.file. Hard link shares the same inodes number, the permissions and data of the original file.
#### Found all files that contain the squid and traceroute sequence:
##### By default, the squid is not in the system. Squid is a caching proxy for the Web supporting HTTP, HTTPS, FTP, and more.
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/squid%20and%20traceroute.png)
#### Determined which partitions are mounted in the system, as well as the types of these partitions.:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/mounted%20partitioins%20and%20devices.png)
#### Count the number of lines containing a given sequence of characters in a given file:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/number%20of%20lines.png)
#### Using the find command, found all files in the /etc directory containing the host character sequence.:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/find%20host.png)
#### Listed all objects in /etc that contain the ss character sequence. :
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/find%20and%20grep%20ss.png)
#### Organized a screen-by-screen print of the contents of the /etc directory with used stream redirection operations.:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/scr-by-scr%20print.png)
####  Types of devices:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/lsdev%20devices.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/lshw%20devices.png)
#### Totally 7 types of files are available in Linux with 3 Major categories. The details are below.

- |      -       | Regular File           |
- |      d       | Directory              |
- |      l       | Link File              |
- |      c       | Character Device File  |
- |      s       | Local Socket File      |
- |      p       | Named Pipe File        |
- |      b       | Block Device File      |

#### Device files are denoted as the following:

- c - character
- b - block
- p - pipe
- s - socket

#### Character Device
These devices transfer data, but one a character at a time. You'll see a lot of pseudo devices (/dev/null) as character devices, these devices aren't really physically connected to the machine, but they allow the operating system greater functionality.
#### Block Device
These devices transfer data, but in large fixed-sized blocks. You'll most commonly see devices that utilize data blocks as block devices, such as harddrives, filesystems, etc.
#### Pipe Device
Named pipes allow two or more processes to communicate with each other, these are similar to character devices, but instead of having output sent to a device, it's sent to another process.
#### Socket Device
Socket devices facilitate communication between processes, similar to pipe devices but they can communicate with many processes at once.
#### Listed the first 5 directory files that were recently accessed in the /etc directory:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.1/last%205%20files.png)
