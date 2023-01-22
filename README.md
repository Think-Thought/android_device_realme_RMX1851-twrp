# TWRP Device Tree for the realme 3 Pro (RMX1851)

![Realme RMX1851](https://static.realme.net/page/realme-3-pro/images/pc/8-Speedway-Design-id-1-9a68411c86.png)

## Build Instructions
```sh
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch twrp_RMX1851-eng
make recoveryimage
```


## Note about ozip decrypt
* This is necessary for downgrades back to stock android-9.0 (ColorOS).
* Early versions of android-10.0(Realme UI v1) have decryptor built into the updater binary so this patch isnt necessary.
* Later versions of android-10.0(Realme UI v1) are not ozip encrypted at all and so is android-11.0 (Realme UI v2) potentially following the OPLUS merger.
* To automate renaming .ozip to .zip, ozip decrypt tool can be used with dummy key for devices launching with android 10 and above.

### Special Thanks:
- Thanks to @pjgowtham for Unified SMD710 tree
- TWRP team
- @mauronofrio
- @SathamHussainM
