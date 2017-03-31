VirtualHook
-----------

## Introduction 

VirtualHook is a tool for hooking application without root permission. It is based on two projects:

- [VirtualApp](https://github.com/asLody/VirtualApp). It's a plugin framework which allows running applications in its virtual space.
- [YAHFA](https://github.com/rk700/YAHFA). It's a hook framework for ART which allows hooking Java method of the application.

Since YAHFA supports Android 6.0 and 5.1, currently VirtualHook would only run on those platforms.

## Build

Import and build the project in Android Studio. There are four modules:

- `app`. This is the VirtualApp application module.
- `lib`. This is the VirtualApp library module.
- `YAHFA`. This is the YAHFA hook module.
- `demoHookPlugin`. This is a demo hook plugin which compiles to an APK.

After building the APKs, push the `demoHookPlugin` APK to device at `/sdcard/io.virtualhook/patch.apk` and run the main application. The hook plugin would be applied to all applications running in VirtualApp.

Please refer to [demoHookPlugin](https://github.com/rk700/VirtualHook/tree/master/VirtualApp/demoHookPlugin) for more details.

## License

Both VirtualApp and YAHFA are distributed under GNU GPL V3.
