# STM32F103C8 (Blue Pill)  Toolchain
Main repo at https://github.com/libopencm3/libopencm3-template

## Prerequisites
* st-link tools
```sh
sudo apt install st-link gcc-arm-none-eabi
```

## Instructions
 1. git clone --recurse-submodules https://github.com/libopencm3/libopencm3-template.git your-project
 2. cd your-project
 3. make -C libopencm3 # (Only needed once)
 4. make -C my-project

If you have an older git, or got ahead of yourself and skipped the ```--recurse-submodules```
you can fix things by running ```git submodule update --init``` (This is only needed once)

## Directories
* my-project contains your application
* my-common-code contains something shared.

## Flashing
```sh
st-flash --reset write "project name".bin 0x8000000
```
Since FLASH at 0x8000000
