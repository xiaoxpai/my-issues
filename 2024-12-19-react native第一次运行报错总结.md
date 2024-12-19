
## 你可能会报错，无法下载依赖插件

```text
Error Plugin [id: 'com.facebook.react.settings'] was not found in any of the following sources:
```

### 尝试解决 【本人测试，已解决】

可以尝试修改`settings.gradle`  文件



## 执行指令，报错如下
```bash
npm run android --clear-cache
```

```text
FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':gradle-plugin:shared:compileKotlin'.
> Could not resolve all files for configuration ':gradle-plugin:shared:compileClasspath'.
   > Could not resolve com.google.guava:listenablefuture:9999.0-empty-to-avoid-conflict-with-guava.
     Required by:
         project :gradle-plugin:shared > com.google.guava:guava:31.0.1-jre
      > Could not resolve com.google.guava:listenablefuture:9999.0-empty-to-avoid-conflict-with-guava.
         > Could not get resource 'https://repo.maven.apache.org/maven2/com/google/guava/listenablefuture/9999.0-empty-to-avoid-conflict-with-guava/listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.pom'.
            > Could not GET 'https://repo.maven.apache.org/maven2/com/google/guava/listenablefuture/9999.0-empty-to-avoid-conflict-with-guava/listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.pom'.
               > The server may not support the client's requested TLS protocol versions: (TLSv1.2, TLSv1.3). You may need to configure the client to allow other protocols to be used. For more on this, please refer to https://docs.gradle.org/8.10.2/userguide/build_environment.html#sec:gradle_system_properties in the Gradle documentation.
                  > Remote host terminated the handshake
```


```text
BUILD FAILED in 1m 1s
error Failed to install the app. Command failed with exit code 1: gradlew.bat app:installDebug -PreactNativeDevServerPort=8081 FAILURE: Build failed with an exception. * What went wrong: Execution failed for task ':gradle-plugin:shared:compileKotlin'. > Could not resolve all files for configuration ':gradle-plugin:shared:compileClasspath'. > Could not resolve com.google.guava:listenablefuture:9999.0-empty-to-avoid-conflict-with-guava. Required by: project :gradle-plugin:shared > com.google.guava:guava:31.0.1-jre > Could not resolve com.google.guava:listenablefuture:9999.0-empty-to-avoid-conflict-with-guava. > Could not get resource 'https://repo.maven.apache.org/maven2/com/google/guava/listenablefuture/9999.0-empty-to-avoid-conflict-with-guava/listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.pom'. > Could not GET 'https://repo.maven.apache.org/maven2/com/google/guava/listenablefuture/9999.0-empty-to-avoid-conflict-with-guava/listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.pom'. > The server may not support the client's requested TLS protocol versions: (TLSv1.2, TLSv1.3). You may need to configure the client to allow other protocols to be used. For more on this, please refer to https://docs.gradle.org/8.10.2/userguide/build_environment.html#sec:gradle_system_properties in the Gradle documentation. > Remote host terminated the handshake * Try: > Run with --stacktrace option to get the stack trace. > Run with --info or --debug option to get more log output. > Run with --scan to get full insights. > Get more help at https://help.gradle.org. BUILD FAILED in 1m 1s.
info Run CLI with --verbose flag for more details.
```

###  尝试解决：【本人测试，已解决】

挂梯子，多执行几次指令即可


## 当解决掉上述的所以错误（依赖或插件）无关紧要的异常，会报错，但是不需要解决，也能正常运行app

```text
> Task :app:installDebug
[PropertyFetcher]: ShellCommandUnresponsiveException getting properties for device emulator-5554
java.lang.Throwable: ShellCommandUnresponsiveException getting properties for device emulator-5554
        at com.android.ddmlib.PropertyFetcher.handleException(PropertyFetcher.java:259)
        at com.android.ddmlib.PropertyFetcher$1.run(PropertyFetcher.java:213)
Caused by: com.android.ddmlib.ShellCommandUnresponsiveException
        at com.android.ddmlib.internal.DeviceImpl.lambda$executeRemoteCommand$18(DeviceImpl.java:891)
        at com.android.ddmlib.internal.DeviceImpl.logRun1(DeviceImpl.java:1801)
        at com.android.ddmlib.internal.DeviceImpl.executeRemoteCommand(DeviceImpl.java:755)
        at com.android.ddmlib.internal.DeviceImpl.lambda$executeRemoteCommand$15(DeviceImpl.java:618)
        at com.android.ddmlib.internal.DeviceImpl.logRun1(DeviceImpl.java:1801)
        at com.android.ddmlib.internal.DeviceImpl.executeRemoteCommand(DeviceImpl.java:615)
        at com.android.ddmlib.internal.DeviceImpl.lambda$executeShellCommand$13(DeviceImpl.java:557)
        at com.android.ddmlib.internal.DeviceImpl.logRun1(DeviceImpl.java:1801)
        at com.android.ddmlib.internal.DeviceImpl.executeShellCommand(DeviceImpl.java:554)
        at com.android.ddmlib.PropertyFetcher$1.run(PropertyFetcher.java:209)

Installing APK 'app-debug.apk' on 'Medium_Phone_API_35(AVD)' for :app:debug
Installed on 1 device.
```