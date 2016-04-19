This is a script for backing up Siemens Scalamce switches.
The script logs in and connects with SSH to the switch,
then copies the current configuration to a TFTP server.
(The Scalance switches do not support a more secure protocol)

Make sure that you have expect installed on your system.
Add/change the address of the TFTP server in the script below.
Supply the hostname or IP address of the switch together with
a username and a password as arguments to the script.

There is no confirmation from within a Scalance switch to see if
the command "cfgsave" was successful.
So this script is not able to tell if the configuration backup
is actually on the TFTP server when finished.

The script can be added to Op5 or some other Nagios like system,
or automated in other ways.                                   