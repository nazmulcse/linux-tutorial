Dual boot issue between Windows & CentOS
============

Sometimes We want to use windows & linux using dual boot. In this tutorial, I will discuss
dual boot problem in Windows to CentOS & vice versa.

###### Problem 1 :
After installing windows when we install centos then Windows is not found in dual boot option.
For getting Windows in dual boot option follow the following command:

First check your partition list using the command

```
lsblk
```

After showing partition list, we see that windows system drive(C drive) is
sd1 that means first partition

Then run the command using Super user mode

```
nano /boot/grub2/grub.cfg
```

After opening grub file, add the following code after last menuentry option

```
 menuentry 'Windows OS' {
        set root='(hd0,1)'
        chainloader +1
 }
```

Here (hd0,1) is for first partition sd1


###### Problem 2 :

After installing CentOS when we install Windows then CentOS is not found in dual boot option.
Enter bootable pendrive with Centos or CD/DVD and restart windows. After restarting, CentOS
installation start with three option. Then follow the following command :

```
Troubleshoot img -> Rescue a CentOS system -> Enter command 1
```

Then hit the enter. After comming new cmd window, again hit the enter. then write the following command that is shown in window

```
chroot /mnt/sysimage
```

And hit the enter. Then write the following command for installing grub2 bootloader in centos 7

```
grub2-install /dev/sda
```

Then install grub2 and enter exit command and at last reboot . 

