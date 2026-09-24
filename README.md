# Idle Pirate: build the APK

## Easiest: GitHub builds it for you (no installs)
1. Create a free GitHub account and a new empty repository.
2. Upload ALL files from this folder (including the hidden .github folder) to it.
3. Open the repo's "Actions" tab and wait for "Build APK" to finish (about 5 minutes).
4. Open the finished run and download the "idle-pirate-apk" artifact. Unzip it to get app-debug.apk.
5. Send the APK to your phone, allow "install unknown apps" for your browser or file manager, and tap it.

## Or build on your computer
Needs Node 20+, Java 17 and Android Studio (for the Android SDK):
npm install && npx cap add android && npx cap sync android && cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk

Note: Fleets (multiplayer) only work inside Claude, so in the APK that tab shows a "not available" message. Everything else works offline and saves on your phone.
