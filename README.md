# VoltageOS 17 for merlinx and lancelot

Initialize the Android 17 sources and add this local manifest:

```bash
repo init -u https://github.com/VoltageOS/manifest.git -b 17 --git-lfs
git clone -b vos https://github.com/MrShockWAVEog/manifest.git .repo/local_manifests
repo sync
```

The `vos` branches of the common and device trees must be pushed before syncing.
Both devices build without bundled GApps (`WITH_GAPPS := false`) and display
`MrShockWAVEog` as the maintainer. Builds default to `UNOFFICIAL`.

Build either device:

```bash
source build/envsetup.sh
brunch merlinx userdebug
# Or: brunch lancelot userdebug
```
