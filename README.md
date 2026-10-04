android_vendor_Gcam
===================
## How to use
Clone the repository into `vendor/Gcam` and add this line to the `device.mk` file of your device tree:

```make
$(call inherit-product, vendor/Gcam/config.mk)
```

By default Gcam is installed **alongside** the stock camera app of your ROM.
