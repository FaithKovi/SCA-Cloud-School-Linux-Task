# SCA-Cloud-School-Linux-Task 

## Description of the Task

* Create 3 groups and 15 users
* Assign the 15 users across the 3 groups
* Demonstrate that user(s) in a group cannot access files/folders that belong to another group unless they are added to that group

## Prequisites

* Install virtualbox

## Task Commands
* Create 3 groups and 15 users
To create a user
```
$ sudo useradd username    Example: sudo useradd karen
```
Use this to create other users. A total of 15 users.
To create groups,
```
$ sudo groupadd -g group-ID group-name     Example: sudo groupadd -g SCAgroup1      
```
Use this to create other two groups ```SCAgroup2``` and ```SCAgroup3```

* Assign the 15 users across the 3 groups
To add user to a group
```
$ sudo usermod -a -G [groupname] [username]       Example:  sudo usermod -a -G SCAgroup1 karen
```
Add each user to a group, adding users 1-5 in ```SCAgroup1```, users 6-10 in ```SCAgroup2``` and users 11-15 in ```SCAgroup3```


* Demonstrate that user(s) in a group cannot access files/folders that belong to another group unless they are added to that group
I created files for each group and assigned them to the respective groups
```
$ sudo chgrp SCAgroup1 SCAgroup1.txt
```
```
$ sudo chgrp SCAgroup2 SCAgroup2.txt
```
```
$ sudo chgrp SCAgroup3 SCAgroup3.txt
```
Checking if the user permissions are correct
```ls``
The Output shows

