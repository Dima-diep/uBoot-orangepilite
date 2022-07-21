# BUILDING

For building, run these commands:
```
// Setup arch
 ~/uBoot-orangepi $ export ARCH=arm
// Make config
 ~/uBoot-orangepi $ make orangepi_lite_new_defconfig
// Install cross-toolchain and host gcc
 ~/uBoot-orangepi $ sudo apt install gcc-10-arm-linux-gnueabi gcc-10 binutils binutils-arm-linux-gnueabi
// compile uBoot image
 ~/uBoot-orangepi $ make -j[your cpus] CROSS_COMPILE=/usr/bin/arm-linux-gnueabi-
// Write image to sdcard
 ~/uBoot-orangepi $ dd if=u-boot-sunxi-with-spl.bin of=/dev/[your sdcard] seek=8 bs=1024
```
