login as: root
Authenticating with public key "imported-openssh-key"


1. Change vm.swappiness = 1

	[root@ip-172-31-4-101 vm]# sysctl vm.swappiness=1
	vm.swappiness = 1
	[root@ip-172-31-4-101 vm]#

2. Format FS to -ext4
	[root@ip-172-31-4-101 ~]# lsblk
	NAME MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
	xvdf 202:80   0   1T  0 disk
	xvde 202:64   0  50G  0 disk /

	[root@ip-172-31-4-101 ~]# mkfs -t ext4 /dev/xvdf
	mke2fs 1.41.12 (17-May-2010)
	Filesystem label=
	OS type: Linux
	Block size=4096 (log=2)
	Fragment size=4096 (log=2)
	Stride=0 blocks, Stripe width=0 blocks
	67108864 inodes, 268435456 blocks
	13421772 blocks (5.00%) reserved for the super user
	First data block=0
	Maximum filesystem blocks=4294967296
	8192 block groups
	32768 blocks per group, 32768 fragments per group
	8192 inodes per group
	Superblock backups stored on blocks:
	        32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632, 2654208,
	        4096000, 7962624, 11239424, 20480000, 23887872, 71663616, 78675968,
	        102400000, 214990848

	Writing inode tables: done
	Creating journal (32768 blocks): done
	Writing superblocks and filesystem accounting information: done

	This filesystem will be automatically checked every 34 mounts or
	180 days, whichever comes first.  Use tune2fs -c or -i to override.

3. Create Data Directory
	[root@ip-172-31-4-101 ~]# mkdir /data

4. Mount 
	[root@ip-172-31-4-101 ~]# mount /dev/xvdf /data

	[root@ip-172-31-4-101 ~]# df
	Filesystem      1K-blocks   Used  Available Use% Mounted on
	/dev/xvde         8256952 665500    7172024   9% /
	tmpfs             7685696      0    7685696   0% /dev/shm
	/dev/xvdf      1056894132 204056 1003002988   1% /data

5. Backup fstab and edit/add UUID and startup settings
	[root@ip-172-31-4-101 ~]# cp /etc/fstab /etc/fstab.orig

	[root@ip-172-31-4-101 ~]# cd /etc/

	[root@ip-172-31-4-101 etc]# ls -al /dev/disk/by-uuid/
	total 0
	drwxr-xr-x. 2 root root  80 Nov 15 21:03 .
	drwxr-xr-x. 5 root root 100 Nov 15 20:54 ..
	lrwxrwxrwx. 1 root root  10 Nov 15 20:54 44d27f92-d3df-4207-80ea-22830afccf03 ->                                                                                                                      ../../xvde
	lrwxrwxrwx. 1 root root  10 Nov 15 21:03 7ad9d6d6-8330-43fa-8514-b6209d26662f ->                                                                                                                      ../../xvdf


	[root@ip-172-31-4-101 etc]# nano fstab

		LABEL=centos_root               /        ext4      defaults         0 0
		devpts     /dev/pts  devpts  gid=5,mode=620   0 0
		tmpfs      /dev/shm  tmpfs   defaults         0 0
		proc       /proc     proc    defaults         0 0
		sysfs      /sys      sysfs   defaults         0 0
		7ad9d6d6-8330-43fa-8514-b6209d26662f    /data   ext4    defaults,nofail 0       2

6. Mount (if no errors, successful)

	[root@ip-172-31-4-101 etc]# mount -a

	[root@ip-172-31-4-101 etc]# lsblk
	NAME MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
	xvdf 202:80   0   1T  0 disk /data
	xvde 202:64   0  50G  0 disk /


7. Resize fs
	[root@ip-172-31-4-101 etc]# resize2fs /dev/xvde
	resize2fs 1.41.12 (17-May-2010)
	Filesystem at /dev/xvde is mounted on /; on-line resizing required
	old desc_blocks = 1, new_desc_blocks = 4
	Performing an on-line resize of /dev/xvde to 13107200 (4k) blocks.
	The filesystem on /dev/xvde is now 13107200 blocks long.

	[root@ip-172-31-4-101 etc]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvde        50G  697M   47G   2% /
	tmpfs           7.4G     0  7.4G   0% /dev/shm
	/dev/xvdf      1008G  200M  957G   1% /data

