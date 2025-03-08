## Linux Privilege Escalation

There are 3 sets of permissions, 1 each for: 
- owner
- members of the file's group
- everyone else

Uses of chmod command in linux:

https://www.howtogeek.com/437958/how-to-use-the-chmod-command-on-linux/

To set the setuid bit, use the following command:
- chmod u+s 

https://forums.justlinux.com/showthread.php?98125-chmod-u-s

The setuid bit: This bit is present for files which have executable permissions. The setuid bit simply indicates that when running the executable, it will set its permissions to that of the user who created it (owner), instead of setting it to the user who launched it. 

# Tcpdump manual

https://www.tcpdump.org/manpages/tcpdump.1.html

-z postrotate-command
Used in conjunction with the -C or -G options, this will make tcpdump run " postrotate-command file " where file is the savefile being closed after each rotation. For example, specifying -z gzip or -z bzip2 will compress each savefile using gzip or bzip2.
Note that tcpdump will run the command in parallel to the capture, using the lowest priority so that this doesn't disturb the capture process.
And in case you would like to use a command that itself takes flags or different arguments, you can always write a shell script that will take the savefile name as the only argument, make the flags & arguments arrangements and execute the command that you want.

## Operating system

User mode & kernel mode

Kernel has control over the entire computer and handles all input and output requests.

Hardware Abstraction Layer handles all communication between kernel and hardware.
