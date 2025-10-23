# Prerequisites

- PC
- Knowledge of Java/Kotlin, Android, adb and git
- [Android Studio](https://developer.android.com/studio) - While you can technically make plugins with any IDE, Android Studio is by far the easiest and most convenient as it manages many things for you
- [Java SDK](https://jdk.java.net/11/) - Comes with Android Studio
- [Android Platform Tools](https://developer.android.com/studio/releases/platform-tools) - Comes with Android Studio
- [Git](https://git-scm.com/downloads)
- [Jadx](https://github.com/skylot/jadx) - This is used to decompile the Discord apks to human readable java files

<details>
<summary>Java warning!</summary>
<br>
You may get errors while using gradle with JDK11. If that's your case, please put the following line in your gradle.properties file:

```
org.gradle.jvmargs=-Dhttps.protocols=TLSv1.2
```
</details>

<details>
<summary>Manually getting Android tools</summary>
<br>
If you dont want to use Android Studio (for some reason), heres the following tools you'll need:
- Android build-tools;30.0.2
- Android platforms;31.0.0
</details>


