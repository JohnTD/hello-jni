Hello JNI
=========

Android平台：集成NDK，JNI，Gradle等功能，已实现Hello World功能.....

优点：纯命令行搭建，免去Android studio等繁杂软件的安装及使用。

使用方法：

1. sdk, ndk开发环境搭建, 确保android, ndk-build等程序正常运行;

2. 使用android sdk manager安装如下插件：
Tools:
    Android SDK Tools
    Android SDK Platform-tools
    Android SDK Build-tools
Android 4.4.2(API 19): (具体视手机系统定)
    SDK Platform
    Samples for SDK
    ARM EABI v7a System Image
    Google APIs(ARM System Image)
    Sources for Android SDK
Extras:
    Android Support Respository
    Android Support Library
    Google Respository

3. 修改local.properties内容改为本机sdk, ndk目录;

4. 修改app/build.gradle:
compileSdkVersion, buildToolsVersion

5. gradle2.8安装, 并在目录下执行：
gradle init wrapper
./gradlew
./gradlew clean
./gradlew build
在hello-jni/app/build/output/apk下会生成app-arm7-debug-unaligned.apk

6. hello-jni/app/src/main/下运行命令生成so库文件:
ndk-build
