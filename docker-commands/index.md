# Docker Commands
[Manuals](../index.md)

Before you begin using Docker on a Linux system, ensure that you are a member
of the `docker` group. To verify this, execute the following commands:

#### Check if group `docker` exist.
```shell
sudo grep "^docker:" /etc/group
```
if not 
```shell
sudo groupadd docker
```
#### Check your groups 
 ```shell
 groups
 ```
> adm cdrom sudo dip plugdev lxd

if not  
```shell
sudo usermod -a -G docker $USER
```
