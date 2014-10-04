N9005 Omega Kernel KK 4.4.2

Based on Samsung kernel sources Kit Kat Update 9

****************************************************

1. How to Build

- get Toolchain
			From Android Source Download site( http://source.android.com/source/downloading.html )
			Toolchain is included in Android source code.

- edit Makefile
			edit "CROSS_COMPILE" to right toolchain path(You downloaded).
			ex) CROSS_COMPILE= $(android platform directory you download)/android/prebuilt/linux-x86/toolchain/arm-eabi-4.7/bin/arm-eabi-
			ex) CROSS_COMPILE=/usr/local/toolchain/arm-eabi-4.7/bin/arm-eabi-
- Build
		$ sudo su
		$ export ARCH=arm
		$ make VARIANT_DEFCONFIG=msm8974_sec_hlte_eur_defconfig msm8974_sec_defconfig SELINUX_DEFCONFIG=selinux_defconfig
		$ make
		
2. Output files
		- Kernel : output/arch/arm/boot/zImage

3. How to Clean	
		$ make clean

****************************************************

