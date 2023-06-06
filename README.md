  File: XSIBackup-App_1.0.0.1.tar.gz  
CRC-32: 92b9fd0f
   MD4: f246155e7a09b8eec1cfd23afff25704
   MD5: 0f5760fc7586f82408000482ce60b4e6
 SHA-1: a0ec124a7a3a8cdef2f00757e3369d0dcad4470e
 
Download also from sourceforge.net:
https://sourceforge.net/projects/xsibackup-app/

The default root password is 'xsibackup'.

Change log: https://33hops.com/xsibackup-datacenter-change-log.html

Run the binary invoking 'xsibackup'.
Run the nCurses GUI invoking 'xsibackup-gui'.

This appliance contains ©XSIBackup 2.0, which is capable of backing up VMs 
in any ©ESXi server reachable over IP/SSH. The set of arguments and flags 
is exactly the same as in previous version of (c)XSIBackup-DC/ Pro, but 
some new arguments have been added to allow accessing and backing up VMs in 
other hosts.

This is the manual for (c)XSIBackup, all commands apply.
https://33hops.com/xsibackup-dc-full-manual-home.html

Please read this post where specific arguments are explained:
https://33hops.com/xsibackup-2-what-is-new.html


INSTALLATION

The virtual machine is Hardware Version 9, you should be able to uncompress 
and register the .tar.gz package directly to any ©ESXi version above or 
equal to 5.1.

You can use any command line Linux SCP client or some Windows tool such as 
WinSCP, Filezilla, etc... able to use SCP or SFTP.

SCP the .tar.gz file to the root of some data store you want to install the 
appliance to and run:

tar -xvf XSIBackup-App_1.0.0.0.tar.gz

The appliance will be uncompressed in its own folder. Register, switch the VM 
on and when prompted answer you copied the VM (this is to generate a new UID 
and MAC).

The appliance comes preconfigured with 2 CPUs and 2 GB of RAM. This will be 
enough for most scenarios with small to medium sized VMs, nonetheless, you 
can tweak the appliance to suit your needs and increase memory and/or CPUs.


USAGE:

1/ Add one or more backup hosts.
2/ Add one or more backup servers "Key exchange" menu entry.
3/ Create some job.
4/ Run the job from the GUI.
5/ Schedule the job in the cron.

(*) Jobs running detached from a TTY run faster than jobs run in the shell.
(**) Jobs run from the shell (command line) run faster than jobs run 
from the GUI.


LICENSING:

Trial license allows to use all functions for a limited period of time. The  
free period end date will depend on when you downloaded the appliance. Once 
the trial period is over you will still be able to backup VMs up to 100GB 
to local storage.

Licensing an installation is also the same as doing it in ©XSIBackup 
directly installed in ©ESXi. The only consideration is that you also have to
indicate the backup host for which you want to generate your request.key file.

xsibackup --request-key --backup-host=a.b.c.d

Previous license files are not valid. You can use the appliance's license 
files in multiple instances of the appliance, each license covers one host 
from an unlimited number of appliance instances.
