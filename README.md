# Hackintosh HP Workstation Z600 OpenCore Bootloader

## System Specification
- Processor: 2 x 3.1 GHz 6-Core Intel Xeon X5675
- Memory: 32.03 GB 1600 MHz DDR3
- Graphics: NVIDIA Quadro K4000 3 GB --> Change to **Radeon RX 570 4 GB** for update macOS

## Information
- Change from AppleAHCIPort.kext to CtlnaAHCIPort.kext. This is for update to Big Sur. Issue related SATA. The cause Apple removed the AppleIntelPchSeriesAHCI class from AppleAHCIPort.kext. So boot panic with error "Waiting for Root Device"

## Attention
- Please generate SMBios and add to conflig.plist (Using https://github.com/corpnewt/GenSMBIOS)

## Feature Work Well
- Sleep and Wake up
- Airdrop & Handoff
- iMessage & Facetime
- Find My Mac

## Issues
- Audio ALC262 (0x10ec0262) does not support codec -> using USB Sound Card

## OS Version Tested
- macOS High Sierra 10.13.6 (17G13035, 17G14019)
- macOS Catalina 10.15.6 (19G73, 19G2021)
