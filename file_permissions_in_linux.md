# File permissions in linux


## Ownership and Permission

- The concept of Linux file permission and ownership is crucial in Linux.
- Linux is a multi-user operating system and is used in main-frame and services. Therefore, the files should be kept safe from maline users who can corrupt, change or steal the data.  
- Therefore, for effective security linux divides authorization into two levels: 
  - Ownership
  - Permissions


## Ownership in Linux files

- There are three types of ownerships assigned to every file or directory in all Linux systems, as listed below:
  - User:
    > A user is the owner of the file. By default, the person who created a file becomes its owner. Hence, a user is also sometimes called an owner.
  - Group:
    > A user- group can contain multiple users. All users belonging to a group will have the same Linux group permissions access to the file.
  - Others:
    > Any other user who has access to a file. This person has neither created the file, nor he belongs to a usergroup who could own the file. Practically, it means everybody else. Hence, when you set the permission for others, it is also referred as set permissions for the world.


## Permissions in Linux files

- Now, how does Linux distinguish between these three user types so that a user ‘A’ cannot affect a file which contains some other user ‘B’s’ vital information/data. This is where Permissions set in, and they define user behavior.
- Each and every file and directory in your Linux system has following 3 permission defined for all the 3 owners discussed above.
  - Read (r): 
    > This permission give you the authority to open and read a file. Read permission on a directory gives you the ability to lists its content.
  - Write (w):
    > The write permission gives you the authority to modify the contents of a file. The write permission on a directory gives you the authority to add, remove and rename files stored in the directory. 
  - Execute (x):
    > In Unix/Linux, you cannot run a program unless the execute permission is set. If the execute permission is not set, you might still be able to see/modify the program code(provided read & write permissions are set), but not run it.


## 	Syntax explanation of file permissions in Linux

- The ls -l command on the terminal gives:
  ```bash 
    -rw-rw-r-- 1 surya surya 3028 Jan 30 10:15 sample.pdf
  ```
- The first 10 characters explains the file permissions for each type of owners. 
- The first character is either a "-" which represents a file or a "d" which represents a directory.
- The following set of 3 characters show the permissions of the owner.
- The next set of 3 characters show the permissions for the group.
- The last set of 3 characters show the permissions for the world which means any user.
  > Example:
    > "-rwxrw-r--"
    > In this case, the first character "-" tells us that we are viewing a file.  
    > The next set of three characters "rwx" tells us that the owner has read, write and execute permissions.  
    > The following set of three characters "rw-" tells us that the group members have read, write access but not execute access.  
    > The following set of three characters "r--" tells us that any other user can only read the contents of the file.



## Changing file/directory permissions in Linux using "chmod"

- Say you do not want your colleague to see your personal images. This can be achieved by changing file permissions.
- The "chmod" stands for changing mode and using this command we can set permissions on a file/directory for the owner, group and the world.
  > Syntax:
    ```bash
      root@ubuntu:~# chmod permissions filename 
    ```
- Absolute(Numeric) mode: In this mode, file permissions are not represented as characters but a three-digit octal number. The table below gives numbers for all for permissions types.
>    | Number    | Permission Type   | Symbol  |
>    | --------  | ----------------- | ------- |
>    | 0         | No Permision      | ---     |
>    | 1         | Execute           | --x     |
>    | 2         | Write             | -w-     |
>    | 2         | Write             | -w-     |
>    | 2         | Write             | -w-     |
	





