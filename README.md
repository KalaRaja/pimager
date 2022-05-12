# pimager

A simple menu driven script to flash raspberry pi OS - https://www.raspberrypi.com/software/ on linux based machines.

The menu is show below -

```
 Select Device(s)
    2. Disk /dev/sdb: 57.3 GiB, 61530439680 bytes, 120176640 sectors
    1. Disk /dev/sda: 239.02 GiB, 256641603584 bytes, 501253132 sectors


  Options
    r. Refresh device list
    w. Write image to selected device(s)
    i. Toggle incremental hostname ON
    c. Cleanup
    q. Quit

  Press a key
 ```

* You can select multiple devices and then raspberry OS will be flashed on all selected devices.
* After flashing, ssh will be enabled on all devices, hostname will be pi1, pi2 ..piN depending on number of devices selected.
* Password auth will be turned off and your public key located at $HOME/.ssh/id_rsa.pub will be added to the authorized_keys of the flashed OSes.
* If no prublic key is found at that location, a new key will be created with an empty passphrase.
* The Menu doesn't display user input and the corresponding process starts right after pressing a key.
* If you prefer to flash images one by oe in different devices, then ou can choose to have incremental hostnames pi1, pi2 ..piN. Incremental hostname option is only available when only ne device is selected.
* With incremental hostnames, you can remove the flash drive, insert another one and choose refresh and select the flash device to flash OS, the hostnames will be incremental. 
