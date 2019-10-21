# android_device_lenovo_kunlun2
For building TWRP for Lenovo K10 Note

TWRP device tree for Lenovo K10 Note

## Features

BETA BUILD TREE

## Compile

First checkout minimal twrp with omnirom tree:

```
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
repo sync
```

Then add these projects to .repo/manifest.xml:

```xml
<project path="device/lenovo/kunlun2" name="RaySlash/android_device_lenovo_kunlun2" remote="github" revision="pie" />
```

Finally execute these:

```
. build/envsetup.sh
lunch omni_kunlun2-eng
mka recoveryimage ALLOW_MISSING_DEPENDENCIES=true # Only if you use minimal twrp tree.
```

To test it:

```
fastboot flash recovery out/target/product/kunlun2/recovery.img
```

## Other Sources

Kernel Sources: using precompiled stock kernel

