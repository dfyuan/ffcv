﻿## ffcv - furtive fastcv
Now runs in Android Studio. 

## Prerequisites
<ol>
<li> QTI FastCV SDK (binary not included in repo) </li>
<li> ANDROID-NDK (confirmed using version r10e) </li>
<li> ANDROID-SDK API 22 </li>
</ol>

## Building
Certain steps from: https://developer.qualcomm.com/software/fast-cv-sdk/getting-started still apply. 

<ol>
<li> Copy lib/libfastcv.a to your ndk lib directory (e.g <Android-NDK-Root/platforms/<Android API>/arch-arm/usr/lib) </li>
<li> Copy fastcv.h to <Android-NDK-Root/platforms/<Android API>/arch-arm/usr/include/fastcv) </li>
</ol>

Currently, ndk-build is run separately in the jni folder rather than using gradle. 

## Status

- Need to replace deprecated camera interface with UVC (USB Video Class) in YUV420sp fmt, see https://github.com/saki4510t/UVCCamera
- Wifi ADB works, make sure if using VM that you have a bridged interface and are not behind NAT. Then adb connect ip_of_android_device. 

## License
This repository contains proprietary Qualcomm Technologies Incorporated('QTI') software. 
