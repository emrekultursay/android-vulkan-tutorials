Tutorial 6 - Texture
=============================
Render a textured triangle


Description
----------
*  adding texture to triangle


Requirement
--------------
Pre-build shaderc with:
```
 mkdir -p  app/src/main/cpp/shaderc
 cd app/src/main/cpp/shaderc
 ${ANDROID_NDK}/ndk-build -j 10 NDK_PROJECT_PATH=. APP_BUILD_SCRIPT=${ANDROID_NDK}/sources/third_party/shaderc/Android.mk APP_STL:=${ANDROID_STL} APP_ABI:=arm64-v8a,x86_64 APP_PLATFORM:=${APP_PLATFORM} libshaderc_combined
```

Replace the `ANDROID_NDK`, `ANDROID_STL`, and `APP_PLATFORM` with appropriate values, such as the
path to NDK r25.1, `c++_static`, and `latest`.

This build step can take 3-5 minutes. If you only care about a single ABI, setting `APP_ABI`
accordingly will reduce this build time by half.

Screenshot
------------
<img src="./Tutorial_6_Screenshot.png" height="400px">


Known Issues
------------

On Windows, you may encounter the following build error during `shaderc` compilation:

```
$ANDROID_NDK/toolchains/llvm/prebuilt/windows-x86_64/bin/llvm-ar.exe: error: script line 1: unknown command: "create
```

In this case, edit the following generated files and remove all copies of double quotes (i.e., the
'"' char):

```
tutorial06_texture/app/src/main/cpp/shaderc/obj/local/arm64-v8a/combine.ar
tutorial06_texture/app/src/main/cpp/shaderc/obj/local/x86_64/combine.ar
```
