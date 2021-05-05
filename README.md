# WakeOnLAN
It's a simple C Utility to allow RISC OS to be able to send magic packets.

In other words you can use this utility to wake up NAS devices, PC and laptops that support the WakeUp on LAN feature and that have been configured so and that are connected to the same LAN as your RISC OS device.

## Usage
You can use WakeOnLAN in two different ways:

### The command line
As soon as RISC OS Filer has seen !WakeOnLAN Application you'll be able to use it from the command line (both in regular CLI and in a TaskWindow) by typing:
```
WakeOnLAN -m <mac address> [ -b <broadcast address> ] [ -v ]
```
The parameter `-m` allows you to specify the Media Access Code (MAC) address of the device you want to wake up. The syntax is the usual mac address form like 01:02:03:04:05:06 (this parameter is NOT optional).

The parameter `-b` allows you to specify a broadcast address where to send the WOL packet. If you do not specify this parameter the default value is 192.168.0.255 (IPv4). You should use this parameter if your network is different than the default one.

Here is a practical example from the command line:
```
*WakeOnLAN -m 01:02:03:04:05:06 -b 192.168.100.255
```

### The RISC OS Desktop
If you double click on the !WakeOnLAN application, it will be loaded as a multi-task application on your icon bar. You can click on the icon bar to open the setup window and input the MAC address of the device you want to wake up and the broadcast IP of your network.

A useful thing is on the UI you can save the IP broadcast address in the !Choices file so you do not need to re-type it all the times.

The UI utilise RISC OS FrontEnd module, so make sure you have it installed before trying to run !WakeOnLAN in multi-tasking.

## Obtaining !WakeOnLAN without compiling code
If you are not keen to recompile code on RISC OS using GCC or other compilers you can find a built and ready to install !WakeOnLAN from:


## Compile WakeOnLAN from the source
Just git clone this repo on a Linux box in a directory you share with your RISC OS device and make sure you have GCC (at least 4.7.4 release or higher) installed on your RISC OS system.

Open the Shared folder with !OmniClient and get into the directory that contains this README file using the regular RISC OS Filer.

Double click on the file called MkGCC and wait until it's done :)

## Feedback

### In case of problems
For any issue you may encounter please use the Issues option here on GitHub on the top. Please do not try to contact us directly, the RISC OS Community handles all the communications here on github.

### Requesting new features
As for the problems reporting please use the Issues option here on GitHub also to request new features

### Contributing
We welcome improvements and new ideas, before you submit your changes please have a look at the Contributing Guidelines [here](CONTRIBUTING.md)

## License

WakeOnLAN is distribute under Apache License 2.0 (more details [here](LICENSE)) Please note there are some restrictions, so read the source code for more details.

Copyright (c) 2021 Paolo Fabio Zaino and contributors

Contributors:
[![Paolo](https://avatars2.githubusercontent.com/u/8824337?v=4)](https://github.com/pzaino)
