# mt_os
Linux operating system administration. Covers Debian and RPM based distributions.

#Operating System commands and best practies

This repository contains notebooks that will assist with installation and configuration of operating systems for Linux servers, desktops and Raspberry Pi (RPi). In order to perform root level shell commands you will need to lauch the Jupyter environment with extra commands.



**Raspbian**

The notebook [00_mt_raspian_admin.ipynb](https://nbviewer.jupyter.org/github/worker-bee-micah/mt_os/blob/master/00_mt_raspbian_admin_notebook.ipynb) contains commands that can run in the browser and creates the rasbian.md which can be viewed in a browser if IPython is not installed on your system.

The default operating system for Raspberry Pi that is a Debian based destribution.
Additional settings are needed after installing onto the Pi in order to read and write from the GPIO ports.  You will need to enable i2c, SPI, SSH, and SERIAL. 


/boot/config.txt

This file has to be present or the Rpi operates with defaults.It is read when the system boots up, if you change it you will need a full restart.  This file controls almost everything, best practice is to have one option per line.  Can use this to load an emergency kernal, remove one comment, save and restart.

Disable L2 cache, designed to be used by the GPU alone.

disable_l2cache=1 #  turn back on with a zero.


Networking for the Raspberry Pi as a server for sensor arrays begins with this [notebook](www.remojo.net)
You should be able to use OpenSSH to control the RPi that interfaces with the sensor array(s). This RPi will produce a local data set and also a push to a web facing API.




**Debian**

This notebook contains system adminstration commands for deploying Debian based servers and workstations.  

>>..System startup commands, run levels, SysV scripts
>>..Network Admin, the interfaces file
>>..User Admin, groups and ACLs
>>..Firewall design
>>..Intrusion detection, file system monitors and scanners
>>..Remote backups, network and API configuration managment
>>..Hardware management


