# Hackintosh HP Workstation Z600 OpenCore Bootloader

## System Specification
- Processor: 2 x 3.1 GHz 6-Core Intel Xeon X5675
- Memory: 32.03 GB 1600 MHz DDR3
- Graphics: *NVIDIA Quadro K4000 3 GB* --> Changed **Radeon RX 570 4 GB** to update macOS from High Sierra to latest version
- Wireless: BCM94360CD(Wifi) + 20702B0(Bluetooth 4.0) Airport Adapter

## Information
- Change from AppleAHCIPort.kext to CtlnaAHCIPort.kext. This is for update to Big Sur. Issue related SATA. The cause Apple removed the AppleIntelPchSeriesAHCI class from AppleAHCIPort.kext. So boot panic with error "Waiting for Root Device"
- Z600 / Z800 with AppleALC ID28 also always needed the CodecCommander.kext

## Attention
- Please generate SMBios and add to conflig.plist (Using https://github.com/corpnewt/GenSMBIOS)

## Feature Work Well
- Sleep and Wake up
- Airdrop & Handoff
- iMessage & Facetime
- Find My Mac
- Native HD Audio

## OS Version Tested
- macOS High Sierra 10.13.6 (17G13035, 17G14019)
- macOS Catalina 10.15.6 (19G73, 19G2021)
- macOS Big Sur 11.0 Beta (20A5343i, 20A5354i)

## Issues
- Big Sur: Apple stop support BCM5764M Ethernet card, need use NullEthernet.kext to fix iServices

## Credits
- [Apple](https://www.apple.com) for macOS  
- [Acidanthera](https://github.com/acidanthera) for Hackintosh
