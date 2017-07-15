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
