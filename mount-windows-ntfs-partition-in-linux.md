Linux Tutorial
============
A dummy repository to let other learn how to work in CentOS. :)

What is NTFS3G ?
============

NTFS3G is an open source cross-platform, stable, GPL licensed, POSIX, NTFS R/W driver used in Linux. It provides safe handling of Windows NTFS file systems viz create, remove, rename, move files, directories, hard links, etc.

Once EPEL is installed and enabled, let’s install ntfs-3g package using the below command with root user.

```
yum -y install ntfs-3g
```

#Fuse Install

Next, install and load FUSE driver to mount detected devices with below command. FUSE module is included in the kernel itself in version 2.6.18-164 or newer.

```
yum install fuse
modprobe fuse
``

#Identify NTFS Partition

Once fuse module is loaded, type below command to find out NTFS Partitions in Linux.

```
fdisk -l
OR
lsblk
 Device Boot      Start    End      Blocks   Id  System
/dev/sdb1         1	   21270    7816688   b  W95 FAT32
```

#Mount NTFS partition

First create a mount point to mount the NTFS partition.

```
mkdir /mnt/nts
```

Simply run the following command to mount the partition. Replace sda1 with your actual partition found.


```
mount -t ntfs-3g /dev/sda1 /mnt/nts
```

Once it’s mounted on /mnt/ntfs, you may use regular Linux ls -l command to list the content of mounted filesystem.

If you want to make mount point permanent at the boot time, then simple add the following line at the end of /etc/fstab file. This will remain as permanent.


```
/dev/sda1    /mnt/usb    ntfs-3g        defaults    0    0
```

#Umount NTFS Partition

Simply, use the following command to unmount the mounted partition.


```
umount /mnt/usb
```

