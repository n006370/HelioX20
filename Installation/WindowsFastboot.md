## Windows Host

This section show how to install a new operating system to your MediaTek X20 using the fastboot method on a Windows host computer.

***

#### **Necessary Condition**

You need prepare 6 components:
- xflash.exe
- Normal load(Include image files and scatter file etc.)
- Special images and scatter file
- lib.cfg.xml
- fastboot.exe
- fastboot command script file

#### **Flash Tool access path**

alps\vendor\mediatek\proprietary\system\core\xflash

#### **How to build special images**

Execute following commands, build system will automatically create FES folder and come out the special lk.bin, where FES store the needed files for xflash download to target befor entering fastboot mode. 

`$ source build/envsetup.sh`

`$ lunch full_amt6797_64_open-eng`

`$ make -j16 PLATFORM_FASTBOOT_EMPTY_STORAGE=yes -k 2>&1 | tee build.log`

Then, you can find a folder named FES.

PATH: \out\target\product\amt6797_64_open\FES

#### **Prepare your Windows host machine**

- xflash.exe
   - \xflash\bin\win\xflash.exe
- Normal load(Include image files and scatter file etc.)
   - You can put it in anywhere, eg, \xflash\bin\win\img
- Special images and scatter file
   - You can put it in anywhere, eg, \xflash\bin\win\FES. How to build it?
   - Please see “How to build special images”.
- lib.cfg.xml
   - \xflash\bin\win\config
- fastboot.exe
   - \xflash\bin\win, you shoud put it in normal load folder.
- fastboot command script file
   - Writen by yourself, you should put it in normal load folder.

#### **Windows Download**

Step 1. Make a device to enter fastboot mode
- Prepare special images and corresponding scatter file.
- Run program in command line mode like this:

    `xflash.exe enter-fastboot “G:\xflash\bin\win\FES\MT6797_Android_scatter.txt”`
- Then plug in usb to device.
- Xflash will scan and open device COM port and connect it, download some necessary images to devices, then make device to enter fastboot mode.

Step 2. Run fastboot command script file
- You need write a download script.

        Such as xflash.bat
        
        fastboot devices
        fastboot flash gpt PGPT
        fastboot flash preloader preloader_amt6797_64_open.bin
        fastboot flash recovery recovery.img
        fastboot flash scp1 tinysys-scp.bin
        fastboot flash scp2 tinysys-scp.bin
        fastboot flash lk lk.bin
        fastboot flash lk2 lk.bin
        fastboot flash boot boot.img
        fastboot flash logo logo.bin
        fastboot flash tee1 trustzone.bin
        fastboot flash tee2 trustzone.bin
        fastboot flash system system.img
        fastboot flash cache cache.img
        fastboot flash userdata userdata.img
        fastboot reboot
        
- Run the download script, download success.
