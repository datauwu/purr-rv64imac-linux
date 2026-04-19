# Purr RV64IMAC Emulator

A self-contained RV64IMAC emulator written in **Purr**, a custom bytecode-compiled programming language.

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

The guest root filesystem also includes extra userspace programs for fun, including:

- `/usr/bin/shorkfetch` or `shorkfetch` - a fetch-style system information utility you can run inside the emulated Linux environment
- `/usr/bin/shorkmatrix` or `shorkmatrix` - a Matrix-style terminal animation utility you can run inside the emulated Linux environment

These are included as part of the guest system and remain licensed under their own respective terms.

## Requirements

The following files must be in the same folder as `emulator.exe`:

- `fw_jump.bin`
- `Image`
- `virt.dtb`
- `rootfs.cpio`

`emulator.exe` currently supports 64-bit Windows only.
It requires the Universal CRT (UCRT) and an ANSI-compatible terminal.

# Important

- Do not press Ctrl+C while the emulator is booting unless you intentionally want to terminate it.
- Do not press Ctrl+Shift+C in your terminal while the emulator is running or booting.
- Interrupting the emulator during boot will usually force you to restart it and wait through the boot process again.
