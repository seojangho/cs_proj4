# Computer Security Project4
SNU Computer Security (2015fall) Project 4

[@seojangho](https://github.com/seojangho) (JangHo Seo) & [@lastone817](https://github.com/lastone817) (DongJin Shin)

## How to build

Basically follow the instructions on http://appanalysis.org/download.html, with `.repo/local_manifests/local_manifest.xml` in the following

```
<manifest>
  <remote name="github" fetch="git://github.com"/>
  <remove-project name="platform/dalvik"/>
  <project path="dalvik" remote="github" name="seojangho/android_platform_dalvik" revision="jangho"/>
  <remove-project name="platform/libcore"/>
  <project path="libcore" remote="github" name="TaintDroid/android_platform_libcore" revision="taintdroid-4.3_r1"/>
  <remove-project name="platform/frameworks/base"/>
  <project path="frameworks/base" remote="github" name="seojangho/android_platform_frameworks_base" revision="jangho"/>
  <remove-project name="platform/frameworks/native"/>
  <project path="frameworks/native" remote="github" name="TaintDroid/android_platform_frameworks_native" revision="taintdroid-4.3_r1"/>
  <remove-project name="platform/frameworks/opt/telephony"/>
  <project path="frameworks/opt/telephony" remote="github" name="TaintDroid/android_platform_frameworks_opt_telephony" revision="taintdroid-4.3_r1"/>
  <remove-project name="platform/system/vold"/>
  <project path="system/vold" remote="github" name="TaintDroid/android_platform_system_vold" revision="taintdroid-4.3_r1"/>
  <remove-project name="platform/system/core"/>
  <project path="system/core" remote="github" name="TaintDroid/android_platform_system_core" revision="taintdroid-4.3_r1"/>
  <remove-project name="device/samsung/manta"/>
  <project path="device/samsung/manta" remote="github" name="TaintDroid/device_samsung_manta" revision="taintdroid-4.3_r1"/>
  <remove-project name="device/samsung/tuna"/>
  <project path="device/samsung/tuna" remote="github" name="TaintDroid/android_device_samsung_tuna" revision="taintdroid-4.3_r1"/>
  <project path="packages/apps/TaintDroidNotify" remote="github" name="TaintDroid/android_platform_packages_apps_TaintDroidNotify"
      revision="taintdroid-4.3_r1"/>
</manifest>

```

## What to expect

* All the functionalities of TaintDroid must work correctly
* Through `adb logcat`, method calls with tainted arguments are printed with thread ID, caller name, caller name, and taint type(s).

## Related repositories

* [seojangho/android_platform_dalvik](https://github.com/seojangho/android_platform_dalvik)
* [seojangho/android_platform_frameworks_base](https://github.com/seojangho/android_platform_frameworks_base)
