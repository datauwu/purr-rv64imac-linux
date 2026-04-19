# Purr RV64IMAC Emulator

A self-contained RV64IMAC emulator written in **Purr** (custom bytecode-compiled programming language).

This project boots:
- OpenSBI firmware
- a Linux kernel
- a guest root filesystem / initrd

## Included Files

- `emulator.exe` - the emulator executable
- `fw_jump.bin` - OpenSBI firmware
- `Image` - Linux kernel image
- `virt.dtb` - device tree blob
- `rootfs.cpio` - guest root filesystem / initrd

Also included:
- `LICENSE` - license for the emulator itself
- `THIRD_PARTY_NOTICES.txt` - third-party software notices
- `SOURCE_CODE.txt` - source code availability notice for third-party GPL components
- `buildroot.config` - Buildroot configuration used for the guest root filesystem
- `licenses/` - copies of relevant third-party license texts

## Requirements

The following files must be in the same folder as `emulator.exe`:

- `fw_jump.bin`
- `Image`
- `virt.dtb`
- `rootfs.cpio`

`emulator.exe` currently supports 64-bit Windows only.