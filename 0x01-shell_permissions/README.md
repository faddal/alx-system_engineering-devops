# SHELL PERMISSIONS

### 0. create a script that switches the current user to the user `betty`
```sh
su betty
```

### 1. write a cscript thta prints the effective username of the current user
```sh
whoami
```

### 2. write a script that prints all the groups the current user is part of
```sh
groups
```

### 3. write a script that changes the owner of the file `hello` to the user `betty`
```sh
sudo chown betty hello
```

### 4. write a script that creates an empty file called `hello`
```sh
touch hello
```

### 5. write a script that adds execute permission to the owner of the file `hello`
```sh
chmod u+x hello
```

### 6. write a script that adds execute permission to the owner and the group owner, and read permission to other users, the file `hello`
```sh
chown 754 hello
```
