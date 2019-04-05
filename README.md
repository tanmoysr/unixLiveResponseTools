# unixLiveResponseTools
Live Response Thumb Drive for Linux 64-bit system
NOTE
This thumbdrive/program is designed to collect volatile and non-volatile data from the suspected Linux machine. The pendrive is created using Ubuntu Linux version 18.04.2 and 16.04.3 and it is formatted to only support Ubuntu Linux ext4.

Runnig Condition: response file is for Ubuntu Linux version 18 where as responseOld is for Ubuntu Linux version 16 or earlier. The machine should be 64 bit in both version.

CONTENT OF PENDRIVE 
-data folder (empty)
-ldd_output folder (folder contains the ps_t_ldd_shared_library_analysis.txt file)
-tools folder (contains the following tools: arp_t, bash_t, date_t, hostname_t, ifconfig_t, ls_t,lsblk_t,lsusb_t, md5sum_t,mount_t, netstat_t, nstat_t, ps_t, route_t, umount_t, uname_t, whoami_t, who_t, t_arp, t_bash, t_date, t_hostname, t_ifconfig, t_ls,t_lsblk,t_lsusb, t_md5sum,t_mount, t_netstat, t_nstat, t_ps, t_route, t_umount, t_uname, t_whoami, t_who)
-readme file
-response bash file
-responseOld bash file

This pendrive can only be used on Ubuntu Linux 64 bit machine. Use response file for Ubuntu version 18 and responseOld for Ubuntu version 16 or earlier.

Steps to follow
1. Plug-in the pendrive to hte supected system
2.The pendrive will automatically mount and click on the pendrive to open
3.Right click inside the open pendrive directory and click "open terminal" inorder to open the terminal with this location : username@ubuntu:~ cd /media/device_name/pendrive
4.On the terminal type sudo chmod 777 ./response to give everyone execute permissions
5.Run the bash script by using this command; 
          username@ubuntu:~ cd /media/device_name/pendrive sudo bash ./response
6. The response bash file will run and data collected will be to saved into the data folder of the pendrive.

CONTENT OF PENDRIVE AFTER RUNNING THE BASH SCRIPT
-data folder:- (will contain the following files, access-time, arp-data, current_user, directory-data, end-time, examining_info,host_name, inod-time, ip-data, login-data, md-5, mount-data, openpoert-data, rouing table data, Running processes, start-time, system data)
		
-ldd_output folder (folder contains the t_md5sum_ldd_shared_library_analysis.txt file)
-tools folder ((contains the following tools, t_date, t_ifconfig, t_ls,t_lsblk,t_md5sum,t_mount,t_netstat,t_uname,t_who,t_route)
-readme file
-response bash file

ErrorList:
Due to different version of Ubuntu the following error can be happened.
1. /lib/x86_64-linux-gnu/libsmartcols.so.1: version `SMARTCOLS_2.30' not found (required by ./tools/lsblk_t) :It means that the OS is Ubuntu16 and the code is for Ubuntu18. So, you have to run 'responseOld' for Ubuntu16 or earlier.

2. ./tools/t_ps: error while loading shared libraries: libprocps.so.4: cannot open shared object file: No such file or directory : It means that the OS is Ubuntu18 and the code is for Ubuntu16. So, you have to run 'response' for Ubuntu18.


