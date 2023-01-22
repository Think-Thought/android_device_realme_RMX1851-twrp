# android_device_realme_RMX1851-twrp
Recovery tree for Realme SDM710 devices

## Features

Works:

 - Everything

## Compile

First checkout manifest :

```
repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-11
repo sync
```

Then clone the current device tree onto device/realme/RMXS710


Finally execute these:

```
. build/envsetup.sh
lunch twrp_RMX1851-eng
mka recoveryimage
```

To test it:

```
fastboot flash /path/to/recovery.img
```

## Note about ozip decrypt
* This is necessary for downgrades back to stock android-9.0 (ColorOS).
* Early versions of android-10.0(Realme UI v1) have decryptor built into the updater binary so this patch isnt necessary.
* Later versions of android-10.0(Realme UI v1) are not ozip encrypted at all and so is android-11.0 (Realme UI v2) potentially following the OPLUS merger.
* To automate renaming .ozip to .zip, ozip decrypt tool can be used with dummy key for devices launching with android 10 and above.

## Credits

- Thanks to @pjgowtham for Unified SMD710 tree
- TWRP team