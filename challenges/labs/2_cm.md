2_cm.md

ls Cloudera manager
```
[root@ip-172-31-21-240 etc]# ls /etc/yum.repos.d
CentOS-Base.repo       CentOS-Media.repo      mysql-community.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo      mysql-community-source.repo
CentOS-fasttrack.repo  cloudera-manager.repo
```

Cloudera Manger Repo File
```
[cloudera-manager]
# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 6 x86_64
name=Cloudera Manager
baseurl=https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/5/
gpgkey =https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/RPM-GPG-KEY-cloudera
gpgcheck = 1
```
