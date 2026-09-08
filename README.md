# Evil Tux
I woke up today and decided to choose violence. So I forked linux source tree and modified bochs setmode function in bochs driver. (Basically increased bpp to 256 just for fun).
And now tux is evil.

# Instructions (to check out the EVIL TUX)
basically the same as the standart linux kernel:
1. `make allnoconfig`
2. `make menuconfig` -> select here 64bit kernel, then in general setup INITRAMFS support, ELF formats, In device drivers pci support, in graphics support - DRM, and drm support for bochs, don't forget to enable boot logo and legacy fbdevf support.
3. `make -j$(nproc)`
4. `qemu-system-x86_64 -kernel arch/x86/boot/bzImage`
5. Enjoy.

# Motivation
I've always wanted to poke around the linux kernel, see it's structure and everything. So yeah, i've made ther simplest change possible but in the process i've learned the compile process and I think i'll use this knowledge in the os i'm currently building.
