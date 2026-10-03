android_vendor_Gcam
===================
## How to use
Clone the repository into `vendor/Gcam` and add this line to the `device.mk` file of your device tree:

```make
$(call inherit-product, vendor/Gcam/config.mk)
```

By default Gcam is installed **alongside** the stock camera app of your ROM.

## Remove the stock camera (optional)
If you want Gcam to replace the stock camera app, run this single command from the root of your ROM source:

```bash
grep -q overrides vendor/Gcam/Android.bp || sed -i '/privileged: true,/a\    overrides: ["Aperture", "Camera2", "Snap", "SnapdragonCamera"],' vendor/Gcam/Android.bp
```

Then rebuild the ROM. Module names that do not exist in your tree are ignored, so it is safe to leave all of them.
