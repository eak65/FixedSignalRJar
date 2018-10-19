# FixedSignalRJar
Fixed SignalR for Android Client

You might get so many error after having official files for SignalR for Android Client

I would suggest adding following lines in build.gradle file after replacing with the jars would may help

```
splits {
        abi {
            enable true
            reset()
            include 'x86', 'armeabi-v7a'
            universalApk true
        }
    }

packagingOptions {
        exclude 'lib/getLibs.ps1'
        exclude 'lib/getLibs.sh'
        exclude 'lib/gson-2.2.2.jar'
    }
```
