# Dell_Optiplex_5040_SFF

This is a EFI for MacOS based on the OpenCore project.
This EFI is created to run on the DELL Optiplex 5040SFF, other Dell machines and variants may be able to run it.

The EFI/Config is set to NOT utilize the iGPU and any other GPUs used will need to have the config adjusted.

In order to get full hardware acceleration the RX 550 Lexa Core needs to be spoffed as a Baffin Core based AMD Card.
This EFI is using the ACPI-Spoofing method, thought Device Properties spoofing might work for other Lexa Core cards.

PC Spesc:

CPU:    I5-6500
iGPU:   Intel HD 530 (DISABLED)
dGPU:   AMD RX 550 - 4Gb (LEXA CORE)
RAM:    16Gb DDR3L - 1600 Mhz

**!!!!!!!!  IMPORTANT   !!!!!!!!!!**

For iGPU utilization:
For MacOS to be installed two major keypoints must be addressed:
1. MSR needs to be deactivated - Not available in BIOS nor is it addressible from the config.plist
2. (DVMT) Graphics Memory allocation needs to be more than 32Mb, otherwise installer/OS will boot to a black screen
-> the above changes can be done only by changing the values within the BIOS (BIOS Modding) which may lead to a BRICKED MACHINE

**!!!!!!!!  IMPORTANT   !!!!!!!!!!**
