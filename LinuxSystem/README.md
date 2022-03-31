#  Linux system course

Author: Liran Cohen

Email: [liran@rct.co.il](mailto:liran@rct.co.il)


# Linux - preface and introduction

**<span style="text-decoration:underline;">Deliveries:</span>**


* What is Linux, what is it used for
* How was Linux created and why
* Linux strengths
    * Why virtually all of the servers in the world run Linux?
* Linux weaknesses
    * Why do most users use Windows?


**<span style="text-decoration:underline;">Reading materials:</span>**

* [https://www.geeksforgeeks.org/introduction-to-linux-operating-system/#:~:text=Linux%20is%20a%20community%20of,Torvalds%20on%20September%2017%2C%201991](https://www.geeksforgeeks.org/introduction-to-linux-operating-system/#:~:text=Linux%20is%20a%20community%20of,Torvalds%20on%20September%2017%2C%201991).
* [https://en.wikipedia.org/wiki/Linux](https://en.wikipedia.org/wiki/Linux)
* [https://renewablepcs.wordpress.com/about-linux/advantages-of-using-linux/](https://renewablepcs.wordpress.com/about-linux/advantages-of-using-linux/)

**<span style="text-decoration:underline;">Timing:</span>**


* DIY: 1.5h
* Frontal


# User mode / Kernel mode

**<span style="text-decoration:underline;">Deliveries:</span>**

* User mode / Kernel mode differences
    * security & privileges
    * syscalls & interrupts


**<span style="text-decoration:underline;">Reading materials:</span>**

* [https://www.geeksforgeeks.org/user-mode-and-kernel-mode-switching/](https://www.geeksforgeeks.org/user-mode-and-kernel-mode-switching/)
    * Don't get too hanged up on how a cpu works if you don't know assembly, just get a basic understanding of the flow.
* [https://blog.codinghorror.com/understanding-user-and-kernel-mode/](https://blog.codinghorror.com/understanding-user-and-kernel-mode/)

**<span style="text-decoration:underline;">Timing:</span>**


* DIY: 1.5h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**
* Explain to your module trainer the workflow of a user space process that communicates with hardware (sends data through the network, writes files to disk, etc.).


# Linux flavours and terminology

**<span style="text-decoration:underline;">Deliveries:</span>**

* Unix philosophy
    * Do One Thing and Do It Well
    * Everything is a file
* GNU, GCC and POSIX
* Unix
    * How is Linux and BSD related to unix
    * Linux vs BSD
* Differences between linux distros

**<span style="text-decoration:underline;">Reading materials:</span>**

* https://hackaday.com/2018/09/10/doing-one-thing-well-the-unix-philosophy/
* https://unix.stackexchange.com/questions/141016/a-laymans-explanation-for-everything-is-a-file-what-differs-from-windows
* [https://opensource.com/article/19/7/what-posix-richard-stallman-explains](https://opensource.com/article/19/7/what-posix-richard-stallman-explains)
* [https://opensource.com/article/18/5/differences-between-linux-and-unix](https://opensource.com/article/18/5/differences-between-linux-and-unix)
* https://stackoverflow.com/questions/3403938/whats-the-relationship-between-a-linux-os-and-a-kernel

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**

* Write down the biggest differences for a sysadmin that is used to RHEL when he works with Ubuntu


# The Linux boot process

**<span style="text-decoration:underline;">Deliveries:</span>**



* Understand the linux boot process
    * BIOS/UEFI - just know that it exists
    * MBR/GPT - briefly
    * Boot manager (GRUB)
    * Initrd
    * Systemd (targets)

**<span style="text-decoration:underline;">Reading materials:</span>**



* <span style="text-decoration:underline;">https://opensource.com/article/17/2/linux-boot-and-startup</span>
* [https://en.wikipedia.org/wiki/GUID_Partition_Table](https://en.wikipedia.org/wiki/GUID_Partition_Table) (up to and including history title)
* [https://www.howtogeek.com/56958/htg-explains-how-uefi-will-replace-the-bios/](https://www.howtogeek.com/56958/htg-explains-how-uefi-will-replace-the-bios/) (up to and including how to access uefi on modern pcs)

**<span style="text-decoration:underline;">Timing:</span>**



1. DIY: 2h
2. Frontal


# Systemd

**<span style="text-decoration:underline;">Deliveries:</span>**

* Sysv init (legacy)
* Systemd concepts
    * Units
        * Targets
        * Services
* Journalctl
     * flags
        * -k
        * -u
        * -xe
* Systemctl
    * enable
    * status
    * stop
    * start
    * restart

**<span style="text-decoration:underline;">Reading materials:</span>**


* [https://www.liquidweb.com/kb/linux-runlevels-explained/](https://www.liquidweb.com/kb/linux-runlevels-explained/)
* [https://en.wikipedia.org/wiki/Systemd](https://en.wikipedia.org/wiki/Systemd)
* [https://www.linux.com/training-tutorials/understanding-and-using-systemd/](https://www.linux.com/training-tutorials/understanding-and-using-systemd/)
* [https://trstringer.com/effective-journalctl/](https://trstringer.com/effective-journalctl/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2.5h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Create a systemd service running the command: ls -l
* Output should be visible in /var/log/messages


# Rebooting and shutting down

**<span style="text-decoration:underline;">Deliveries:</span>**

* shutdown
* reboot

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.ionos.com/digitalguide/server/configuration/linux-shutdown-command/](https://www.ionos.com/digitalguide/server/configuration/linux-shutdown-command/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 0.5h

**<span style="text-decoration:underline;">Drill:</span>**



* Protect your linux machine from attackers by scheduling a shutdown at exactly 18:59


#  Kernel modules

**<span style="text-decoration:underline;">Deliveries:</span>**



* Insmod
* lsmod
* rmmod
* Modprobe
* Dkms vs binary module

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://wiki.archlinux.org/index.php/Kernel_module#:~:text=Kernel%20modules%20are%20pieces%20of,as%20built%2Din%20or%20loadable](https://wiki.archlinux.org/index.php/Kernel_module#:~:text=Kernel%20modules%20are%20pieces%20of,as%20built%2Din%20or%20loadable)
* [https://wiki.archlinux.org/index.php/Dynamic_Kernel_Module_Support](https://wiki.archlinux.org/index.php/Dynamic_Kernel_Module_Support)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 0.75h
* Frontal



# The logon \ Logout process

**<span style="text-decoration:underline;">Deliveries:</span>**

* Login process
    * getty/agetty
    * Profile
    * Bashrc

**<span style="text-decoration:underline;">Reading materials:</span>**

* [https://www.linuxnix.com/how-login-process-work-in-linux](https://www.linuxnix.com/how-login-process-work-in-linux)
* [https://www.theunixschool.com/2011/07/what-is-profile-file.html?m=1](https://www.theunixschool.com/2011/07/what-is-profile-file.html?m=1)
* [https://www.journaldev.com/41479/bashrc-file-in-linux](https://www.journaldev.com/41479/bashrc-file-in-linux)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Change the bash prompt to: "LIVE - [\u@\h \W]\\$ "


# Text editors Vim, nano

**<span style="text-decoration:underline;">Deliveries:</span>**


* Vim
    * open
    * save
    * exit
* nano
    * open
    * save
    * exit

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.shell-tips.com/linux/vi-vs-vim/#:~:text=Vi%20stands%20for%20Visual.,Vi%20standard%20with%20many%20additions](https://www.shell-tips.com/linux/vi-vs-vim/#:~:text=Vi%20stands%20for%20Visual.,Vi%20standard%20with%20many%20additions)<span style="text-decoration:underline;">.</span>
* [https://vimhelp.org/vim_faq.txt.html#faq-1.4](https://vimhelp.org/vim_faq.txt.html#faq-1.4)
* [https://www.howtogeek.com/howto/42980/the-beginners-guide-to-nano-the-linux-command-line-text-editor/](https://www.howtogeek.com/howto/42980/the-beginners-guide-to-nano-the-linux-command-line-text-editor/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 0.5h
* No frontal


# Vi intro

**<span style="text-decoration:underline;">Deliveries:</span>**

* Moving in vi
* Familiarity:
    * grep regex
    * Vi regex SnR

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://developer.ibm.com/tutorials/l-vi/](https://developer.ibm.com/tutorials/l-vi/)
* <span style="text-decoration:underline;">https://www.codingcommanders.com/linux/vi-intro.html</span>

* [http://vimregex.com/](http://vimregex.com/)
* [https://www.cyberciti.biz/faq/grep-regular-expressions/](https://www.cyberciti.biz/faq/grep-regular-expressions/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 3h
* Frontal: 0.5h

**<span style="text-decoration:underline;">Drill:</span>**

* run `sudo yum install vim-enhanced` and then `vimtutor`, finish vimtutor

# Nsswitch.conf

**<span style="text-decoration:underline;">Deliveries:</span>**



* Name service switch
* Different switching options (files, nis, ldap, ddns)
* Different service options (hosts, groups, services etc.)

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://en.wikipedia.org/wiki/Name_Service_Switch](https://en.wikipedia.org/wiki/Name_Service_Switch)
* [https://searchitchannel.techtarget.com/feature/Using-nsswitchconf-to-find-Linux-system-information](https://searchitchannel.techtarget.com/feature/Using-nsswitchconf-to-find-Linux-system-information)
* [https://developers.redhat.com/blog/2018/11/26/etc-nsswitch-conf-non-complexity](https://developers.redhat.com/blog/2018/11/26/etc-nsswitch-conf-non-complexity)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Change order host resolution is performed to dns first and then hosts file.


# Permissions, Theory, Ownership

**<span style="text-decoration:underline;">Deliveries:</span>**

* Familiarity:
    * File permissions
    * Directory permissions
    * umask
    * chmod
    * chown
    * chgrp

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.pluralsight.com/blog/it-ops/linux-file-permissions](https://www.pluralsight.com/blog/it-ops/linux-file-permissions)
* [https://www.guru99.com/file-permissions.html](https://www.guru99.com/file-permissions.html)
* [https://www.cyberciti.biz/tips/understanding-linux-unix-umask-value-usage.html](https://www.cyberciti.biz/tips/understanding-linux-unix-umask-value-usage.html)
* https://unix.stackexchange.com/questions/21251/execute-vs-read-bit-how-do-directory-permissions-in-linux-work

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2.5h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Create a new directory and an empty file inside it
    * Change permissions of the file to be readable only by the root user
    * Change the directory permissions to be accessible only by the wheel group
* Create a file
    * Change its permissions to 007
    * What are the effective permissions of your user on the file?


# Account management

**<span style="text-decoration:underline;">Deliveries:</span>**



* Home directories
* User
    * useradd
    * userdel
    * usermod
* Group
    * groupadd
    * groupdel
    * groupmod
    * gpasswd
        * (just know that it exists)

**<span style="text-decoration:underline;">Reading materials:</span>**

* [https://www.theunixschool.com/2011/07/what-is-profile-file.html?m=1](https://www.theunixschool.com/2011/07/what-is-profile-file.html?m=1)
* [https://www.journaldev.com/41479/bashrc-file-in-linux](https://www.journaldev.com/41479/bashrc-file-in-linux)
* [No need to read "Understanding Setuid" and below](https://www.tecmint.com/manage-users-and-groups-in-linux/)
* [https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/ch-managing_users_and_groups](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/ch-managing_users_and_groups)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1h
* Frontal

# Root directories

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarity with the linux directory structure
* Know the reasons for the different directories

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.howtogeek.com/117435/htg-explains-the-linux-directory-structure-explained/](https://www.howtogeek.com/117435/htg-explains-the-linux-directory-structure-explained/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1h
* Frontal


# in system help and documentation

**<span style="text-decoration:underline;">Deliveries:</span>**



* Commands familiarity:
    * Man

**<span style="text-decoration:underline;">Reading materials:</span>**



* <span style="text-decoration:underline;">Run ‘man man’</span>

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1h


# Working with a terminal command line

**<span style="text-decoration:underline;">Deliveries:</span>**



* Commands familiarity:
    * Pwd
    * cd
    * ls
    * w
    * who
    * clear
    * screen

**<span style="text-decoration:underline;">Reading materials:</span>**



* <span style="text-decoration:underline;">Man &lt;command></span>

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 0.5h
* Frontal


# File manipulation commands

**<span style="text-decoration:underline;">Deliveries:</span>**



* Commands familiarity:
    * cp
    * mv
    * rm
    * tar
    * gzip
    * du
    * find
    * locate
    * which
    * whereis

**<span style="text-decoration:underline;">Reading materials:</span>**



* <span style="text-decoration:underline;">Man &lt;command></span>

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1.5h
* Frontal


# Basic Text manipulation commands

**<span style="text-decoration:underline;">Deliveries:</span>**



* Commands familiarity:
    * grep
      * -A
      * -B
      * --Exec
    * less
    * more
    * cat
    * jq
    * uniq
    * sort
    * tail
    * head
    * cut
    * wc
    * Don't go in depth:
        * awk
        * sed

**<span style="text-decoration:underline;">Reading materials:</span>**



* <span style="text-decoration:underline;">Man &lt;command></span>

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2.5h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**

* Use the command sudo yum install -y words to install a words file. It is now located at /usr/share/dict/words
    * Display the top 27 lines of the words file
    * Display the bottom 30 lines of the words file
    * Which flag is needed in order to open a file using tail in a continuous mode?
    * List the number of lines of the words file
    * Print the words file to screen but change every occurrence of A to Alpha

    * Print the the screen only the first column of the file /etc/fstab using both cut and awk

    * What is the difference between more and less?
    * Print to the screen only the lines that contain the string abc (from the words file)

# System administration commands

**<span style="text-decoration:underline;">Deliveries:</span>**



* Commands familiarity:
    * hostname
      * systemd has hostnamectl, similar, just know it exists
    * watch
    * lsof
    * free
    * lspci
    * uname
    * whoami
    * date
      * systemd has timedatectl, similar, just know it exists
    * dmesg
        * same as journalctl -k

**<span style="text-decoration:underline;">Reading materials:</span>**



* <span style="text-decoration:underline;">Man &lt;command></span>

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2.5h
* Frontal

# Process Control and troubleshooting

**<span style="text-decoration:underline;">Deliveries:</span>**

* strace
* top
    * Explain **all** of the parameters you see in the command (2.5h)
    * Explain how each can be used to identify issues and unusual behaviours in your machine
* vmstat
    * Explain si so and bi bo (the rest you already know from top)
* Briefly
    * nmon
    * htop
    * ps
    * pstree

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.howtoforge.com/linux-pstree-command/](https://www.howtoforge.com/linux-pstree-command/)
* [https://www.geeksforgeeks.org/ps-command-in-linux-with-examples/](https://www.geeksforgeeks.org/ps-command-in-linux-with-examples/)
* [https://www.booleanworld.com/guide-linux-top-command/](https://www.booleanworld.com/guide-linux-top-command/)
* [https://www.techrepublic.com/article/how-to-monitor-your-linux-servers-with-nmon/](https://www.techrepublic.com/article/how-to-monitor-your-linux-servers-with-nmon/)
* [https://www.howtogeek.com/howto/ubuntu/using-htop-to-monitor-system-processes-on-linux/](https://www.howtogeek.com/howto/ubuntu/using-htop-to-monitor-system-processes-on-linux/)
* [https://www.tecmint.com/strace-commands-for-troubleshooting-and-debugging-linux/](https://www.tecmint.com/strace-commands-for-troubleshooting-and-debugging-linux/)
* Supplement with man

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 4h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**
* Show all of the files which a process opens
* Show a summary of all the syscalls a process has made

# File system concepts, inodes

**<span style="text-decoration:underline;">Deliveries:</span>**


* Inodes
* Familiarity:
    * Ext (->4)
    * Xfs

**<span style="text-decoration:underline;">Reading materials:</span>**


* [https://www.howtogeek.com/465350/everything-you-ever-wanted-to-know-about-inodes-on-linux/](https://www.howtogeek.com/465350/everything-you-ever-wanted-to-know-about-inodes-on-linux/)
* [https://opensource.com/article/18/4/ext4-filesystem](https://opensource.com/article/18/4/ext4-filesystem)
* [http://landoflinux.com/linux_xfs_filesystem_introduction.html](http://landoflinux.com/linux_xfs_filesystem_introduction.html)


**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2.5h
* Frontal

# Special files and directories

**<span style="text-decoration:underline;">Deliveries:</span>**



* familiarity:
    * Everything is a file
    * Directories
    * Devices
    * Sockets
    * Named pipes
    * Links
        * hard link
        * symbolic link

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.livefirelabs.com/unix_tip_trick_shell_script/unix_operating_system_fundamentals/file-types-in-unix.htm#:~:text=READ%20MORE%20%3E%3E-,Device%20(Special)%20Files,files%20and%20block%20special%20files](https://www.livefirelabs.com/unix_tip_trick_shell_script/unix_operating_system_fundamentals/file-types-in-unix.htm#:~:text=READ%20MORE%20%3E%3E-,Device%20(Special)%20Files,files%20and%20block%20special%20files)<span style="text-decoration:underline;">.</span>
* [https://en.wikipedia.org/wiki/Unix_file_types](https://en.wikipedia.org/wiki/Unix_file_types)
* [https://www.geeksforgeeks.org/soft-hard-links-unixlinux/](https://www.geeksforgeeks.org/soft-hard-links-unixlinux/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2.5h
* Frontal


# Piping and I/O redirection

**<span style="text-decoration:underline;">Deliveries:</span>**


* STDIN, STDOUT, STDERR
* Write output to file
* Read from file
* Append to file
* Pipe output to another command

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.guru99.com/linux-redirection.html](https://www.guru99.com/linux-redirection.html)
* [https://www.digitalocean.com/community/tutorials/an-introduction-to-linux-i-o-redirection](https://www.digitalocean.com/community/tutorials/an-introduction-to-linux-i-o-redirection)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1h
* Frontal


**<span style="text-decoration:underline;">Drill:</span>**
* print the first 100 lines in /var/log/secure file in reverse sort (first in order is last)
* the command should be in one line.

**<span style="text-decoration:underline;">Drill:</span>**

* explain following command: `cp ./file1 ./dir1/ >> cp-out.txt 2>&1`



# File-system utilities

**<span style="text-decoration:underline;">Deliveries:</span>**

  * fdisk
  * mount
    * fstab
  * df
  * Just know that it exists
    * lsblk
    * mkfs
    * tune2fs
    * fsck
    * smartctl


**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.2daygeek.com/linux-fdisk-command-to-manage-disk-partitions/](https://www.2daygeek.com/linux-fdisk-command-to-manage-disk-partitions/)
* [https://www.tecmint.com/linux-disk-scanning-tools/](https://www.tecmint.com/linux-disk-scanning-tools/)
* [https://www.howtogeek.com/howto/38125/htg-explains-what-is-the-linux-fstab-and-how-does-it-work/](https://www.howtogeek.com/howto/38125/htg-explains-what-is-the-linux-fstab-and-how-does-it-work/)

**<span style="text-decoration:underline;">Timing:</span>**



1. DIY: 2h
2. Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Create a new partition
* Format the partition using XFS
* Mount the new partition you create at the /data mount point





# The super-user (root)

**<span style="text-decoration:underline;">Deliveries:</span>**



* The root user
* The wheel group
* su
* sudo
* Setuid (suid)
* Setgid (sgid)
* Sticky bit
* /etc/sudoers

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.cyberciti.biz/faq/linux-login-as-super-user/](https://www.cyberciti.biz/faq/linux-login-as-super-user/)
* [https://mediatemple.net/community/products/dv/204643890/an-introduction-to-the-root-user#:~:text=The%20root%20is%20the%20user,root%20user%2C%20and%20the%20superuser](https://mediatemple.net/community/products/dv/204643890/an-introduction-to-the-root-user#:~:text=The%20root%20is%20the%20user,root%20user%2C%20and%20the%20superuser)
* [https://www.liquidweb.com/kb/how-do-i-set-up-setuid-setgid-and-sticky-bits-on-linux/](https://www.liquidweb.com/kb/how-do-i-set-up-setuid-setgid-and-sticky-bits-on-linux/)
* [https://www.linuxnix.com/suid-set-suid-linuxunix/](https://www.linuxnix.com/suid-set-suid-linuxunix/)
* [https://wiki.debian.org/sudo](https://wiki.debian.org/sudo)
* [https://phoenixnap.com/kb/linux-sudo-command#:~:text=Sudo%20stands%20for%20SuperUser%20DO,sensitive%20files%20from%20being%20compromised](https://phoenixnap.com/kb/linux-sudo-command#:~:text=Sudo%20stands%20for%20SuperUser%20DO,sensitive%20files%20from%20being%20compromised)<span style="text-decoration:underline;">.</span>


**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2.5h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**


* Create a new user
* Allow the user to install packages (yum)

**<span style="text-decoration:underline;">Drill:</span>**

* Add sticky bit to file, who can edit the file now?


# Linux attributes

**<span style="text-decoration:underline;">Deliveries:</span>**

* What are linux attributes?
    * No need to remember them, just immutable
* lsattr
* chattr

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://linuxize.com/post/chattr-command-in-linux/](https://linuxize.com/post/chattr-command-in-linux/)
* [https://sudoedit.com/linux-file-attributes/](https://sudoedit.com/linux-file-attributes/)
* [https://medium.com/for-linux-users/linux-file-attributes-made-easy-8d100c0a5813](https://medium.com/for-linux-users/linux-file-attributes-made-easy-8d100c0a5813)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Create a file
* Make the file resilient for deletion by users (except root)
* Make file immune to time changes (not change the modification time




# SElinux in a nutshell

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarity:
    * getenforce
    * setenforce
    * sestatus
    * ls -Z
    * /etc/selinux/config

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.linode.com/docs/guides/a-beginners-guide-to-selinux-on-centos-7/](https://www.linode.com/docs/guides/a-beginners-guide-to-selinux-on-centos-7/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2.5h
* Frontal


# Bash Environment and other startup files

**<span style="text-decoration:underline;">Deliveries:</span>**

  * env
  * echo
  * unset
  * PATH
  * History
  * Shortcuts
      * Ctrl+R
      * Ctrl+A
      * Ctrl+E
      * Ctrl+D
      * Ctrl+W
      * Ctrl+C

**<span style="text-decoration:underline;">Reading materials:</span>**


* [https://cs.lmu.edu/~ray/notes/bash/](https://cs.lmu.edu/~ray/notes/bash/)
* [https://www.digitalocean.com/community/tutorials/how-to-read-and-set-environmental-and-shell-variables-on-linux](https://www.digitalocean.com/community/tutorials/how-to-read-and-set-environmental-and-shell-variables-on-linux)
* [https://www.geeksforgeeks.org/echo-command-in-linux-with-examples/#:~:text=echo%20command%20in%20linux%20is,the%20screen%20or%20a%20file](https://www.geeksforgeeks.org/echo-command-in-linux-with-examples/#:~:text=echo%20command%20in%20linux%20is,the%20screen%20or%20a%20file)<span style="text-decoration:underline;">.</span>
* [https://www.gnu.org/software/bash/manual/html_node/Bash-Startup-Files.html](https://www.gnu.org/software/bash/manual/html_node/Bash-Startup-Files.html)
* [https://www.digitalocean.com/community/tutorials/how-to-use-bash-history-commands-and-expansions-on-a-linux-vps#:~:text=Bash%20allows%20you%20to%20adjust,memory%20for%20the%20current%20session](https://www.digitalocean.com/community/tutorials/how-to-use-bash-history-commands-and-expansions-on-a-linux-vps#:~:text=Bash%20allows%20you%20to%20adjust,memory%20for%20the%20current%20session)<span style="text-decoration:underline;">.</span>
* [https://ostechnix.com/list-useful-bash-keyboard-shortcuts/](https://ostechnix.com/list-useful-bash-keyboard-shortcuts/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h
* Frontal


# Basic shell scripts

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarity:
    * Sha-bang format
    * Bash variables
    * Bash conditionals
    * Bash loops

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://livecodestream.dev/post/introduction-to-bash-for-beginners/](https://livecodestream.dev/post/introduction-to-bash-for-beginners/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 4h

**<span style="text-decoration:underline;">Drill:</span>**



* Finish all the exercises in [https://www.learnshell.org/en/Welcome](https://www.learnshell.org/en/Welcome)


# Scheduling work

**<span style="text-decoration:underline;">Deliveries:</span>**

* Crontab
* at

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://linoxide.com/linux-how-to/schedule-job-linux-commands/#:~:text=Job%20scheduling%20is%20a%20feature,a%20pre%2Ddetermined%20time%20schedule](https://linoxide.com/linux-how-to/schedule-job-linux-commands/#:~:text=Job%20scheduling%20is%20a%20feature,a%20pre%2Ddetermined%20time%20schedule)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 0.5h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Run the backup script you created earlier and make sure it runs ever 20 minutes
* Make the backup script run at 2am


# Software packages

**<span style="text-decoration:underline;">Deliveries:</span>**



* rpm
* yum
* just know that it exists
    * dnf
    * apt
    * apk


**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://access.redhat.com/solutions/1189](https://access.redhat.com/solutions/1189)
* [https://access.redhat.com/solutions/9934](https://access.redhat.com/solutions/9934)
* [https://access.redhat.com/articles/yum-cheat-sheet](https://access.redhat.com/articles/yum-cheat-sheet)
* [https://webhome.phy.duke.edu/~rgb/General/yum_HOWTO/yum_HOWTO/yum_HOWTO-1.html](https://webhome.phy.duke.edu/~rgb/General/yum_HOWTO/yum_HOWTO/yum_HOWTO-1.html)


**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1.5h


# Networking basics

**<span style="text-decoration:underline;">Deliveries:</span>**



* ARP
* Ip (protocol)
* Ip (command)
* Tcp
* Udp
* Routing
* Default gateway
* Netstat
* Telnet
* Netcat
* nmcli
    * Open /etc/sysconfig/network-scripts, open a script and read it (on RHEL/CentOS)

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.cloudflare.com/learning/network-layer/internet-protocol/](https://www.cloudflare.com/learning/network-layer/internet-protocol/)
* [https://www.techrepublic.com/article/understand-the-basics-of-linux-routing/#:~:text=On%20Linux%20and%20UNIX%20systems,both%20static%20and%20dynamic%20routing](https://www.techrepublic.com/article/understand-the-basics-of-linux-routing/#:~:text=On%20Linux%20and%20UNIX%20systems,both%20static%20and%20dynamic%20routing)<span style="text-decoration:underline;">.</span>
* [https://www.tecmint.com/20-netstat-commands-for-linux-network-management/](https://www.tecmint.com/20-netstat-commands-for-linux-network-management/)
* [https://www.varonis.com/blog/netcat-commands/](https://www.varonis.com/blog/netcat-commands/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 3.5h
* Frontal

# Network file-system (nfs)

**<span style="text-decoration:underline;">Deliveries:</span>**

* /etc/exports
* Exportfs
* Mount -t nfs

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/nfs-serverconfig](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/nfs-serverconfig)
* [https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/nfs-clientconfig#s2-nfs-fstab](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/nfs-clientconfig#s2-nfs-fstab)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h

**<span style="text-decoration:underline;">Drill:</span>**



* Add an NFS mount to your fstab


# SSH

**<span style="text-decoration:underline;">Deliveries:</span>**

* Ssh
* Scp
* Remote command execution
* Ssh host key
* ssh-keygen
* ssh-copy-id
* .ssh directory
* rsync

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://opensource.com/article/20/9/ssh](https://opensource.com/article/20/9/ssh)
* [https://dev.to/risafj/ssh-key-authentication-for-absolute-beginners-in-plain-english-2m3f](https://dev.to/risafj/ssh-key-authentication-for-absolute-beginners-in-plain-english-2m3f)
* [https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories](https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Generate an RSA key and configure a passwordless login to a remote server
* Synchronize a directory with a remote server


# LVM - Logical volume manager

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarity:
    * Pv
    * Lv
    * Vg
    * vgs
    * vgs
    * lvs
    * Resizing lv
    * Extending vg

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.digitalocean.com/community/tutorials/an-introduction-to-lvm-concepts-terminology-and-operations](https://www.digitalocean.com/community/tutorials/an-introduction-to-lvm-concepts-terminology-and-operations)
* [https://www.thegeekdiary.com/redhat-centos-a-beginners-guide-to-lvm-logical-volume-manager/](https://www.thegeekdiary.com/redhat-centos-a-beginners-guide-to-lvm-logical-volume-manager/)
* [https://www.thegeekdiary.com/centos-rhel-how-to-extend-physical-volume-in-lvm-by-extending-the-disk-partition-used/](https://www.thegeekdiary.com/centos-rhel-how-to-extend-physical-volume-in-lvm-by-extending-the-disk-partition-used/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 3h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Extend a vg and adjust the lv accordingly to the max vg size
