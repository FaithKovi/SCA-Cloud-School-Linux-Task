# SCA-Cloud-School-Linux-Task 

## Description of the Task

* Create 3 groups and 15 users
* Assign the 15 users across the 3 groups
* Demonstrate that user(s) in a group cannot access files/folders that belong to another group unless they are added to that group

## Prequisites

* Install virtualbox

## Task Commands

* Create user
```
sudo useradd username    Example: sudo useradd karen
```
Use this to create other users. A total of 15 users.
* Create groups
```
sudo groupadd -g group-ID group-name     Example: sudo groupadd -g SCAgroup1      
```
Use this to create other two groups ```SCAgroup2``` and ```SCAgroup3```
* Add users to group
```
sudo usermod -a -G [groupname] [username]       Example:  sudo usermod -a -G SCAgroup1 karen
```
Add each user to a group

* Create files for each group
```
sudo chgrp SCAgroup1 SCAgroup1.txt
```
```
sudo chgrp SCAgroup2 SCAgroup2.txt
```
```
sudo chgrp SCAgroup3 SCAgroup3.txt
```
