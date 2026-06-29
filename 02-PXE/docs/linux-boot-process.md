## Linux Boot Process

## Overview

Before an operating system can run, a computer follows a defined boot sequence that initializes hardware, loads the operating system, and starts essential services.

## Boot Sequence

1. Power On
2. BIOS/UEFI Initialization
3. Power-On Self-Test (POST)
4. Boot Device Selection
5. GRUB Boot Loader
6. Linux Kernel Loading
7. systemd Initialization
8. User Login

## Components

BIOS/UEFI

Initializes hardware and determines the boot device according to the configured boot order.

POST

Verifies CPU, RAM, storage devices, and other hardware before continuing.

GRUB

Loads the selected Linux kernel into memory.

Linux Kernel

Initializes hardware drivers, memory management, networking, and core operating system functions.

systemd

Starts user-space services such as networking, SSH, logging, and other configured daemons.

Relation to PXE

PXE Boot modifies the boot device selection stage by instructing the firmware to boot from the network instead of a local storage device.

Understanding the normal Linux boot process provides the foundation for understanding PXE-based network booting.
