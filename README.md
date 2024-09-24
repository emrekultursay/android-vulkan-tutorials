Tutorial Samples
================
A set of samples to illustrate Vulkan API on Android with Android Studio.

To build the samples:
- Inside Android Studio, use File --> New --> Import Project
- Find your sample's directory or `build.gradle` file, and open it

This will force Andrioid Studio to create local.properties file to config your SDK location. If you see
an Android SDK error during importing, you can open local.properties file and correct the SDK path.

Other Resources:	
Additional Android Studio/NDK samples:    
- [Android Vulkan API Basic Samples](https://github.com/googlesamples/vulkan-basic-samples)
- [Google Play Game Samples](https://github.com/playgameservices/cpp-android-basic-samples)
- [Google Android NDK Samples](https://github.com/googlesamples/android-ndk)

Contents
-------------
- [Tutorial 1 - Load Vulkan](./tutorial01_load_vulkan)
  - create a vulkan device
- [Tutorial 2 - Prebuilt Layers](./tutorial02_prebuild_layers)
  - create a vulkan device with vulkan validation layers
- [Tutorial 3 - Traceable Layers](./tutorial03_traceable_layers)
  - create a vulkan device with validation layers that could be traced.
Refer to README.md under its directory
- [Tutorial 4 - First Window](./tutorial04_first_window)
  - create a vulkan window with WSI 
- [Tutoiral 5 - Triangle](./tutorial05_triangle)
  - draw a simple triangle with Android Studio integrated shaderc feature
- [Tutorial 6 - Texture](./tutorial06_texture)
  - draw textured triangle with [CDep](https://github.com/google/cdep) packed shaderc pre-built binary
  - glsl shaders are compiled at app run time (similar to openGL traditional shader compiling model)

Pre-requisites
--------------
- A device running Android 8.0 (API level 26) or higher
- [Android Studio Jellyfish](https://developer.android.com/studio/index.html) or higher
- Android NDK r25c
    * [NDK](https://developer.android.com/ndk/downloads/index.html)
- CMake 3.22.1 from Android SDK

Test Matrix
------------
| Andrid Studio         | CMake       | NDK      | Device          | API Level |
|-----------------------|-------------|----------|-----------------|-----------|
| Jellyfish 2023.3.1    | 3.22.1      | r25c     | Pixel 7 Pro     | 34        |
| Jellyfish 2023.3.1    | 3.22.1      | r25c     | x86_64 Emulator | 31        |


Known Issues
------------

On Windows, if you hit the maximum 260 character path limit issue, copy/install the NDK
to a directory close to the file system root (e.g., `C:`).

Getting Started
---------------
- From the Welcome screen, select "Import Project" (or, if you already have a project open, select File > New > Import Project)
- Navigate to the sample you downloaded and click OK

License
-------
Copyright 2024 Google, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
