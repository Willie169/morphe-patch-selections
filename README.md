## Morphe Patch Selections

This repo contains my patch selections for [Morphe Patches](https://github.com/MorpheApp/morphe-patches).

### Usage

1. Install Morphe according to guides in [Morphe Patches](https://github.com/MorpheApp/morphe-patches).
2. Add the following sources with deep links or manually:
  - [adobo](https://github.com/jkennethcarino/adobo): [deep link](https://morphe.software/add-source?github=jkennethcarino/adobo)
  - [Morning-Entree-Patches](https://github.com/Entree3k/Morning-Entree-Patches): [deep link](https://morphe.software/add-source?github=Entree3k/Morning-Entree-Patches)
  - [Nai64Patches](https://github.com/Nai64/Nai64Patches): [deep link](https://morphe.software/add-source?github=Nai64/Nai64Patches)
3. Download [`morphe_all_selections.json`](https://raw.githubusercontent.com/Willie169/morphe-patch-selections/refs/heads/main/morphe_all_selections.json) from this repo.
4. In Morphe, go to Settings > Advanced and enable Expert mode.
5. In Morphe, go to System > Patch selections and Import the downloaded `morphe_all_selections.json`.
6. Obtain original APKs.
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
7. Download Block ads, trackers, and analytics host file for apps that need it.
  - For Earphone Alarm (`com.wixsite.ut_app.utalarm`), download [earphone_alarm_host.txt](https://github.com/Willie169/morphe-patch-selections/raw/refs/heads/main/earphone_alarm_host.txt) and put it to `/storage/emulated/0/Download/`.
8. Patch apps.
9. Read the following notices:
  - Package name of MacroDroid is not changed because many functionalities of it rely on it. You have to export data and uninstall the original MacroDroid and then install the patched one and import data to use it. You have to exclude MacroDroid from being updated by other app managers such as Google Play and Obtainium.
  - Remove Internet Permission is not used for Gboard because keyboards of many languages need to download additional resources in the initial setup.
  - Remove Internet Permission and Disable Telemetry is not used for Earphone Alarm because doing so will cause crashes, and thus connections to Google may still occur.
  - Remove Internet Permission is not used for CalcES because doing so will cause crashes, and thus connections to Google may still occur.
  - Remove Internet Permission and Block ads, trackers, and analytics is not used for MacroDroid because doing so will cause crashes or fails when patching, and thus connections to Google will still occur.

For more patches, you may refer to [Morphe Community Patches](https://morphe-patches.software).

