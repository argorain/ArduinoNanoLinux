# Arduino Nano v3 Linux Setup
Target of this project is init of Linux Arduino project without Arduino IDE and Atmel Studio. Just avr-gcc, make and avrdude. Good luck.

## Preparations
Install avr toolchain and avrdude

    sudo aptitude install avr-gcc gdb-avr avr-libc avrdude

## Usage
Connect your Arduino to PC and try to build project
    
    make
    make flash

Now you should see LED blinking.

## Reuse
If you want to reuse this project (respectively its Makefile), just rewrite following variables to your own. More files are simply divided by spaces. BINARY says result hex file name, SOURCE are your source files, OBJS are resulting object files (usually same names as sources, just ending with .o) and HEADERS are your header files.
    
    # PROJECT DEFINES
    BINARY = MyAwesomeProject
    SOURCE = main.c blinking.c timer.c`
    OBJS = main.o blinking.o timer.o
    HEADERS = blinking.h timer.h