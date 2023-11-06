# OpenCore 0.9.5 Configuration for Dell XPS 15 9560

### Ventura/BigSur work for DELL XPS 9560 1080 FullHD
other options see here: https://www.tonymacx86.com/threads/guide-dell-xps-9560-ventura-opencore.324866/
Thanks a lot to InsaneCultist

## UEFI BIOS Variables Setup

| Variable                                 | Offset | Default         | Desired         | Comment |
|------------------------------------------|--------|-----------------|-----------------|---------|
| Above 4GB MMIO BIOS assignment           | 0x79A  | 0x00 (Disabled) | 0x01 (Enabled)  |         |
| ACPI Removal Object Suppport             | 0x491  | 0x00 (Disabled) | 0x00            |         |
| CFG Lock                                 | 0x4ED  | 0x01 (Enabled)  | 0x00 (Disabled) |         |
| CSM Support                              | 0xFC8  | 0x01 (Enabled)  | 0x00 (Disabled) |         |
| DVMT Pre-Allocated                       | 0x795  | 0x02 (64M)      | 0x02 (64M)      |         |
| DVMT Total Gfx Memory                    | 0x796  | 0x02 (256M)     | 0x03 (MAX)      |         |
| GPIO filter                              | 0x47B  | 0x00            | 0x01            |         |
| GPIO3 Force Pwr                          | 0x45F  | N/A             | 0x01            |         |
| Native OS Hot Plug                       | 0x479  | N/A             | 0x01            |         |
| Skip PCI OptionRom                       | 0x48F  | 0x00            | 0x00            |         |
| SW SMI on TBT hot-plug                   | 0x47A  | 0x01 (Enabled)  | 0x01            |         |
| Thunderbolt Boot Support                 | 0x45B  | 0x00 (Disabled) | 0x01            |         |
| Thunderbolt Usb Support                  | 0x45A  | 0x00 (Disabled) | 0x01            |         |
| Thunderbolt(TM) PCIe Cache-line Size     | 0x45E  | 0x20 (32)       | 0x80 (128)      |         |
| Wait time in ms after applying Force Pwr | 0x460  | 0xC8 (200)      | 0xC8 (200)      |         |
| Wake From Thunderbolt(TM) Devices        | 0x452  | 0x01 (Enabled)  | 0x01            |         |

## References

- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [Dortania's Getting Started With ACPI](https://dortania.github.io/Getting-Started-With-ACPI/)
- [DarkWake on macOS Catalina](https://www.insanelymac.com/forum/topic/342002-darkwake-on-macos-catalina-boot-args-darkwake8-darkwake10-are-obsolete/)
- [XPS15 9560 EFI by jardenliu and SilentSliver](https://github.com/jardenliu/XPS15-9560-Catalina/tree/OpenCore/)
- [Post on fixing TBT on High Sierra](https://www.tonymacx86.com/threads/how-to-build-your-own-imac-pro-successful-build-extended-guide.229353/)
- [SSDT for TBT Hotplug](https://www.tonymacx86.com/threads/in-progress-ssdt-for-thunderbolt-3-hotplug.248784/page-55)
- [osy86's Hac-Mini](https://osy.gitbook.io/hac-mini-guide/)
