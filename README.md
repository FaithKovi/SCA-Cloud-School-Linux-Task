# SCA-Cloud-School-Linux-Task 

## Description of the Task

* Create 3 groups and 15 users
* Assign the 15 users across the 3 groups
* Demonstrate that user(s) in a group cannot access files/folders that belong to another group unless they are added to that group

## Prequisites

* Install VM instance on GCP
* Knowledge of Linux

## Task Commands
* Create 3 groups and 15 users
To create a user
```
$ sudo useradd username    Example: sudo useradd karen
```
Use this to create other users. A total of 15 users.
![Create Users](https://github.com/FaithKovi/sca-operation-images/blob/main/group1-add.PNG)
![Create Users](https://github.com/FaithKovi/sca-operation-images/blob/main/group2-users.PNG)
![Create Users](https://github.com/FaithKovi/sca-operation-images/blob/main/group3-users.PNG)

To create groups,
```
$ sudo groupadd -g group-name     Example: sudo groupadd -g SCAgroup1      
```
Use this to create other two groups ```SCAgroup2``` and ```SCAgroup3```

![Create Groups](https://github.com/FaithKovi/sca-operation-images/blob/main/groups.PNG)

* Assign the 15 users across the 3 groups
To add user to a group
```
$ sudo usermod -a -G [groupname] [username]       Example:  sudo usermod -a -G SCAgroup1 karen
```
Add each user to a group, adding users 1-5 in ```SCAgroup1```, users 6-10 in ```SCAgroup2``` and users 11-15 in ```SCAgroup3```

![Add user to group](https://github.com/FaithKovi/sca-operation-images/blob/main/group1-add.PNG)
![Add user to group](https://github.com/FaithKovi/sca-operation-images/blob/main/group2-add.PNG)
![Add user to group](https://github.com/FaithKovi/sca-operation-images/blob/main/group3-add.PNG)
![all](https://github.com/FaithKovi/sca-operation-images/blob/main/all-groups.PNG)
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
![Assign text](https://github.com/FaithKovi/sca-operation-images/blob/main/text-create.PNG)
Checking if the user permissions are correct
```ll```
The Output shows
![Final](https://github.com/FaithKovi/sca-operation-images/blob/main/final.PNG)

