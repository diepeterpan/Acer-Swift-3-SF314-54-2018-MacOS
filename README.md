# Acer-Swift-3-SF314-54-2018-MacOS
Use this OpenCore EFI to run MacOS on Acer Swift 3 SF314-54 (2018) 

**Now supporting MacOS Tahoe 26.0.1 / tested on 12 October 2025**

## Configuration

| Specifications | Detail                                                  |
| ------------------- | ------------------------------------------- |
| Computer model      | Acer Swift 3 SF314-54 (2018)      |
| Processor           | Intel Core i5-8250U     |
| Memory              | 8GB/20GB  DDR4 2400MHz              |
| Hard Disk           | Only tested with SATA SSD    |
| Integrated Graphics | Intel UHD Graphics 620                     |
| Monitor             | FHD 1920x1080 (14 inch) |
| Sound Card          | Realtek ALC256 (layout-id:13)           |
| Wireless Card       | Swapped with a Intel AX210                    |
| SD Card Reader      | Realtek                 |


## Current Status

### Tahoe specific:

- Currently the **USB is not mapped** and just using an **USBInjectAll.kext** specific to Tahoe, *mapping USB in Tahoe is a todo and a maybe*.

- Using **VoodooHDA** for audio as per https://github.com/chris1111/VoodooHDA-Tahoe install after upgrade to Tahoe
  <br>**(NOTE: Only the Headphone out is working for external speakers and maybe HDMI sound)**

- Using **IntelBluetooth 2.5.0** built for Tahoe see https://github.com/lshbluesky/IntelBluetoothFirmware?tab=readme-ov-file 

- Using **apfs_aligned.efi** for encrypted drive

### As is:

- **Fingerprint sensor** is not working
- **Built-in DMIC** is not working

- Everything else works well

- Brightness keys now using new .kext and working 100% with normal brightness keys **F3** and **F4**

- Ensure to edit the **config.plist** and add valid  **PlatformInfo Generic** and **SMBIOS** values

  <img src="Image1.png"/>

- Install **Captin.dmg** to have a Caps Lock indicator on screen

- Install **ComboJack** to assist with Headphones / Headset *(Don't think I am using this anymore)*

- **Apple Watch** unlock is not consitant but seems to be a generic problem on hackintoshes

- **2.4 GHz Wifi interference** with Bluetooth (mostly Bluetooth audio) also seems to be a common problem
