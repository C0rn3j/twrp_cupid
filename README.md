# twrp_cupid

Attempt at creating a device tree

https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp/tree/twrp-12.1#getting-started

## Cherrypicked fscrypt

After repo sync cherrypick the patch if platform_manifest_twrp_aosp still requires it:

```console
cd bootable/recovery
git fetch https://gerrit.twrp.me/android_bootable_recovery refs/changes/05/5405/6 && git cherry-pick FETCH_HEAD
```

To get kernel, get https://android.googlesource.com/platform/system/tools/mkbootimg/+/refs/heads/master/unpack_bootimg.py (packed in this repo)

Though it does not look like recovery needs kernel, it's not included in stock recovery.

```console
mkdir -p imgdump
./unpack_bootimg.py --boot_img cupid_eea_global_images_V13.0.16.0.SLCEUXM_20220408.0000.00_12.0_eea/images/boot.img --out imgdump
```
