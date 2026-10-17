# DroidWin Launcher (Android project)

A native Android launcher/companion app with a neon gaming UI. It is a **launcher and organizer**, not a Windows emulator.

## Included functionality
- Home dashboard and Winlator installation detection/launch
- Game/application library with saved shortcuts
- Android system document picker for EXE/installers and persisted URI references
- Saved performance preferences (resolution/profile/touch/gamepad guidance)
- Container-management guidance and shortcut into Winlator
- Desktop-mode and input guidance
- Basic Android gamepad/joystick event logging
- Local troubleshooting/activity log
- Python/coding tool guidance

## Important Winlator integration limitation
Winlator does not expose a stable public API for arbitrary third-party apps to create containers, apply graphics settings, or execute a selected EXE inside a specific container. This project therefore opens Winlator and stores file references/preferences, but does not claim to launch selected EXEs directly inside a Winlator container. A selected document URI may not be accessible to Winlator; you may need to copy the file into Winlator's accessible storage using Android's file manager.

Package detection currently checks `com.winlator` and `com.winlator.cmod`. Forks can use different package IDs; edit `MainActivity.kt` if needed.

## Build
1. Install Android Studio and a JDK 17.
2. Open this folder as an existing Android Studio project.
3. Allow Gradle sync and install Android SDK Platform 35 (or adjust `compileSdk`/`targetSdk` to the SDK you have installed).
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK is typically at `app/build/outputs/apk/debug/app-debug.apk`.

This project does not include Gradle wrapper binaries. Android Studio can generate/use the Gradle wrapper or build with its configured Gradle installation.

## Device support
- minSdk 26 (Android 8.0+)
- Android 14 and earlier are supported in principle; exact UI/engine behavior depends on device and Android version.
- No root required for the launcher's features.
- Actual game compatibility depends on Winlator, device CPU/GPU/driver, RAM, storage, and each game's requirements.

## Security
Only install Winlator from a source you trust. Use legally obtained game files. This app does not download game ROMs, cracks, or Windows binaries.
