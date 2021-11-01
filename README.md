# WakeOnLAN
WakeOnLAN is a simple C Utility that allows RISC OS to send magic Wake-on-LAN packets.

In other words you can use this utility to wake up NAS devices, PCs and laptops that support the Wake-on-LAN feature. Each remote device will likely require this feature to be enabled, typically in the BIOS. Remote devices will also need to be connected to the same LAN as your RISC OS device.

## Tutorial
A short [YouTube tutorial](https://youtu.be/DITiZoxlEBg) is available demonstrating how to use this utility.

## Usage
You can use WakeOnLAN in two different ways:

### The command line
As soon as RISC OS Filer has seen the !WakeOnLAN Application you will be able to use it from the command line (both in regular CLI and in a TaskWindow) by typing:
```
WakeOnLAN -m <mac address> [ -b <broadcast address> ] [ -v ]
```
The parameter `-m` allows you to specify the Media Access Code (MAC) address of the device you want to wake up. The syntax is in the usual MAC address form such as 01:02:03:04:05:06 (this parameter is NOT optional).

The parameter `-b` allows you to specify a broadcast address where to send the Wake-on-LAN (WOL) packet. If you do not specify this parameter the default value is 192.168.0.255 (IPv4). You should use this parameter if your network configuration is different to the default one.

Here is a practical example from the command line:
```
*WakeOnLAN -m 01:02:03:04:05:06 -b 192.168.100.255
```

### The RISC OS Desktop
If you double-click on the !WakeOnLAN application, it will be loaded as a multi-tasking application on the icon bar. You can click the icon bar icon to open the setup window and input the MAC address of the device to wake up along with the broadcast IP address of your network.

In the UI you can save the IP broadcast address to the !Choices file to eliminate the need to re-type it all the time.

*Note:* The UI makes use of the RISC OS FrontEnd module, so make sure you have it installed before trying to run !WakeOnLAN in multi-tasking mode.

## Obtaining !WakeOnLAN without compiling code
If you are not keen to recompile code on RISC OS using GCC or other compilers you can find a pre-built and ready to install !WakeOnLAN from:

## Compile WakeOnLAN from the source
Using git, clone this repository on a Linux box in a directory shared with your RISC OS device and make sure you have GCC (at least 4.7.4 release or higher) installed on your RISC OS system.

Open the Shared folder with !OmniClient and navigate to the directory that contains this README file using the regular RISC OS Filer.

Double click on the file called MkGCC and wait until it is done :)

## Feedback

### In case of problems
For any issue you may encounter please use the [Issues](https://github.com/RISC-OS-Community/WakeOnLAN/issues) option here on GitHub. Please do not try to contact us directly as all RISC OS Community communication is handled here on GitHub.

### Requesting new features
New features are also to be requested via [Issues](https://github.com/RISC-OS-Community/WakeOnLAN/issues) on GitHub. Create a new issue using the [New issue](https://github.com/RISC-OS-Community/WakeOnLAN/issues/new/choose) button and choose the 'New Requirement' template.

### Contributing
We welcome improvements and new ideas, before you submit your changes please have a look at the Contributing Guidelines [here](CONTRIBUTING.md)

## License

WakeOnLAN is distribute under Apache License 2.0 (more details [here](LICENSE)) Please note there are some restrictions, so read the source code for more details.

Copyright (c) 2021 Paolo Fabio Zaino and contributors

Contributors:

[![Paolo](https://avatars2.githubusercontent.com/u/8824337?s=42&v=4)](https://github.com/pzaino)
