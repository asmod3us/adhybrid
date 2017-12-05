Sample [Cordova](https://cordova.apache.org) project with an Android platform using the [AppDynamics plugin](https://github.com/asmod3us/appdplugin). Also works with [PhoneGap Build](https://build.phonegap.com).

If you want to set up AppDynamics with your own Cordova or PhoneGap app, here's what to do:

1. Install the [AppDynamics plugin](https://github.com/asmod3us/appdplugin):

    ``` cordova plugin add https://github.com/asmod3us/appdplugin```

    or

    ```phonegap plugin add https://github.com/asmod3us/appdplugin```
1. In some cases, CordovaLib's build.gradle needs to be pointed to jcenter to find the right version of gradle. It will look similar to this after:

    ```
buildscript {
    ...
    repositories {
        mavenCentral()
        jcenter()
    }
    ...
}
```
1. Review the [docs](https://docs.appdynamics.com/display/PRO42/Instrument+a+Mobile+Application) for additional platform-specific setup.
