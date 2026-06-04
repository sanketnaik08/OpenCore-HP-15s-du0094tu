# OpenCore Configuration for HP 15s-du0094tu + macOS Ventura

This is a complete OpenCore EFI configuration for running macOS Ventura on the **HP 15s-du0094tu** laptop with **Intel Core i3-8145U (Whiskey Lake)** processor.

## System Specifications

- **Laptop Model:** HP 15s-du0094tu
- **Processor:** Intel Core i3-8145U (Whiskey Lake, 8th Gen)
- **GPU:** Intel UHD Graphics 620
- **RAM:** 8 GB DDR4
- **Storage:** 1 TB HDD
- **Target OS:** macOS Ventura (13.x)
- **SMBIOS:** MacBookPro15,2

## Quick Start

1. **Generate SMBIOS data** using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
2. **Update config.plist** with your SMBIOS values
3. **Download required files** (see INSTALLATION_GUIDE.md)
4. **Create USB installer** with this EFI
5. **Boot and install** macOS Ventura

## Documentation

- **README.md** - Overview and system requirements
- **INSTALLATION_GUIDE.md** - Step-by-step installation instructions
- **SETUP_CHECKLIST.md** - Complete checklist for setup verification

## Key Features

✅ Full working macOS Ventura support
✅ GPU acceleration (UHD Graphics 620)
✅ Audio support
✅ Trackpad with gestures
✅ WiFi & Bluetooth
✅ Battery management
✅ Sleep/Wake functionality
✅ Brightness control
✅ USB power management

## Important Notes

⚠️ **CRITICAL:** You MUST generate your own SMBIOS data. Never use sample data for production use.

## File Structure

```
OpenCore-HP-15s-du0094tu/
├── README.md
├── INSTALLATION_GUIDE.md
├── SETUP_CHECKLIST.md
└── EFI/
    ├── BOOT/
    │   └── (BOOTx64.efi - Download from OpenCore)
    └── OC/
        ├── config.plist
        ├── ACPI/
        │   └── (SSDT files)
        ├── Drivers/
        │   └── (UEFI drivers)
        ├── Kexts/
        │   └── (Kernel extensions)
        └── Tools/
```

## Resources

- [Dortania OpenCore Laptop Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [OpenCore Documentation](https://github.com/acidanthera/OpenCorePkg)
- [Hackintosh Reddit Community](https://www.reddit.com/r/hackintosh/)

## License

This EFI configuration is provided as-is for educational purposes.

---

**Status:** Ready for customization
**Last Updated:** June 2026
**OpenCore Version:** Latest (see releases)