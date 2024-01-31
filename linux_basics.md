***
# Linux Basics
***

## Top regular use commands in Linux

1. pwd: 
  - The pwd command allows you to print the current working directory on your terminal.
  	> Example: 
      ```bash
        root@ubuntu:~# pwd
      ```
***
2. ls: 
  - The ls command is used to list all the files and directories in the current working directory.
  	> Example: 
  	  ```bash
  	    root@ubuntu:~# ls
  	  ```
***
3. cd: 
  - The cd command allows you to navigate through directories. Just type cd followed by directory as shown below.
  	> Example: 
  	  ```bash
  	    root@ubuntu:~# cd <directory path>
  	  ```
***
4. mkdir:
  - The mkdir command allows you to create directories within the terminal.
  - The -p options is used to create sub-directories of a directory. It will create parent directory first, if it doesn’t exist.
    > Example: 
  	  ```bash
  	    root@ubuntu:~# mkdir <folder name>
        root@ubuntu:~# mkdir -p user/abcd/efgh
      ```
***
5. cp:
  - The cp command is equivalent to the copy-pastein Windows.
    > Example: 
  	  ```bash
  	    root@ubuntu:~# cp <source> <destination>
  	  ```
***
6. rm:
  - The rm command is used to delete files and folders.
  - You have to add the -r argument to it. Without the -r argument, rm command won't delete directories.
    > Example: 
  	  ```bash
  	    root@ubuntu:~# rm <file name>
		root@ubuntu:~# rm -r <folder/directory name>
  	  ```
***
7. touch:
  - To create a new file, the touch command is used.
    > Example: 
  	  ```bash
  	    root@ubuntu:~# touch <file name>
  	  ```
***
8. ln:
  - To create a link to another file, we use the ln command.
  - The basic syntax involves using the -s parameter so we can create a symbolic link or soft link.
    > Example: 
  	  ```bash
  	    root@ubuntu:~# ln -s <source path> <link name>
  	  ```
***
9. cat:
  - The cat command prints the contents of a file.
    > Example: 
  	  ```bash
  	    root@ubuntu:~# cat <file name>
  	  ```
***
10. echo:
  - The echo command whatever follows the command.
    > Example: 
  	  ```bash
  	    root@ubuntu:~# echo <Text to print on terminal>
  	  ```
***
11. less:
  - The less command is used when the output printed by any command is larger than the screen space and needs scrolling.
  - The less command allows us to break down the output and scroll through it with the use of the enter or space keys.
    > Example: 
  	  ```bash
	    root@ubuntu:~# cat /boot/grub/grub.cfg  | less
  	  ```
***
12. man:
  - The man command is very useful Linux command that offers a really efficient way to know the functionality of pretty much all the packages and commands. 
    > Example:
      ```bash
        root@ubuntu:~# man <command>
      ```
***
13. uname:
  - The uname command with the "-a" parameter prints out the complete information of your computer.
    > Example:
      ```bash
        root@ubuntu:~# uname -a
      ```
***
14. whoami:
  - The whoami command prints tha name of the current user.
    > Example:
      ```bash
        root@ubuntu:~# whoami 
      ```
***
15. grep:
  - The grep command is used to search for a specific string within an output..
    > Example:
      ```bash
        root@ubuntu:~# ls | grep text.txt 
      ```
***
16. head and tail:
  - The head command prints the first 10 lines of the file, while the tail command prints the last 10 lines of the file.
    > Example:
      ```bash
        root@ubuntu:~# head text.txt 
        root@ubuntu:~# tail text.txt
      ```
***
17. diff:
  - The diff commond tells you the instructions on how to change the first file to make it match the second file.
    > Example:
      ```bash
        root@ubuntu:~# diff [options] text1.txt text2.txt
      ```
***
18. cmp:
  - The cmp command tells us the line number which is different and not the actual text.
    > Example:
      ```bash
        root@ubuntu:~# cmp text1.txt text2.txt
      ```
***
19. comm:
  - The comm commands is used to compare to files and will output three columns, where the first column is text contained only in file 1, second column is text common in both files and the last column contains text present only in file 2.
    > Example:
      ```bash
        root@ubuntu:~# comm file1.txt file2.txt
      ```
***
20. sort:
  - The sort command will provide a sorted output of the contents of the file.
    > Example:
      ```bash
        root@ubuntu:~# sort file.txt
      ```
***
21. whereis:
  - The whereis command will output the exact location of any command that you type in after the whereis command.
    > Example:
      ```bash
        root@ubuntu:~# whereis sudo
      ```
***
22. whatis:
  - The whatis command gives us an explanation of what a command actually is.
    > Example:
      ```bash
        root@ubuntu:~# whatis sudo
      ```
***
23. sudo:
  - The sudo command isused to run commands with escalated priveleges.
    > Example:
      ```bash
        root@ubuntu:~# sudo cp text.tx text1.txt 
      ```
***
24. useradd:
  - The useradd is used to create a new user.
    > Example:
      ```bash
        root@ubuntu:~# useradd JournalDev -d /home/JD
      ``` 
***
25. usermod:
  - The usermod command is used to modify existing users. You can modify any value of the user including the groups, the permissions, etc.
    > Example:
      ```bash
        root@ubuntu:~# usermod JournalDev -a -G sudo, audio, mysql
      ```
***
26. passwd:
  - The passwd command is used to set the password for your own account, or if you have the permissions, set the password for other accounts.
    > Example:
      ```bash
        root@ubuntu:~# passwd
      ```
***
27. meld:
  - The meld command is a visual diff and merge tool which allows us to compare files or directories and merge changes between them in a graphical and user-friendly way.
    > Example:
      ```bash
        root@ubuntu:~# meld file1.txt file2.txt
      ```
***
28. tree:
  - The tree command is used to display contents of a directory in a tree like format.
    > Example:
      ```bash
        root@ubuntu:~# tree
        #list only directories
        root@ubuntu:~# tree -d
        #list tree with specified depth
        root@ubuntu:~# tree -L 1
      ```
***
29. du:
  - The du command is used to gain disk usage information quickly.
    > Example:
      ```bash
        #disk usage in kilobytes with human-readable format
        root@ubuntu:~# du -kh 
        #sum of disk usage in kilobytes with human-readable format
        root@ubuntu:~# du -skh
        #disk usage in human-readable format of a particular file
        root@ubuntu:~# du -sh file path
        #sum of disk usage of all files in human-readable format
        root@ubuntu:~# tree
      ```
***
30. tee:
  - The tee command takes the ouput of a command as standard input and writes it to both the standard output(terminal) and one or more files.
    > Example:
      ```bash
        root@ubuntu:~# df -h | tee disk_usage.txt
      ```
***
31 evince:
  - The evince command is used to open a .pdf document
    > Example: 
    ``` bash
      root@ubuntu:~# evince sample.pdf
      #to open in fullscreen mode
      root@ubuntu:~# evince --fullscreen sample.pdf
      #to open in presentation mode
      root@ubuntu:~# evince --presentation sample.pdf
      # to open in preview mode
      root@ubuntu:~# evince --preview sample.pdf
    ```
***
31 find:
  - The find command is used to for searching and locatind directories in a file system hierarchy.
    > Example: 
    ``` bash
      root@ubuntu:~# find /path/to/search -name "text.txt"
      #to find files by extension
      root@ubuntu:~# find . name "*.pdf"
      #to find directories
      root@ubuntu:~# find . -type d 
      # to find files larger than a specific size
      root@ubuntu:~# find . -type f -size +1M
      # to find files modified within the last  days
      root@ubuntu:~# find . -type f -mtime -7
    ```
***
32. 