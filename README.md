# twrp_cupid

Attempt at creating a device tree

https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp/tree/twrp-12.1#getting-started

## Cherrypicked fscrypt

After repo sync cherrypick the patch if platform_manifest_twrp_aosp still requires it:

```console
cd bootable/recovery
git fetch https://gerrit.twrp.me/android_bootable_recovery refs/changes/05/5405/6 && git cherry-pick FETCH_HEAD
```
