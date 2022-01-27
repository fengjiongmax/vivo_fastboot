# vivo_fastboot
Modified fastboot sources to unlock vivo phones
How to use :-

Lock vivo bootloader   :  fastboot bbk lock_vivo 

Unlock vivo bootloader :  fastboot bbk unlock_vivo

This binary can be compiled using any toolchain (on linux only) or using the official method by downloading whole AOSP source.
If you want to compile for windows, you probably have to use the whole AOSP source.

How to compile :-

Clone the following aosp sources using git from android.googlesource.com (android-4.4_r**,branch name: kitkat-release)

platform/system/core, platform/system/extras, /platform/external/libselinux, /platform/external/zlib, /platform/external/openssl. 

Now navigate to platform/system/core/ directory 

type git clone https://github.com/Naveen3Singh/vivo_fastboot.git fastboot

Now the vivo_fastboot source will be downloaded in fastboot directory with a custom makefile for our toolchain.

Now type make within fastboot directory to compile the fastboot binary.

if you get compile error, it's most likely due to toolchain, edit makefile to point to your toolchain.
If you want to add support for more commands, just search "vivo_bsp" in fastboot.c, & replace it with your desired commmand.
