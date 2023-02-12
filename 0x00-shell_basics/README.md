# SHELL BASICS

> commands to know
`cd`
`ls`
`pwd`
`less`
`file`
`ln`
`cp`
`mv`
`rm`
`mkdir`
`type`
`which`
`help`
`man`
<br/>

> 0. write a script that prints the absolute path name of the current working directory.
>```console
>pwd
>```  
<br/>

> 1. display the contents list of your current directory.
>```console
>ls
>```  
<br/>

> 2. write a script that changes the working directory to the user’s home directory.
>```console
>cd ~
>```
<br/>

> 3. display current directory contents in a long format
>```console
>ls -l
>```
<br/>

> 4. display current directory contents, including hidden files. Use the long format.
>```console
>ls -al
>```
<br/>

> 5. display current directory contents.
> - long format
> - with user and group IDs displayed numerically
> - and hidden files (starting with .)
>```console
>ls -aln
>```
<br/>

> 6. create a script that creates a directory named `my_first_directory` in the `/tmp/ directory`.
>```console
>mkdir /tmp/my_first_directory
>```
<br/>

> 7. move the file `betty` from `/tmp/` to `/tmp/my_first_directory`.
>```console
>mv /tmp/betty /tmp/my_first_directory
>```
<br/>

> 8. delete the file betty.
>- The file `betty` is in `/tmp/my_first_directory`
>```console
>rm /tmp/my_first_directory/betty
>```
<br/>

> 9. delete the directory `my_first_directory` that is in the `/tmp` directory.
>```console
>rmdir /tmp/my_first_directory
>```
<br/>

> 10. write a script that changes the working directory to the previous one.
>```console
>cd -
>```
<br/>

> 11. Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the `parent of the working directory` and the `/boot` directory (in this order), in `long format`.
>```console
>ls -al . .. /boot
>```
<br/>

> 12. Write a script that prints the type of the file named `iamafile`. The file `iamafile` will be in the `/tmp` directory when we will run your script.
>```console
>file /tmp/iamafile
>```
<br/>

> 13. Create a symbolic link to `/bin/ls`, named `__ls__`. The symbolic link should be created in the current working directory.
>```console
>ln -s /bin/ls __ls__
>```
<br/>

> 14. Create a script that copies all the `HTML` files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.
>```console
>cp -u *.html ..
>```
</br>

> 15. Create a script that moves all files beginning with an uppercase letter to the directory `/tmp/u`. You can assume that the directory `/tmp/u` will exist when we will run your script
>```console
>mv [[:upper:]]* /tmp/u
>```
<br/>

> 16. Create a script that deletes all files in the current working directory that end with the character `~`.
>```console
>rm *[~]
>```
<br/>

> 17. Create a script that creates the directories `welcome/`, `welcome/to/` and `welcome/to/school` in the current directory. You are only allowed to use two spaces (and lines) in your script, not more.
>```console
>mkdir -p welcome/to/school
>```
<br/>

> 18. Write a command that lists all the files and directories of the current directory, separated by commas (,).
> - Directory names should end with a slash (/)
> - Files and directories starting with a dot (.) should be listed
> - The listing should be alpha ordered, except for the directories . and .. which should be listed at the very beginning
> - Only digits and letters are used to sort; Digits should come first
> - You can assume that all the files we will test with will have at least one letter or one digit
> - The listing should end with a new line
>```console
>ls -amp
>```
<br/>

> 19. Create a magic file `school.mgc` that can be used with the command file to detect `School` data files. School data files always contain the string `SCHOOL` at `offset 0`.
- [video on magic files](https://www.youtube.com/watch?v=fVOd3Dxifms)
