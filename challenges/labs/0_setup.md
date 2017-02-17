0_setup.md

Cloud Provider AWS

Linux Release - Centos 6.5

Disk Space Enabled

		[root@ip-172-31-25-177 sysconfig]# sysctl vm.swappiness=1
		vm.swappiness = 1
		[root@ip-172-31-25-177 sysconfig]# lsblk
		NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
		xvda    202:0    0   16G  0 disk
		├─xvda1 202:1    0  500M  0 part /boot
		└─xvda2 202:2    0 15.5G  0 part
		  ├─VolGroup-lv_root (dm-0)
		        253:0    0 13.9G  0 lvm  /
		  └─VolGroup-lv_swap (dm-1)
		        253:1    0  1.6G  0 lvm  [SWAP]
		xvdb    202:16   0   50G  0 disk

		[root@ip-172-31-28-97 sysconfig]# sysctl vm.swappiness=1
		vm.swappiness = 1
		[root@ip-172-31-28-97 sysconfig]# lsblk
		NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
		xvda    202:0    0   16G  0 disk
		├─xvda1 202:1    0  500M  0 part /boot
		└─xvda2 202:2    0 15.5G  0 part
		  ├─VolGroup-lv_root (dm-0)
		        253:0    0 13.9G  0 lvm  /
		  └─VolGroup-lv_swap (dm-1)
		        253:1    0  1.6G  0 lvm  [SWAP]
		xvdb    202:16   0   50G  0 disk

		[root@ip-172-31-30-17 sysconfig]# sysctl vm.swappiness=1
		vm.swappiness = 1
		[root@ip-172-31-30-17 sysconfig]# lsblk
		NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
		xvda    202:0    0   16G  0 disk
		├─xvda1 202:1    0  500M  0 part /boot
		└─xvda2 202:2    0 15.5G  0 part
		  ├─VolGroup-lv_root (dm-0)
		        253:0    0 13.9G  0 lvm  /
		  └─VolGroup-lv_swap (dm-1)
		        253:1    0  1.6G  0 lvm  [SWAP]
		xvdb    202:16   0   50G  0 disk

		[root@ip-172-31-21-240 sysconfig]# sysctl vm.swappiness=1
		vm.swappiness = 1
		[root@ip-172-31-21-240 sysconfig]# lsblk
		NAME                        MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
		xvda                        202:0    0   16G  0 disk
		├─xvda1                     202:1    0  500M  0 part /boot
		└─xvda2                     202:2    0 15.5G  0 part
		  ├─VolGroup-lv_root (dm-0) 253:0    0 13.9G  0 lvm  /
		  └─VolGroup-lv_swap (dm-1) 253:1    0  1.6G  0 lvm  [SWAP]
		xvdb                        202:16   0   50G  0 disk

		[root@ip-172-31-22-220 sysconfig]# sysctl vm.swappiness=1
		vm.swappiness = 1
		[root@ip-172-31-22-220 sysconfig]# lsblk
		NAME                        MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
		xvda                        202:0    0   16G  0 disk
		├─xvda1                     202:1    0  500M  0 part /boot
		└─xvda2                     202:2    0 15.5G  0 part
		  ├─VolGroup-lv_root (dm-0) 253:0    0 13.9G  0 lvm  /
		  └─VolGroup-lv_swap (dm-1) 253:1    0  1.6G  0 lvm  [SWAP]
		xvdb                        202:16   0   50G  0 disk

Yum Repolist Enabled

		[root@ip-172-31-25-177 etc]# yum repolist enabled
		Loaded plugins: fastestmirror
		Loading mirror speeds from cached hostfile
		 * base: mirrors.ocf.berkeley.edu
		 * extras: mirror.team-cymru.org
		 * updates: centos.sonn.com
		repo id              repo name                       status
		base                 CentOS-6 - Base                 6,696
		extras               CentOS-6 - Extras                  63
		updates              CentOS-6 - Updates                825
		repolist: 7,584

		[root@ip-172-31-28-97 etc]# yum repolist enabled
		Loaded plugins: fastestmirror
		Loading mirror speeds from cached hostfile
		 * base: mirror.sigmanet.com
		 * extras: centos.mirrors.tds.net
		 * updates: centos.sonn.com
		repo id           repo name                     status
		base              CentOS-6 - Base               6,696
		extras            CentOS-6 - Extras                63
		updates           CentOS-6 - Updates              825
		repolist: 7,584

		[root@ip-172-31-30-17 etc]# yum repolist enabled
		Loaded plugins: fastestmirror
		Loading mirror speeds from cached hostfile
		 * base: mirror.sigmanet.com
		 * extras: yum.tamu.edu
		 * updates: centos.mirrors.hoobly.com
		repo id               repo name                        status
		base                  CentOS-6 - Base                  6,696
		extras                CentOS-6 - Extras                   63
		updates               CentOS-6 - Updates                 825
		repolist: 7,584

		[root@ip-172-31-21-240 etc]# yum repolist enabled
		Loaded plugins: fastestmirror
		Loading mirror speeds from cached hostfile
		 * base: mirror.sigmanet.com
		 * extras: mirror.team-cymru.org
		 * updates: centos.sonn.com
		repo id                               repo name                                         status
		base                                  CentOS-6 - Base                                   6,696
		extras                                CentOS-6 - Extras                                    63
		updates                               CentOS-6 - Updates                                  825
		repolist: 7,584

		[root@ip-172-31-22-220 etc]# yum repolist enabled
		Loaded plugins: fastestmirror
		Loading mirror speeds from cached hostfile
		 * base: mirror.sigmanet.com
		 * extras: mirror.team-cymru.org
		 * updates: centos.mirrors.hoobly.com
		repo id                            repo name                                     status
		base                               CentOS-6 - Base                               6,696
		extras                             CentOS-6 - Extras                                63
		updates                            CentOS-6 - Updates                              825
		repolist: 7,584


Add Users & Groups

	raffles:x:2000:502::/home/raffles:/bin/bash
	fullerton:x:3000:501::/home/fullerton:/bin/bash

	hotels:x:501:
	shops:x:502:


