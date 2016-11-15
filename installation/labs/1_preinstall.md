1. Access CM Server via .ssh

	login as: root
	Authenticating with public key "imported-openssh-key"
	Last login: Mon Nov 14 15:52:37 2016 from 84.167.109.10

2. Make an EBS volume available for use - 'lsblk'

	[root@ip-172-31-13-101 ~]# lsblk
	NAME MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
	xvdf 202:80   0   1T  0 disk /data
	xvde 202:64   0  32G  0 disk /

3. Create an ext4 file system on the volume 'xvdf'

	[root@ip-172-31-13-101 ~]# mkfs -t ext4

4. Create mount point directory for the volume '/data'

	[root@ip-172-31-13-101 ~]# mkdir /data

5. Mount Volume

	[root@ip-172-31-13-101 ~]# mount /dev/xvdf /data

6. Show results

	[root@ip-172-31-13-101 etc]# df
	Filesystem      1K-blocks   Used  Available Use% Mounted on
	/dev/xvde         8256952 780824    7056700  10% /
	tmpfs             7685696      0    7685696   0% /dev/shm
	/dev/xvdf      1056894132 204056 1003002988   1% /data

7. Make copy of fstab call 'fstab.orig'

	cp /etc/fstab /etc/fstab.orig

	[root@ip-172-31-13-101 etc]# ls -a
	.                        filesystems     motd            rpc
	..                       fstab           mtab            rpm
	acpi                     fstab.orig      my.cnf          rsyslog.conf

8. Edit fstab to auto mount volume on system reboot, add entry on edit:

	/dev/xvdf       /data   ext4    defaults        1       2

9. Get UUID for volume 'dev/xvdf'

	[root@ip-172-31-13-101 etc]# ls -al /dev/disk/by-uuid/
	total 0
	drwxr-xr-x. 2 root root  80 Nov 14 15:51 .
	drwxr-xr-x. 5 root root 100 Nov 14 14:36 ..
	lrwxrwxrwx. 1 root root  10 Nov 14 14:36 44d27f92-d3df-4207-80ea-22830afccf03 -> ../../xvde
	lrwxrwxrwx. 1 root root  10 Nov 14 15:51 87fddd4a-1329-44cf-a295-d178a2d894ea -> ../../xvdf

10. Edit fstab and use UUID (as recommended) 

	87fddd4a-1329-44cf-a295-d178a2d894ea    /data   ext4    defaults,nofail 0       2

11. Test volume mount, if no error - all OK!

	[root@ip-172-31-13-101 etc]# mount -a
	[root@ip-172-31-13-101 etc]#


