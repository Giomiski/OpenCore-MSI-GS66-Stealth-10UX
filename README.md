This is an [OpenCore](https://github.com/acidanthera/OpenCorePkg) setup for the MSI GS66 Stealth 10UX series laptops

# Hardware specs

| CPU | Intel 10th Gen (Comet Lake) |
| :-: | :-: |
| iGPU | Intel UHD 630 |
| dGPU | NVIDIA RTX 30 Series laptop |
| Sound card | Realtek ALC298 |
| Network card | Intel Killer E3100X (Intel I225-LM) |
| Wireless card | Intel AX210 |

> List of all aviable models [GS66-Stealth-10UX](https://www.msi.com/Laptop/GS66-Stealth-10UX/Specification)

# Configuration

> [!IMPORTANT]
> Complete the config.plist file by generating the below values with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) using ```MacBookPro16,4``` model otherwise the system will not boot
>
> > You can edit the config.plist file by using [ProperTree](https://github.com/corpnewt/ProperTree)
> 
> ### config.plist
>   - PlatformInfo
>       - Generic
>         - MLB
>         - ROM
>         - SystemSerialNumber
>         - SystemUUID
>
>
> >GenSMBIOS values reminder
> >  - Serial = SystemSerialNumber
> >  - Board Serial = MLB
> >  - SmUUID = SystemUUID
> >  - Apple ROM = ROM
>
> Full explain can be found in the [PlatformInfo](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/coffee-lake-plus.html#platforminfo) section of the [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide)

## Display

If you have the 300Hz display model add ```-igfxmpc``` to the boot-args to enable full refresh rate

## Wireless card

### macOS Sequoia

After finishing installing macOS, transfer with a USB drive or download if you have an ethernet cable plugged in, the latest version of [OCLP](https://github.com/dortania/Opencore-Legacy-Patcher/releases), install it, than run ```Post-Install Root Patch```

After finishing installing the root patches, reboot when asked
