# Device Tree for building TWRP for POCO C31 (angelicain)

1.Getting Started
---------------
**Initialize local repo**
```
mkdir ~/twrp-12.1
cd ~/twrp-12.1
repo init -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
```
**Sync up with this command:**
```bash
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
```

2.Preparing device for building
---------------
**Clone this repo**
```bash
git clone https://github.com/suchit-7x/twrp_xiaomi_angelicain.git device/xiaomi/angelicain
```

3.Build
---------------
**Set up environment**
```bash
. build/envsetup.sh
```
**Build the recovery**
```bash
lunch twrp_angelicain-eng
mka recoveryimage
```

* If is successful, congratulation!
* Go to `out/target/product/angelicain/` and you will find your recovery.img
