# A snap package of the linux dtc command

[![Snap Status](https://build.snapcraft.io/badge/ogra1/devicetree-compiler.svg)](https://build.snapcraft.io/user/ogra1/devicetree-compiler)

This is the linux devicetree compiler "dtc" as a snap.
Due to the limits of snap packages you need to first copy the devicetree files to your home dir to allow dtc access to them.

If you use this snap on Ubuntu Core, note that the home interface will not auto-connect, connect it manually with:

`snap connect devicetree-compiler:home`

You can convert binary device tree files to plaintext to edit them and convert them back to binary.

## Convert binary devicetree to dts text format

devicetree-compiler -I dtb ~/sun8i-h3-nanopi-neo-air.dtb -O dts -o ~/sun8i-h3-nanopi-neo.dts

## Convert text format to binary dtb

devicetree-compiler -I dts ~/sun8i-h3-nanopi-neo.dts -O dtb -o ~/sun8i-h3-nanopi-neo.dtb
