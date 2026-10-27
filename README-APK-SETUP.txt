MarketOS Android APK project

Upload the CONTENTS of this package to the root of:
https://github.com/eagleiam20-create/marketos-onefile

Expected repository layout:
.github/workflows/build-apk.yml
android/settings.gradle
android/build.gradle
android/gradle.properties
android/app/build.gradle
android/app/src/main/AndroidManifest.xml
android/app/src/main/java/com/marketos/app/MainActivity.java
android/app/src/main/res/values/styles.xml
android/app/src/main/assets/index.html

IMPORTANT:
- Upload folders/files, not just the ZIP file.
- If the repository already has files with these paths, replace them with the matching files from this package.
- Then open GitHub > Actions > Build MarketOS Android APK > Run workflow.
- If successful, download the MarketOS-debug-APK artifact and extract app-debug.apk.
- This creates a debug/test APK, not a Play Store release.
- The included HTML is wrapped in a native Android WebView. Supabase backend functionality must still be configured and tested; placeholder credentials or incomplete backend logic will not work automatically.
- Never put a Supabase service_role/secret key in the HTML.
