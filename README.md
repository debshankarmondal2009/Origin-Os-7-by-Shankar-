# Origin Launcher

An original, OriginOS-inspired home screen for Android (Kotlin, no third-party dependencies beyond AndroidX).
It does not use any Vivo/OriginOS icons, wallpapers or code.

## What you get
- Paged home screen with every app on it (no app drawer, like OriginOS)
- Big light-weight clock and date at the top
- Floating translucent dock (up to 5 apps)
- Swipe up anywhere: blurred-style search overlay with the home screen scaling back
- Every app icon re-masked to one shape, so the whole phone looks uniform
- Press-down bounce animation and zoom-from-icon app launch
- Long-press an app: add/remove from dock, hide, app info, uninstall
- Long-press empty space: launcher settings, wallpaper, default launcher

## Customization (long-press empty space > Launcher settings)
Columns, rows per page, icon size, icon roundness (0 = square, 50 = circle),
label on/off and size, dark text for light wallpapers, clock on/off and size,
dock opacity, search opacity, animations, reset dock, unhide apps.

## iOS-style extras
- Today page (swipe right from the first page): date, battery bar, suggested apps (most used)
- App Library page (last page): all apps grouped by type
- Spotlight-style search: swipe down OR up on a home page; type to filter apps,
  do math ("12*8+3"), or search the web
- Haptic feedback on long-press

## Build the APK on your phone only (GitHub Actions, free)
1. Create a free GitHub account, make a new repository, and upload everything in this folder
   (including the hidden .github folder; the GitHub website "Add file > Upload files" works).
2. Open the repo's Actions tab > "Build APK" > wait about 5 minutes for the green tick.
3. Open that run, download the artifact "OriginLauncher-apk", unzip it, install app-debug.apk.

## Build the APK with Android Studio
1. Install Android Studio (free) on a computer.
2. Open this folder (OriginLauncher) with File > Open. Let Gradle sync (needs internet once).
3. Build > Build Bundle(s) / APK(s) > Build APK(s).
4. Copy app/build/outputs/apk/debug/app-debug.apk to your phone and install it
   (allow "install unknown apps" for your file manager).
5. Press the Home button, choose "Origin Launcher", then "Always".

## Notes
- Needs a real wallpaper behind it: set one from the long-press menu.
- If a Gradle sync error mentions the Gradle version, use Gradle 8.9 (already set in
  gradle/wrapper/gradle-wrapper.properties).
- Settings that change at runtime are applied when you return to the home screen.
