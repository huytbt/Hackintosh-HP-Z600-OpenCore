# Hackintosh HP Workstation Z600 OpenCore Bootloader

## System Specification
- Processor: 2 x 3.1 GHz 6-Core Intel Xeon X5675
- Memory: 32.03 GB 1600 MHz DDR3
- Graphics: NVIDIA Quadro K4000 3071 MB --> Change to **Radeon RX 570 4 GB** for update macOS

## Attention
- To get USB functional: Delete '**AppleHPET.kext**' from **/System/Library/Extensions** once you have successfully booted in to macOS. Once deleted, reboot your Z600.
- Always check and delete '**AppleHPET.kext**' after update macOS. Maybe need Repair permissions and Rebuild cache SLE (Using Kext Wizard app).

## Issues
- Graphics Radeon RX 570 can not show dual monitors, one monitor is black. Fix by add CsmVideoDxe-64.efi to drivers. Don't forget update OC/config.plist

## OS Version Tested
- macOS High Sierra 10.13.6 (17G13035, 17G14019)
