## TASK 5.2
During the process of completing this part of the task all required points have been completed. 
#### Analyzed structure of the /etc/passwd and /etc/group files. Specified and defined several pseudo-users:
#### / etc / passwd
1. registration name or login;
2. hash of the password;
3. user ID;
4. default group ID;
5. Personal data field. GECOS field;
6. initial (home) directory;
7. login shell, or shell.Command interpreter
#### / etc / group
1. The symbolic name of the group.
2. Group password is an obsolete field, not used now.
3. Group identifier, or GID.
4. List of names of participants, separated by commas.
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/pseudousers.png)
#### UID ranges:
A UID (user identifier) is a number assigned by Linux to each user on the system. This number is used to identify the user to the system and to determine which system resources the user can access. UIDs are stored in the /etc/passwd file.
The third field represents the UID. Root user has the UID of 0. Most Linux distributions reserve the first 100 UIDs for system use. New users are assigned UIDs starting from 500 or 1000. For example, new users in Ubuntu start from 1000.
When you create a new account, it will usually be give the next-highest unused number. If we create a new user on our Ubuntu system, it will be given the UID of 1001.
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/uerid.png)
####  GID:
Groups in Linux are defined by GIDs (group IDs). Just like with UIDs, the first 100 GIDs are usually reserved for system use. The GID of 0 corresponds to the root group and the GID of 100 usually represents the users group. GIDs are stored in the /etc/groups file.
The third field represents the GID. New groups are usually assigned GIDs starting from 1000.
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/groups.png)
#### How to determine belonging of user to the specific group?:
command id - shows which group the user belongs to 
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/id.png)
#### What are the commands for adding a user to the system? What are the basic parameters required to create a user?:
Main commands are: __useradd, adduser__.  
Main parameters to create a user are:
#### adduser 
- -c -string representation of username
- -d -user home directory
- -g -the group the user will be a member of
- -m -creates a home directory if it does not exist \ gives permission to access the directory for the given user
- -s -path to default shell] {name} [registration name (must not contain ":", "\ n" ...] 
#### useradd
- -D. When invoked without the -D option, the useradd command creates a new user account using the values specified on the command line plus the default values from the system.
- --g, --gid GROUP. The group name or number of the user's initial login group. The group name must exist. A group number must refer to an already existing group.
- -G, --groups GROUP1[,GROUP2,...[,GROUPN]]] A list of supplementary groups which the user is also a member of.
- -p, --password PASSWORD. The encrypted password, as returned by crypt(3). The default is to disable the password.
- -r, --system. Create a system account.
- -N, --no-user-group. Do not create a group with the same name as the user, but add the user to the group specified by the -g option or by the GROUP variable in /etc/default/useradd.
- -s, --shell SHELL. The name of the user's login shell.
- -e, --expiredate EXPIRE_DATE. The date on which the user account is disabled.
- -m, --create-home. Create the user's home directory if it does not exist. 
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/useradd.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/new%20user.png)
#### How do I change the name (account name) of an existing user?:
#### usermod -l new_username old_username
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/changing%20user.png)
#### What is skell_dir? What is its structure?:
- skel is derived from the skeleton because it contains basic structure of home directory
- The /etc/skel directory contains files and directories that are automatically copied over to a new user’s when it is created from useradd command.
- This will ensure that all the users gets same intial settings and environment.
- The location of /etc/skel can be changed by editing the line that begins with SKEL= in the configuration file /etc/default/useradd. By default this line says SKEL=/etc/skel.
### useradd defaults file
GROUP=100  
HOME=/home  
INACTIVE=-1  
EXPIRE=  
SHELL=/bin/bash  
SKEL=/etc/skel  
CREATE_MAIL_SPOOL=yes  
- Default Permission of the /etc/skel directory is drwxr-xr-x.
It is not recommended to change the permission of skel directory or its contents. skel directory there are some profiles that needs the permission of read and trying to give it permission of execute will cause some programs/profiles to stop work or not works as expected.  
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/skel.png)  
#### How to remove a user from the system (including his mailbox)?:
deluser --remove-home username   
- -remove-home - Delete the user's home directory and mail storage. If --backup is specified, then the files will be removed after the backup is created.
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/deluser.png)
#### What commands and keys should be used to lock and unlock a user account?:
passwd -l user_name - lock  the user    
passwd -u user_name - unlock the user  
You can find out if a user is locked or unlocked using __passwd -S user_name__  
Take a look at the second field in the output. Here's what it means:  
- P or PS: password set (user unlocked)  
- L or LK: user locked  
- N or NP: no password required by the user  
Here is an example of the output from the passwd command:    
standard P 10/14/2019 0 99999 7 -1   
#### How to remove a user's password and provide him with a password-freelogin for subsequent password change?:
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/passwd%20exp.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/passwd%20changing.png)
#### Display the extended format of information about the directory, tell about the information columns displayed on the terminal.:
The first column contains the file permissions in the format owner group others. The next column is the type of file or folder, then the owner and group, then the size, creation date and the last parameter is the name.  
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/ls-l.png)  
#### What access rights exist and for whom (i. e., describe the main roles)? Briefly describe the acronym for access rights:
__r - read ( 4 )__  
__w - write ( 2 )__  
__x - execute ( 1 )__   
--- - no rights, at all;  
--x - only execution of the file is allowed as a program, but not modification or reading;  
-w- - only writing and modifying the file is allowed;  
-wx - modification and execution are allowed, but in the case of a directory, you cannot see its contents;  
r-- - read-only rights;  
r-x - read only and execute, no write permission;  
rw- - read and write permissions, but no execution;  
rwx - all rights;  
--s - the SUID or SGID bit is set, the first is displayed in the field for the owner, the second for the group;  
--t - sticky-bit is set, which means users cannot delete this file.  
#### numeric form: 
0 --- no rights  
1 --x execute reading files and their properties  
2 -w- write   
3 -wx write and execute everything except reading the file list  
4 r - read file names  
5 r-x read and execute read access  
6 rw- read and write read file names  
7 rwx all rights all rights     
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/rights.png)
#### What is the sequence of defining the relationship between the file and the user?:
When clarifying the relationship between a file and the user who started the process, the role is determined as follows:  
- If the UID of the file is the same as the UID of the process, the user is the owner of the file  
- If the GID of the file matches the GID of any group the user belongs to, he is a member of the group to which the file belongs.  
- If neither the UID nor the GID of the file overlaps with the UID of the process and the list of groups that the user running it belongs to, that user is an outsider.   
#### What commands are used to change the owner of a file (directory), as well as the mode of access to the file? Give examples, demonstrate on the terminal:
chmod, chown  
chmod 777 filename  
chown -R user ./filename  
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/chmod.png)  
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/chown.png)   
#### What is an example of octal representation of access rights? Describe the umask command:
By default, umask 0002 is used for a regular user. With this mask, the default permissions for the directory are 775, and for the file 664.  
For superuser (root), the default umask is 0022. With this mask, the default permissions for a directory are 755 and for a file 644.   
The octal notations are as follows:   
- 0 : read, write and execute  
- 1 : read and write  
- 2 : read and execute  
- 3 : read only  
- 4 : write and execute  
- 5 : write only  
- 6 : execute only  
- 7 : no permissions  
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/octal.png)
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/umask1.png) 
#### Give definitions of sticky bits and mechanism of identifier substitution. Give an example of files and directories with these attributes.:
In addition to the normal mode bits, there is one special bit called the sticky bit. It only applies to directories.
Usually, users who have write access to the directory can delete files. A directory with the sticky bit set will only allow the file to be deleted if the user owns the file or the directory itself and has write access to the directory.
There are several such directories on a typical Linux system. One of them is the catalog __/ tmp__ where any user can place temporary files. This directory is specially made available for all users, so it is completely open for writing. However, users cannot be allowed to delete other people's files, so for the directory __/ tmp__ the sticky bit is set.
The presence of a sticky bit is indicated by the letter t at the end of the mode line: 
![](https://github.com/Dudnique/DevOps_online_Kyiv_2021Q2/blob/main/m5/task5.2/tmp.png)  
#### What file attributes should be present in the command script?:
Setting the start bit allows, in fact, to run the file for execution. Such files are called "executables" or shebangs. There are two types of executable files: binary - executed by the central processor, as well as scripts or scripts executed by the command interpreter. In the latter case, it is a regular text file, but in order for the interpreter to determine who it is "dealing with", special instructions are placed at the very beginning of such files, like this:  
### #!/usr/bin/bash - Shebang

