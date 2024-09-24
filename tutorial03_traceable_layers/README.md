# Tutorial 03 - traceable_layers

This has the same functionality as [Tutorial 2](../tutorial02_prebuild_layers), but building the validation layers
from the Khronos Group Validation Layer source code hosted on [the github repo](https://github.com/KhronosGroup/Vulkan-ValidationLayers.git).

The benefit is:
- You can peek/step into validation layers.
- You can observe the detailed status when validation layer finds issues in your app.

This can be useful for developers who want to know more about validation layers.

# Background

Building validation layers from sources currently requires NDK r25c or newer.

Developers should get the validation layer source from
[the github repo](https://github.com/KhronosGroup/Vulkan-ValidationLayers.git).


# Build Instructions

In this sample, the validation layers is wrapped into a gradle library module called `layerlib`. The `app`
module depends on this `layerlib` module.

The validation layer source code needs to be pulled in on command line before building the sample. Steps:

1. cd tutorial03_traceable_layers/layerlib
2. git clone --recursive https://github.com/KhronosGroup/Vulkan-ValidationLayers.git
3. Now, at this point, open this sample with Android Studio with "Open an Existing Project" option
4. Build the project, and start debugging (Run > Debug App). It can take 5-10 minutes to build on slower machines.

Once the app triggers validation layer assert (embedded on purpose inside this sample in the app), you can see the stack frames
in the Android Studio IDE debugger. You can also step into the validation layer, and check the values of all variables.

## Future Work
- Automically pull the source code automatically in Gradle.

# Screenshot
![screenshot](screenshot.png)

