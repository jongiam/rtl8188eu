rtl8188eu
=========

Repository for the stand-alone RTL8188EU driver.

What's New
---------
Added vendor/hardware ID of new TP-Link TL-WN722N v2.0 (2357:010c)
Re-enabled hostapd functionality in defconfig
Fixed hlr_auc_gw compilation error (missing eloop.o in HOBJS in Makefile)


Compiling & Building
---------
### Dependencies
To compile the driver, you need to have make and a compiler installed. In addition,
you must have the kernel headers installed. If you do not understand what this means,
consult your distro.
### Compiling

> make all

### Installing

> sudo make install

DKMS
---------
The module can also be installed with DKMS. Make sure to install the `dkms` package first.

    sudo dkms add ./rtl8188eu
    sudo dkms build 8188eu/1.0
    sudo dkms install 8188eu/1.0

Submitting Issues
---------

Frequently asked Questions
---------

### The network manager says: "Device is not ready"!
Make sure you copied the firmware (rtl8188eufw.bin) to /lib/firmware/rtlwifi/

