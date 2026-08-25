## Morphe Patch Selections

This repo contains my patch selections for [Morphe Patches](https://github.com/MorpheApp/morphe-patches).

### Usage

1. Install Morphe according to guides in [Morphe Patches](https://github.com/MorpheApp/morphe-patches).
2. Add [adobo](https://github.com/jkennethcarino/adobo) source according to guides in it.
3. Download [`morphe_all_selections.json`](https://raw.githubusercontent.com/Willie169/morphe-patch-selections/refs/heads/main/morphe_all_selections.json) from this repo.
4. In Morphe, go to Settings > Advanced and enable Expert mode.
5. In Morphe, go to System > Patch selections and Import the downloaded `morphe_all_selections.json`.
6. Obtain original APKs.
  * RAR original APK can be downloaded from its [official site](https://www.win-rar.com/download.html).
  * ONLYOFFICE Documents original APK can be downloaded from its [official site](https://download.onlyoffice.com/install/mobile/android/onlyoffice-documents.apk).
  * Original APKs may be downloaded from [APKPure](https://apkpure.com), [APKMirror](https://www.apkmirror.com), etc. Make sure to:
    * match your device architechture: universal or your device architechture, typically
      + arm64 or arm64-v8a for mordern phones,
      + arm, armeabi, or armeabi-v7a for older phones,
      + x86\_64 for most emulators on PCs,
      + x86 for 32-bit emulators on PCs.
    * match your Android system version.
    * match your device's dpi: 
      + Apps marked nodpi or not marked with any DPI-related info at all are meant for all devices.
      + Apps marked with dpi or dpi range are meant for specific DPIs only. You may use it if you know your device's DPI. Apps marked with 120-640dpi are typically ok for most devices.
  - Original APKs may be obtained by installing the app from Google Play or Aurora Store and letting Morphe extract from it.
7. Patch apps.

### Notes

- Gboard's internet connection permission is not removed because keyboards of many languages need to download additional resources in the initial setup.
- Earphone Alarm's internet connection permission is not removed because removing it will cause the following crash
  ```
  AndroidRuntime: FATAL EXCEPTION: main
  AndroidRuntime: Process: com.wixsite.ut_app.utalarm.adobo, PID: 13707
  AndroidRuntime: java.lang.RuntimeException: Unable to create application com.wixsite.ut_app.utalarm.MyApplication: java.lang.IllegalArgumentException: Purchases requires INTERNET permission.
  AndroidRuntime: 	at android.app.ActivityThread.handleBindApplication(ActivityThread.java:8756)
  AndroidRuntime: 	at android.app.ActivityThread.-$$Nest$mhandleBindApplication(Unknown Source:0)
  AndroidRuntime: 	at android.app.ActivityThread$H.handleMessage(ActivityThread.java:2873)
  AndroidRuntime: 	at android.os.Handler.dispatchMessage(Handler.java:110)
  AndroidRuntime: 	at android.os.Looper.loopOnce(Looper.java:273)
  AndroidRuntime: 	at android.os.Looper.loop(Looper.java:363)
  AndroidRuntime: 	at android.app.ActivityThread.main(ActivityThread.java:10060)
  AndroidRuntime: 	at java.lang.reflect.Method.invoke(Native Method)
  AndroidRuntime: 	at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:632)
  AndroidRuntime: 	at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:975)
  AndroidRuntime: Caused by: java.lang.IllegalArgumentException: Purchases requires INTERNET permission.
  AndroidRuntime: 	at com.revenuecat.purchases.PurchasesFactory.validateConfiguration(PurchasesFactory.kt:322)
  AndroidRuntime: 	at com.revenuecat.purchases.PurchasesFactory.createPurchases(PurchasesFactory.kt:66)
  AndroidRuntime: 	at com.revenuecat.purchases.PurchasesFactory.createPurchases$default(PurchasesFactory.kt:57)
  AndroidRuntime: 	at com.revenuecat.purchases.Purchases$Companion.configure(Purchases.kt:879)
  AndroidRuntime: 	at com.wixsite.ut_app.utalarm.MyApplication.onCreate(MyApplication.kt:27)
  AndroidRuntime: 	at android.app.Instrumentation.callApplicationOnCreate(Instrumentation.java:1384)
  AndroidRuntime: 	at android.app.ActivityThread.handleBindApplication(ActivityThread.java:8750)
  AndroidRuntime: 	... 9 more
  ```

