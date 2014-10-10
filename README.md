HydraFW official firmware for HydraBus/HydraNFC
========

HydraFW is a native C (and asm) open source firmware for HydraBus board with support of HydraNFC Shield.

You can Buy HydraBus/HydraNFC Online in Seeed Studio Online Shop:
http://www.seeedstudio.com/depot/HydraBus-m-132.html

![HydraBus+HydraNFC board](HydraBus_HydraNFC_board.jpg)

For hydrafw usage with VT100 Terminal see wiki
https://github.com/bvernoux/hydrafw/wiki/HydraFW-commands

##How to build, flash and use hydrafw on Windows:

###Required dependencies:

    Custom chibios (based on ChibiOS 3.0) included as Submodule.
    Custom microrl included as Submodule.
    
###Prerequisites for Windows:
    git clone https://github.com/bvernoux/hydrafw.git hydrafw
    cd hydrafw/
    git submodule init
    git submodule update


###To build hydrafw firmware (with mingw or cygwin):
The firmware is set up for compilation with the GCC toolchain GNU_ARM_4_7_2013q3 available here:
https://launchpad.net/gcc-arm-embedded/+milestone/4.7-2013-q3-update

    cd in root directory(which contains directories common, fatfs, hydrabus, hydranfc ...)
    make clean
    make

###Flash and use hydrafw on Windows:
See the wiki https://github.com/bvernoux/hydrafw/wiki/Getting-Started-with-HydraBus

##How to build, flash and use hydrafw on Linux (Debian/Ubuntu):

###Prerequisites for Linux:

    cd ~
    sudo apt-get install git dfu-util python putty
    wget http://www.bialix.com/intelhex/intelhex-1.4.zip
    unzip intelhex-1.4.zip
    cd intelhex-1.4
    sudo python setup.py install --user
    wget https://launchpad.net/gcc-arm-embedded/4.7/4.7-2013-q3-update/+download/gcc-arm-none-eabi-4_7-2013q3-20130916-linux.tar.bz2
    tar xjf gcc-arm-none-eabi-4_7-2013q3-20130916-linux.tar.bz2
    echo 'PATH=$PATH:~/gcc-arm-none-eabi-4_7-2013q3/bin' >> ~/.bashrc
    git clone https://github.com/bvernoux/hydrafw.git hydrafw
    cd ~/hydrafw
    git submodule init
    git submodule update

###Build hydrafw on Linux:

    cd ~/hydrafw
    make clean
    make

###Flash and use hydrafw on Linux:
See the wiki https://github.com/bvernoux/hydrafw/wiki/Getting-Started-with-HydraBus

