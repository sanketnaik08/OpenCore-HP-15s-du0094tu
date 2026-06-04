# Installation Guide - HP 15s-du0094tu + macOS Ventura

## Prerequisites

- USB drive (8GB+) formatted as FAT32
- Another Mac or Linux machine with OpenCore tools
- Internet connection
- GenSMBIOS for generating SMBIOS data

## Step 1: Generate SMBIOS Data (CRITICAL)

1. Download [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
2. Run: `python3 GenSMBIOS.py`
3. Select option 3 (Generate SMBIOS)
4. Choose `MacBookPro15,2`
5. Copy the generated values:
   - SystemSerialNumber
   - MLB
   - SystemUUID
   - ROM

## Step 2: Update config.plist

1. Open `EFI/OC/config.plist` with ProperTree
2. Navigate to: `PlatformInfo > Generic`
3. Update:
   - SystemSerialNumber
   - MLB
   - SystemUUID
   - ROM

## Step 3: Download Required Files

### OpenCore & Drivers
- BOOTx64.efi → `EFI/BOOT/`
- HfsPlus.efi → `EFI/OC/Drivers/`
- OpenLinuxBoot.efi → `EFI/OC/Drivers/`

### Kexts (all in `EFI/OC/Kexts/`)
- Lilu.kext
- VirtualSMC.kext + plugins
- WhateverGreen.kext
- AppleALC.kext
- IntelMausi.kext
- VoodooI2C.kext + VoodooI2CHIDDevice.kext
- BrcmFirmwareData.kext
- BrcmPatchRAM3.kext

### ACPI Tables (in `EFI/OC/ACPI/`)
- SSDT-EC-USBX-LAPTOP.aml
- SSDT-PNLF.aml
- SSDT-PLUG-ALT.aml

## Step 4: Create Installation USB

1. Format USB as FAT32
2. Create macOS Ventura installer
3. Mount EFI partition
4. Copy entire `EFI` folder to USB

## Step 5: BIOS Settings

- Disable Secure Boot
- Disable Fast Boot
- Enable UEFI Boot
- Enable VT-x
- Set USB as first boot device

## Step 6: Boot and Install

1. Insert USB
2. Boot from USB
3. Select "Install macOS Ventura"
4. Follow installer
5. Complete installation

## Step 7: Post-Installation

1. Mount EFI partition of internal drive
2. Copy EFI folder from USB to internal drive
3. Remove debug boot args from config.plist
4. Verify hardware works

## Troubleshooting

- **Kernel Panic**: Enable verbose mode (-v), check config.plist syntax
- **Trackpad not working**: Verify VoodooI2C kexts are present
- **Audio not working**: Check AppleALC.kext and correct layout ID
- **WiFi not detected**: Verify Broadcom kexts are loaded

See README.md for more information.