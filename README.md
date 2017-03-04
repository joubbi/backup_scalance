# backup_scalance

__DO NOT USE THIS SCRIPT!__ _(and reconsider using Siemens Scalance switches)_
_There is a bug (or maybe a feature?) that reboots any Scalance switch when logging in with SSH and issuing commands interactively.
Siemes support is informed about this. They have confirmed the problem, but not fixed the problem to my knowledge._


This is a script for backing up Siemens Scalamce switches.

The script logs in and connects with SSH to the switch,
then copies the current configuration to a TFTP server.
(The Scalance switches don't support a more secure protocol)

Make sure that you have expect installed on your system.

Add/change the address of the TFTP server inside the script.

Supply the hostname or IP address of the switch together with
a username and a password as arguments to the script.


There is no confirmation from within a Scalance switch to see if
the command "cfgsave" was successful.
So this script is not able to tell if the configuration backup
is actually on the TFTP server when finished.

The script can be added to Op5 or some other Nagios like system,
or automated in other ways.

## Version history
* 1.0 2015-08-17 Initial version.
* 0.9 2015-02-16 Proof of concept.

___

Licensed under the [__Apache License Version 2.0__](https://www.apache.org/licenses/LICENSE-2.0)

Written by __farid@joubbi.se__

http://www.joubbi.se/monitoring.html

