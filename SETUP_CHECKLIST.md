# Setup Checklist - HP 15s-du0094tu + macOS Ventura

## Pre-Installation

### System Preparation
- [ ] Backup all data
- [ ] Update HP BIOS to latest
- [ ] Disable Secure Boot
- [ ] Disable Fast Boot
- [ ] Enable UEFI Boot
- [ ] Enable VT-x

### SMBIOS Generation
- [ ] Run GenSMBIOS
- [ ] Generate for MacBookPro15,2
- [ ] Copy SerialNumber
- [ ] Copy MLB
- [ ] Copy SmUUID
- [ ] Copy ROM

### Download Files
- [ ] OpenCore BOOTx64.efi
- [ ] HfsPlus.efi
- [ ] All required Kexts
- [ ] SSDT files

### File Organization
- [ ] Copy BOOTx64.efi to EFI/BOOT/
- [ ] Copy drivers to EFI/OC/Drivers/
- [ ] Copy kexts to EFI/OC/Kexts/
- [ ] Copy SSDTs to EFI/OC/ACPI/

## Installation Phase

### USB Preparation
- [ ] Create macOS installer
- [ ] Mount EFI partition
- [ ] Copy EFI folder to USB
- [ ] Verify files are present

### Boot & Install
- [ ] Set USB as first boot device
- [ ] Boot from USB
- [ ] Select "Install macOS Ventura"
- [ ] Complete installation

## Post-Installation

### EFI Setup
- [ ] Mount internal drive EFI
- [ ] Copy EFI from USB to internal
- [ ] Boot without USB (verify it works)

### System Configuration
- [ ] Remove debug boot args
- [ ] Connect to WiFi
- [ ] Create user account
- [ ] Update system

## Hardware Verification

### Trackpad
- [ ] Touch response
- [ ] Left click
- [ ] Right click
- [ ] Gestures

### Audio
- [ ] Speaker output
- [ ] Microphone input
- [ ] Volume controls

### Display
- [ ] Brightness control
- [ ] External display (if applicable)

### Power
- [ ] Battery detection
- [ ] AC adapter recognition
- [ ] Sleep/Wake

### Connectivity
- [ ] WiFi connects
- [ ] Bluetooth works
- [ ] USB ports functional

## Final Status

- [ ] System is stable
- [ ] All hardware functional
- [ ] Ready for daily use

---

**Installation Date:** ___________
**Completion Date:** ___________
**Notes:** ___________________