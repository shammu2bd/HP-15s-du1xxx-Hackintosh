# HP-15s-du1xxx-Hackintosh
HP-15s-du1xxx Hackintosh working Opencore EFI with macOS 26 Tahoe
- **Bootloader:** OpenCore 1.0.8
- **macOS:** 26.7.1 Tahoe

# Changelog

### Update: 20-Oct-2026
- Initial release

# Specification:
- **MainBoard:** HP-15s-du1xxx
- **Processor:** Core i5-10210U (Comet Lake) 1.60 GHz base clock with up to 4.20 GHz max turbo frequency
- **RAM:** 16GB DDR4 2400mhz (Duel channel 2x2)
- **Graphic:** 
  + Intel UHD Graphics 620
  + No dGPU
- **Network:**
  + **Wifi:** RTL8821ce Wi-Fi 5 (802.11ac) 1x1
  + **Bluetooth:** Realtek Bluetooth 4.2
  + **Ethernet:** Realtek RTL8111 PCI gigabit ethernet
- **Audio:** Realtek ALC236
- **Touchpad:** ELAN I2C-HID
- **SD Card Reader** Realtek card reader
- **Storage**: 256GB NVME SSD, 1TB HDD

# WORKING:
- [x] Power Management
- [x] Intel UHD Graphics 620
- [x] Built-in Wifi (Realtek RTL8821ce) **(No OCLP patch needed)**
- [x] Built-in Bluetooth
- [x] Sound **(Internal Speaker and Headphone working)**
- [x] Mic **(Internal and External both working)**
- [x] SD Card Reader
- [x] Ethernet
- [x] Adjust brightness 
- [x] USB 2.0, 3.0, Type-C
- [x] Trackpad **(All gestures supported)**
- [x] Sleep & wake  **(Not work while connected HUB)**
- [x] Battery Stat
- [x] Tempareture Monitor
- [x] HDMI/VGA port with External Display & Audio output
- [x] Apple Store, iCloud, FaceTime, iMessege
- [x] Universal Control (Not tested)
- [x] AirPlay
- [x] Fn feature **(Brightness and volume button works)**
- [x] Continuity Camera **(works only USB mode. will not work with wifi till now)**

# Not WORKING:
- [ ] Biult-in wifi has some issues
  + WPA3 not works.
  + WPA2/WPA3 mixed mode will work.
  + Noise level not showing.
  + Upload speed sometimes drops.
- [ ] iPhone Mirroring
- [ ] Airdrop
- **Wait for the fix**
- [ ] No DRM support. Will never work.
  + **NETFLIX will not work on safari browser**
  + **AppleTV app will not play videos**

# Installation:

### BIOS Settings

Change the following settings in bios:
- Intel software guard extentions (SGX) - Disabled
- TPM Device -  Hidden
- Secure Boot - Disabled

### Installing macOS:
- Just put this EFI to your USB EFI partition.
- If you don't know how to make bootable your USB then go [here.](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
- Install macOS 26 Tahoe to your SSD or HDD.
- If you are new then go [here.](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html#prerequisites)
- After install mount the USB EFI and copy this to your HDD or SSD EFI.

### iMessege & Facetime Fix:
- Change the serial numbers and other things. You can find the tutorial from [here.](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/broadwell.html#platforminfo)

## Important Note about Updating macOS:
Do not update macOS. You can update only if you update the OC version and kext on your own. Otherwise wait for my update.


## Credits
@RehabMan for his guide for beginner
@alexandred and his team for VoodooI2C 
@acidanthera for his OpenCore Bootloader and kexts
and many more people that I can't list here.
