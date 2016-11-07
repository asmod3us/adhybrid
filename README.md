Sample [Cordova](https://cordova.apache.org) project with an Android platform using the [AppDynamics plugin](https://github.com/steveww/appdplugin). Also works with [PhoneGap Build](https://build.phonegap.com).

If you want to set up AppDynamics with your own Cordova or PhoneGap app, here's what to do:

1. Install the [AppDynamics plugin](https://github.com/steveww/appdplugin):

    ``` cordova plugin add https://github.com/steveww/appdplugin```

    or

    ```phonegap plugin add https://github.com/steveww/appdplugin```
2. Add classpath entry `classpath 'com.appdynamics:appdynamics-gradle-plugin:4.+'` to `build.gradle`. It will look similar to this after:

   ```
buildscript {
...
    dependencies {
        classpath 'com.android.tools.build:gradle:2.2.2'
        classpath 'com.appdynamics:appdynamics-gradle-plugin:4.+'
    }
...
}

    ```
3. In some cases, CordovaLib's build.gradle needs to be pointed to jcenter to find the right version of gradle. It will look similar to this after:

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
4. Review the [docs](https://docs.appdynamics.com/display/PRO42/Instrument+a+Mobile+Application) for additional platform-specific setup.
