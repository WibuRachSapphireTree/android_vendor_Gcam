android_vendor_Gcam
===================
## How to use
Just clone the repository and add this line to your device.mk file of device tree if you want to use Gcam instead of the default camera on your rom.

```make
$(call inherit-product, vendor/Gcam/config.mk)
```
