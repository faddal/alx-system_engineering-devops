# SHELL PERMISSIONS

> commands to know
`chmod`
`sudo`
`su`
`chown`
`chgrp`
`id`
`groups`
`whoami`
`adduser`
`useradd`
`addgroup`
<br/>

> 0. create a script that switches the current user to the user `betty`
>```console
>su betty
>```  
<br/>

> 1. write a cscript thta prints the effective username of the current user
>```console
>whoami
>```  
<br/>

> 2. write a script that prints all the groups the current user is part of
>```console
>groups
>```
<br/>

> 3. write a script that changes the owner of the file `hello` to the user `betty`
>```console
>sudo chown betty hello
>```
<br/>

> 4. write a script that creates an empty file called `hello`
>```console
>touch hello
>```
<br/>

> 5. write a script that adds execute permission to the owner of the file `hello`
>```console
>chmod u+x hello
>```
<br/>

> 6. write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file `hello`
>```console
>chown 754 hello
>```
<br/>

> 7. Write a script that adds execution permission to the owner, the group owner and the other users, to the file `hello`
>```console
>chown a+x hello
>```
<br/>

> 8. Write a script that sets the permission to the file `hello` as follows:
>- Owner: no permission at all
>- Group: no permission at all
>- Other users: all the permissions
>```console
>chmod 007 hello
>```
<br/>

> 9. Write a script that sets the mode of the file `hello` to this:
>```sh
>-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
>```
>```console
>chmod 753 hello
>```
<br/>

> 10. Write a script that sets the mode of the file `hello` the same as `olleh`’s mode.
> The file hello will be in the working directory
> The file olleh will be in the working directory
>```console
>chmod --reference=olleh hello
>```
<br/>

> 11. Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.
>```console
>chmod -R a+X .
>```
<br/>

> 12. Create a script that creates a directory called `my_dir` with permissions `751` in the working directory.
>```console
>mkdir -m 751 my_dir
>```
<br/>

> 13. Write a script that changes the group owner to school for the `file hello`
>```console
>chgrp school hello
>```
<br/>

> 14. Write a script that changes the owner to `vincent` and the group owner to `staff` for all the files and directories in the working directory
>```console
>chown -R vincent:staff .
>```
</br>

> 15. Write a script that changes the owner and the group owner of `_hello` to `vincent` and `staff` respectively.  
> - The file _hello is in the working directory
> - The file _hello is a symbolic link
>```console
>chown -h vincent:staff _hello
>```
<br/>

> 16. Write a script that changes the owner of the file `hello` to `betty` only if it is owned by the user `guillaume`.  
> - The file hello will be in the working directory
>```console
>chown betty hello --from=guillaume
>```
>```console
>if [ $(stat -c '%U' ./hello) = "guillaume" ]; then chown betty hello; fi
>```
<br/>
