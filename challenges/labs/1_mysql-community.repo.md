1_mysql-community.repo.md

		[root@ip-172-31-2-245 yum.repos.d]# nano mysql-community.repo
		[root@ip-172-31-2-245 yum.repos.d]# yum install mysql
		Loaded plugins: fastestmirror, presto
		Loading mirror speeds from cached hostfile
		 * base: repo.uk.bigstepcloud.com
		 * extras: centos.serverspace.co.uk
		 * updates: mirror.vorboss.net
		mysql-connectors-community                                                                                                                                                    | 2.5 kB     00:00
		mysql-connectors-community/primary_db                                                                                                                                         |  11 kB     00:00
		mysql-tools-community                                                                                                                                                         | 2.5 kB     00:00
		mysql-tools-community/primary_db                                                                                                                                              |  32 kB     00:00
		mysql56-community                                                                                                                                                             | 2.5 kB     00:00
		mysql56-community/primary_db                                                                                                                                                  | 168 kB     00:00
		Setting up Install Process
		Package mysql is obsoleted by mysql-community-client, trying to install mysql-community-client-5.6.34-2.el6.x86_64 instead
		Resolving Dependencies
		--> Running transaction check
		---> Package mysql-community-client.x86_64 0:5.6.34-2.el6 will be installed
		--> Processing Dependency: mysql-community-libs(x86-64) >= 5.6.10 for package: mysql-community-client-5.6.34-2.el6.x86_64
		--> Processing Dependency: perl(Sys::Hostname) for package: mysql-community-client-5.6.34-2.el6.x86_64
		--> Processing Dependency: perl(IPC::Open3) for package: mysql-community-client-5.6.34-2.el6.x86_64
		--> Processing Dependency: perl(Getopt::Long) for package: mysql-community-client-5.6.34-2.el6.x86_64
		--> Processing Dependency: perl(File::Temp) for package: mysql-community-client-5.6.34-2.el6.x86_64
		--> Processing Dependency: perl(Fcntl) for package: mysql-community-client-5.6.34-2.el6.x86_64
		--> Processing Dependency: perl(Exporter) for package: mysql-community-client-5.6.34-2.el6.x86_64
		--> Processing Dependency: /usr/bin/perl for package: mysql-community-client-5.6.34-2.el6.x86_64
		--> Running transaction check
		---> Package mysql-community-libs.x86_64 0:5.6.34-2.el6 will be obsoleting
		--> Processing Dependency: mysql-community-common(x86-64) >= 5.6.10 for package: mysql-community-libs-5.6.34-2.el6.x86_64
		---> Package mysql-libs.x86_64 0:5.1.71-1.el6 will be obsoleted
		--> Processing Dependency: libmysqlclient.so.16()(64bit) for package: 2:postfix-2.6.6-2.2.el6_1.x86_64
		--> Processing Dependency: libmysqlclient.so.16(libmysqlclient_16)(64bit) for package: 2:postfix-2.6.6-2.2.el6_1.x86_64
		---> Package perl.x86_64 4:5.10.1-141.el6_7.1 will be installed
		--> Processing Dependency: perl-libs = 4:5.10.1-141.el6_7.1 for package: 4:perl-5.10.1-141.el6_7.1.x86_64
		--> Processing Dependency: perl-libs for package: 4:perl-5.10.1-141.el6_7.1.x86_64
		--> Processing Dependency: perl(version) for package: 4:perl-5.10.1-141.el6_7.1.x86_64
		--> Processing Dependency: perl(Pod::Simple) for package: 4:perl-5.10.1-141.el6_7.1.x86_64
		--> Processing Dependency: perl(Module::Pluggable) for package: 4:perl-5.10.1-141.el6_7.1.x86_64
		--> Processing Dependency: libperl.so()(64bit) for package: 4:perl-5.10.1-141.el6_7.1.x86_64
		--> Running transaction check
		---> Package mysql-community-common.x86_64 0:5.6.34-2.el6 will be installed
		---> Package mysql-community-libs-compat.x86_64 0:5.6.34-2.el6 will be obsoleting
		---> Package perl-Module-Pluggable.x86_64 1:3.90-141.el6_7.1 will be installed
		---> Package perl-Pod-Simple.x86_64 1:3.13-141.el6_7.1 will be installed
		--> Processing Dependency: perl(Pod::Escapes) >= 1.04 for package: 1:perl-Pod-Simple-3.13-141.el6_7.1.x86_64
		---> Package perl-libs.x86_64 4:5.10.1-141.el6_7.1 will be installed
		---> Package perl-version.x86_64 3:0.77-141.el6_7.1 will be installed
		---> Package postfix.x86_64 2:2.6.6-2.2.el6_1 will be updated
		---> Package postfix.x86_64 2:2.6.6-6.el6_7.1 will be an update
		--> Running transaction check
		---> Package perl-Pod-Escapes.x86_64 1:1.04-141.el6_7.1 will be installed
		--> Finished Dependency Resolution

		Dependencies Resolved

		=====================================================================================================================================================================================================
		 Package                                                  Arch                                Version                                           Repository                                      Size
		=====================================================================================================================================================================================================
		Installing:
		 mysql-community-client                                   x86_64                              5.6.34-2.el6                                      mysql56-community                               18 M
		 mysql-community-libs                                     x86_64                              5.6.34-2.el6                                      mysql56-community                              1.9 M
		     replacing  mysql-libs.x86_64 5.1.71-1.el6
		 mysql-community-libs-compat                              x86_64                              5.6.34-2.el6                                      mysql56-community                              1.6 M
		     replacing  mysql-libs.x86_64 5.1.71-1.el6
		Installing for dependencies:
		 mysql-community-common                                   x86_64                              5.6.34-2.el6                                      mysql56-community                              308 k
		 perl                                                     x86_64                              4:5.10.1-141.el6_7.1                              base                                            10 M
		 perl-Module-Pluggable                                    x86_64                              1:3.90-141.el6_7.1                                base                                            40 k
		 perl-Pod-Escapes                                         x86_64                              1:1.04-141.el6_7.1                                base                                            33 k
		 perl-Pod-Simple                                          x86_64                              1:3.13-141.el6_7.1                                base                                           213 k
		 perl-libs                                                x86_64                              4:5.10.1-141.el6_7.1                              base                                           579 k
		 perl-version                                             x86_64                              3:0.77-141.el6_7.1                                base                                            52 k
		Updating for dependencies:
		 postfix                                                  x86_64                              2:2.6.6-6.el6_7.1                                 base                                           2.0 M

		Transaction Summary
		=====================================================================================================================================================================================================
		Install      10 Package(s)
		Upgrade       1 Package(s)

		Total download size: 35 M
		Is this ok [y/N]: y
		Downloading Packages:
		Setting up and reading Presto delta metadata
		Processing delta metadata
		Package(s) data still to download: 35 M
		(1/11): mysql-community-client-5.6.34-2.el6.x86_64.rpm                                                                                                                        |  18 MB     00:00
		(2/11): mysql-community-common-5.6.34-2.el6.x86_64.rpm                                                                                                                        | 308 kB     00:00
		(3/11): mysql-community-libs-5.6.34-2.el6.x86_64.rpm                                                                                                                          | 1.9 MB     00:00
		(4/11): mysql-community-libs-compat-5.6.34-2.el6.x86_64.rpm                                                                                                                   | 1.6 MB     00:00
		(5/11): perl-5.10.1-141.el6_7.1.x86_64.rpm                                                                                                                                    |  10 MB     00:00
		(6/11): perl-Module-Pluggable-3.90-141.el6_7.1.x86_64.rpm                                                                                                                     |  40 kB     00:00
		(7/11): perl-Pod-Escapes-1.04-141.el6_7.1.x86_64.rpm                                                                                                                          |  33 kB     00:00
		(8/11): perl-Pod-Simple-3.13-141.el6_7.1.x86_64.rpm                                                                                                                           | 213 kB     00:00
		(9/11): perl-libs-5.10.1-141.el6_7.1.x86_64.rpm                                                                                                                               | 579 kB     00:00
		(10/11): perl-version-0.77-141.el6_7.1.x86_64.rpm                                                                                                                             |  52 kB     00:00
		(11/11): postfix-2.6.6-6.el6_7.1.x86_64.rpm                                                                                                                                   | 2.0 MB     00:00
		-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
		Total                                                                                                                                                                 33 MB/s |  35 MB     00:01
		warning: rpmts_HdrFromFdno: Header V3 DSA/SHA1 Signature, key ID 5072e1f5: NOKEY
		Retrieving key from file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
		Importing GPG key 0x5072E1F5:
		 Userid : MySQL Release Engineering <mysql-build@oss.oracle.com>
		 Package: mysql57-community-release-el6-9.noarch (installed)
		 From   : /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
		Is this ok [y/N]: y
		Running rpm_check_debug
		Running Transaction Test
		Transaction Test Succeeded
		Running Transaction
		Warning: RPMDB altered outside of yum.
		  Installing : 1:perl-Pod-Escapes-1.04-141.el6_7.1.x86_64                                                                                                                                       1/13
		  Installing : 1:perl-Module-Pluggable-3.90-141.el6_7.1.x86_64                                                                                                                                  2/13
		  Installing : 3:perl-version-0.77-141.el6_7.1.x86_64                                                                                                                                           3/13
		  Installing : 4:perl-libs-5.10.1-141.el6_7.1.x86_64                                                                                                                                            4/13
		  Installing : 1:perl-Pod-Simple-3.13-141.el6_7.1.x86_64                                                                                                                                        5/13
		  Installing : 4:perl-5.10.1-141.el6_7.1.x86_64                                                                                                                                                 6/13
		  Installing : mysql-community-common-5.6.34-2.el6.x86_64                                                                                                                                       7/13
		  Installing : mysql-community-libs-5.6.34-2.el6.x86_64                                                                                                                                         8/13
		  Installing : mysql-community-libs-compat-5.6.34-2.el6.x86_64                                                                                                                                  9/13
		  Updating   : 2:postfix-2.6.6-6.el6_7.1.x86_64                                                                                                                                                10/13
		  Installing : mysql-community-client-5.6.34-2.el6.x86_64                                                                                                                                      11/13
		  Cleanup    : 2:postfix-2.6.6-2.2.el6_1.x86_64                                                                                                                                                12/13
		  Erasing    : mysql-libs-5.1.71-1.el6.x86_64                                                                                                                                                  13/13
		  Verifying  : 1:perl-Pod-Simple-3.13-141.el6_7.1.x86_64                                                                                                                                        1/13
		  Verifying  : 1:perl-Pod-Escapes-1.04-141.el6_7.1.x86_64                                                                                                                                       2/13
		  Verifying  : mysql-community-common-5.6.34-2.el6.x86_64                                                                                                                                       3/13
		  Verifying  : mysql-community-libs-5.6.34-2.el6.x86_64                                                                                                                                         4/13
		  Verifying  : 1:perl-Module-Pluggable-3.90-141.el6_7.1.x86_64                                                                                                                                  5/13
		  Verifying  : mysql-community-libs-compat-5.6.34-2.el6.x86_64                                                                                                                                  6/13
		  Verifying  : 3:perl-version-0.77-141.el6_7.1.x86_64                                                                                                                                           7/13
		  Verifying  : 2:postfix-2.6.6-6.el6_7.1.x86_64                                                                                                                                                 8/13
		  Verifying  : 4:perl-libs-5.10.1-141.el6_7.1.x86_64                                                                                                                                            9/13
		  Verifying  : mysql-community-client-5.6.34-2.el6.x86_64                                                                                                                                      10/13
		  Verifying  : 4:perl-5.10.1-141.el6_7.1.x86_64                                                                                                                                                11/13
		  Verifying  : 2:postfix-2.6.6-2.2.el6_1.x86_64                                                                                                                                                12/13
		  Verifying  : mysql-libs-5.1.71-1.el6.x86_64                                                                                                                                                  13/13

		Installed:
		  mysql-community-client.x86_64 0:5.6.34-2.el6                    mysql-community-libs.x86_64 0:5.6.34-2.el6                    mysql-community-libs-compat.x86_64 0:5.6.34-2.el6

		Dependency Installed:
		  mysql-community-common.x86_64 0:5.6.34-2.el6      perl.x86_64 4:5.10.1-141.el6_7.1           perl-Module-Pluggable.x86_64 1:3.90-141.el6_7.1      perl-Pod-Escapes.x86_64 1:1.04-141.el6_7.1
		  perl-Pod-Simple.x86_64 1:3.13-141.el6_7.1         perl-libs.x86_64 4:5.10.1-141.el6_7.1      perl-version.x86_64 3:0.77-141.el6_7.1

		Dependency Updated:
		  postfix.x86_64 2:2.6.6-6.el6_7.1

		Replaced:
		  mysql-libs.x86_64 0:5.1.71-1.el6

		Complete!


[root@ip-172-31-2-245 yum.repos.d]# ls
CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Media.repo  CentOS-Vault.repo  mysql-community.repo  mysql-community-source.repo
[root@ip-172-31-2-245 yum.repos.d]#


---------- ******** ----------

	[root@ip-172-31-2-245 yum.repos.d]# rpm -qa | grep mysql
	mysql57-community-release-el6-9.noarch
	mysql-community-common-5.6.34-2.el6.x86_64
	mysql-community-libs-compat-5.6.34-2.el6.x86_64
	mysql-community-client-5.6.34-2.el6.x86_64
	mysql-community-libs-5.6.34-2.el6.x86_64
	[root@ip-172-31-2-245 yum.repos.d]#

	[root@ip-172-31-2-246 yum.repos.d]# rpm -qa | grep mysql
	mysql-connector-java-5.1.17-6.el6.noarch
	mysql-community-common-5.6.34-2.el6.x86_64
	mysql-community-libs-compat-5.6.34-2.el6.x86_64
	mysql-community-client-5.6.34-2.el6.x86_64
	mysql57-community-release-el6-9.noarch
	mysql-community-libs-5.6.34-2.el6.x86_64
	[root@ip-172-31-2-246 yum.repos.d]#

	[root@ip-172-31-2-247 yum.repos.d]# rpm -qa | grep mysql
	mysql-connector-java-5.1.17-6.el6.noarch
	mysql-community-common-5.6.34-2.el6.x86_64
	mysql-community-libs-compat-5.6.34-2.el6.x86_64
	mysql-community-client-5.6.34-2.el6.x86_64
	mysql57-community-release-el6-9.noarch
	mysql-community-libs-5.6.34-2.el6.x86_64
	[root@ip-172-31-2-247 yum.repos.d]#

	[root@ip-172-31-2-248 yum.repos.d]# rpm -qa | grep mysql
	mysql-connector-java-5.1.17-6.el6.noarch
	mysql57-community-release-el6-9.noarch
	mysql-community-common-5.6.34-2.el6.x86_64
	mysql-community-libs-compat-5.6.34-2.el6.x86_64
	mysql-community-client-5.6.34-2.el6.x86_64
	mysql-community-libs-5.6.34-2.el6.x86_64
	[root@ip-172-31-2-248 yum.repos.d]#

	[root@ip-172-31-2-249 yum.repos.d]# rpm -qa | grep mysql
	mysql-connector-java-5.1.17-6.el6.noarch
	mysql-community-common-5.6.34-2.el6.x86_64
	mysql-community-libs-compat-5.6.34-2.el6.x86_64
	mysql-community-client-5.6.34-2.el6.x86_64
	mysql57-community-release-el6-9.noarch
	mysql-community-libs-5.6.34-2.el6.x86_64
	[root@ip-172-31-2-249 yum.repos.d]#

---------- ******** ------------

	[root@ip-172-31-2-245 etc]# /usr/bin/mysql_secure_installation



	NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MySQL
	      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

	In order to log into MySQL to secure it, we'll need the current
	password for the root user.  If you've just installed MySQL, and
	you haven't set the root password yet, the password will be blank,
	so you should just press enter here.

	Enter current password for root (enter for none):
	OK, successfully used password, moving on...

	Setting the root password ensures that nobody can log into the MySQL
	root user without the proper authorisation.

	Set root password? [Y/n] y
	New password:
	Re-enter new password:
	Password updated successfully!
	Reloading privilege tables..
	 ... Success!


	By default, a MySQL installation has an anonymous user, allowing anyone
	to log into MySQL without having to have a user account created for
	them.  This is intended only for testing, and to make the installation
	go a bit smoother.  You should remove them before moving into a
	production environment.

	Remove anonymous users? [Y/n] y
	 ... Success!

	Normally, root should only be allowed to connect from 'localhost'.  This
	ensures that someone cannot guess at the root password from the network.

	Disallow root login remotely? [Y/n] n
	 ... skipping.

	By default, MySQL comes with a database named 'test' that anyone can
	access.  This is also intended only for testing, and should be removed
	before moving into a production environment.

	Remove test database and access to it? [Y/n] y
	 - Dropping test database...
	ERROR 1008 (HY000) at line 1: Can't drop database 'test'; database doesn't exist
	 ... Failed!  Not critical, keep moving...
	 - Removing privileges on test database...
	 ... Success!

	Reloading the privilege tables will ensure that all changes made so far
	will take effect immediately.

	Reload privilege tables now? [Y/n] y
	 ... Success!




	All done!  If you've completed all of the above steps, your MySQL
	installation should now be secure.

	Thanks for using MySQL!


	Cleaning up...
	[root@ip-172-31-2-245 etc]#







