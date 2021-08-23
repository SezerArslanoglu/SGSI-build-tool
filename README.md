# SGSI-build-tool
**Copyright (C) 2021 Xiaoxindada (2245062854@qq.com)
Commercial use is not allowed without my permission**
 
## This tool partly depends on:
* Erfan GSIs: https://github.com/erfanoabdi/ErfanGSIs
* MToolkit: https://github.com/Nightmare-MY
* AndroidDump: https://github.com/AndroidDump/dumper
* Thanks for the above list

## Thanks to Jiuyumengzhou https://github.com/pomelohan for the help
## Thanks to Col_or https://github.com/color597 for the help

# This tool is PC version

# Make sure to use the tool for the first time
```
tar uses:
Download this tool
Enter the directory where the tool is located and execute the following command:
su
tar -xf SGSI-build-tool-12.tar
cd SGSI-build-tool-12/12

From v12-1.2 and beyond:
su
tar -xf SGSI-build-tool-12.tar
cd SGSI-build-tool-12
```

```
GitHub:
git clone --recurse-submodules https://github.com/xiaoxindada/SGSI-build-tool.git -b 12
cd SGSI-build-tool-12
su
```

# Use Actions to build SGSI:
https://github.com/xiaoxindada/SGSI-build-action


# The installation tool depends on the environment (it is recommended to hang t)
```
Test environment: Ubuntu 20.04
(Debian series Linux support, Arch series does not support the need to change the script installation dependency)
./setup.sh
```

# Manufacturing SGSI:
```
Put the flashing package into the tmp folder
Make A-only: ./make.sh A
Make AB: ./make.sh AB
It can also be used alone./SGSI.sh A or ./SGSI.sh AB
If the original package is super.img, put super.img in the tool root directory
Then use ./unpacksuper.sh to unpack and then throw the unpacked img into the tool directory and execute it directly./SGSI.sh
The SGSI made by this tool also supports the flashing of dynamic partition models, but it needs to be packaged into super.img
Use ./makesuper.sh to package
The content of Patch1 Patch2 needs to be packaged to vendor.img by yourself, package the system vendor to generate super.img and then flash in, then flash in patch3 to format the data.
This tool only needs to make the patch part of system.img manually
This tool is a semi-automatic tool, because some processing automation is not ideal and changeable, so manual is better. If you don’t know how to deal with these things, you can just not process them and make them directly.
The finished product is output in the SGSI folder, and then you can manually make Patch 1 2 3

v12-1.4 began to use scripts to pass parameters for construction
su
Manufacturing A-only: ./make.sh -a Pixel ./tmp/redfin-ota-spp2.210219.008-3d61e529.zip --fix-bug
Manufacturing AB: ./make.sh --ab Pixel ./tmp/redfin-ota-spp2.210219.008-3d61e529.zip --fix-bug
Use SGSI.sh alone: ​​./SGSI.sh --ab Pixel --fix-bug
```

# Synchronous update tool:
```
./update.sh
```

# This tool packs and unpacks the script
```
img packaging and unpacking: makeimg2.sh unpackimg.sh (can be used alone, supporting any partition packaging and unpacking)
Pack and unpack super.img: makesuper.sh unpacksuper.sh
Unpack and unpack boot.img: makeboot.sh unpackboot.sh
dat/br generation: img2sdat.sh simg2sdat.sh
Unzip the apex of img: apex.sh (apex flattened)
Local deodex: bin/oat2dex/deodex.sh
ozip decryption: oppo_ozip
Pack and unpack dtboimg: makedtbo.sh unpackdtbo.sh
apk signature: bin/tools/signapk/signapk.sh
LG kdz unpack: unpack_kdz.sh
oppo/oneplus ops unpacking: unpack_ops.sh
```

# Patch1 How to make
```
1. Add Vendor Blobs and overlays of oem vendors
2. Clear to make specific modifications according to the log situation
3. Patch samples to upload folders (please imitate yourself)
```

**Cleanup tool, just execute rm.sh to change the directory**

**If you want to donate me, please feel free to QQ group: 967161723**
