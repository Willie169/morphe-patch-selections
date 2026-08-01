## Morphe Patch Selections

This repo contains my patch selections for [Morphe Patches](https://github.com/MorpheApp/morphe-patches).

### Usage

1. Install Morphe according to guides in [Morphe Patches](https://github.com/MorpheApp/morphe-patches).
2. Add [adobo](https://github.com/jkennethcarino/adobo) source according to guides in it.
3. Download [`morphe_all_selections.json`](https://raw.githubusercontent.com/Willie169/morphe-patch-selections/refs/heads/main/morphe_all_selections.json) from this repo.
4. In Morphe, go to Settings > Advanced and enable Expert mode.
5. In Morphe, go to System > Patch selections and Import the downloaded `morphe_all_selections.json`.
6. Patch apps.
  - For those apps whose selections include `Block ads, trackers, and analytics`, download [`all.txt`](https://raw.githubusercontent.com/Willie169/morphe-patch-selections/refs/heads/main/all.txt) from this repo and put it in `/storage/emulated/0/Download/all.txt` or edit the selection option to match where you downloaded `all.txt`.
  - For those with a recommended version from the sources, obtain the corresponding version from a trusted source such as [APKMirror](https://www.apkmirror.com).
  - For those without a recommended version, you may either
    - obtain the app from a trusted source such as [APKMirror](https://www.apkmirror.com), of which the latest version is typically recommended, or
    - install the app from Google Play or Aurora Store, let Morphe extract from your installed one, and then uninstall it to install the patched one.
  - When obtaining an original app from a source, make sure to
    - match your device' architechture: universal or your device architechture, typically
      - arm64 or arm64-v8a for mordern phones,
      - arm, armeabi, or armeabi-v7a for older phones,
      - x86\_64 for most emulators on PCs,
      - x86 for 32-bit emulators on PCs.
    - match your Android system version.
    - match your device's dpi: 
      - Apps marked nodpi or not marked with any DPI-related info at all are meant for all devices.
      - Apps marked with dpi or dpi range are meant for specific DPIs only. You may use it if you know your device's DPI. Apps marked with 120-640dpi are typically ok for most devices.

