# TWRP Device Tree for OnePlus Nord N100

The OnePlus Nord N100 is a mid-range smartphone from OnePlus. It was announced in October 2020 and released in November 2020.

## Device specifications

| Feature                 | Specification                                                   |
| :---------------------- | :---------------------------------------------------------------|
| Chipset                 | Qualcomm SM4250 Snapdragon 460 5G (11 nm)                       |
| CPU                     | Octa-core (4x1.8 GHz Kryo 240 Gold & 4x1.6 GHz Kryo 240 Silver) |
| GPU                     | Adreno 610                                                      |
| Memory                  | 4 GB	                                                    |
| Shipped Android Version | 10.0 (OxygenOS 10.5)                                            |
| Storage                 | 64 GB UFS 2.1	                                            |
| SIM                     | Dual SIM (Nano-SIM, dual stand-by)                              |
| MicroSD                 | Up to 512 GB                                                    |
| Battery                 | 5000 mAh Li-Po (non-removable)                                  |
| Dimensions              | 164.9 x 75.1 x 8.5 mm	                                            |
| Display                 | 6.52 inch, 720 x 1600 (20:9 ratio)                              |
| Rear Camera 1           | 13 MP, f/2.2, (wide), PDAF	                                    |
| Rear Camera 2           | 2 MP, f/2.4, 119˚ (macro)	                                    |
| Rear Camera 3           | 2 MP, f/2.4, (depth)                                            |
| Front Camera            | 8 MP, f/2.0                                                     |
| Fingerprint             | Rear-mounted                                                    |
| Sensors                 | Accelerometer, Gyro, Proximity, Compass                         |


## Compile

First checkout minimal twrp with aosp tree:

```
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
repo sync
```

Later, pick needed patches from gerrit/github

```
https://gerrit.twrp.me/c/android_bootable_recovery/+/5405
https://gerrit.twrp.me/c/android_bootable_recovery/+/5670
https://gerrit.twrp.me/c/android_bootable_recovery/+/5533
https://github.com/HemanthJabalpuri/android_bootable_recovery/commit/6d5c365617778d107ccc6b32b55238715a06d0bc
https://gerrit.twrp.me/c/android_system_vold/+/5540
```

Finally execute these:

```
. build/envsetup.sh
lunch twrp_billie2-eng
mka recoveryimage
```
