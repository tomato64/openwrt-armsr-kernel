# openwrt-armsr-kernel

OpenWrt kernel patches for the Arm SystemReady (EFI) compliant target, subtarget
`armv8` (64-bit ARMv8 machines) — i.e. `armsr/armv8`. Intended for ARM64 virtual
machines (QEMU / Proxmox on aarch64 hosts).

## Usage

Run `./generate-patch.sh` to generate a monolithic kernel patch file from OpenWrt
patches.

This script:
1. Clones OpenWrt at the specified version (v25.12.4)
2. Downloads the vanilla Linux kernel (6.12.87)
3. Copies OpenWrt generic kernel files
4. Applies OpenWrt generic patches (backport, pending, hack)
5. Applies armsr-specific patches
6. Generates a single monolithic patch file

Output: `00001-openwrt-armsr-kernel-6.12.87.patch`
