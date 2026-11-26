# TESLER Android Foundation

Version 0.1.0 · Package `com.tesler.ai` · Android 8.0+ · Kotlin + Jetpack Compose.

## Build a debug APK using GitHub (phone-friendly)

1. Create an empty GitHub repository named `TESLER-Android`.
2. Upload the **contents** of this ZIP to the repository root (do not upload the ZIP itself).
3. Commit the files to the `main` branch.
4. Open the repository's **Actions** tab.
5. Choose **Build TESLER APK** and press **Run workflow** if it has not already started.
6. Wait for the run to finish successfully.
7. Open the completed run and download the `TESLER-debug-apk` artifact.
8. Extract that downloaded artifact ZIP. It contains `app-debug.apk`.
9. Open the APK on Android and allow installation from that source if prompted.

## What's included

- Native Android project skeleton.
- Dark TESLER interface.
- Quick and Deep mode selector, with locally saved selection.
- Basic chat UI shell.
- GitHub Actions workflow to compile a debug APK in the cloud.
- No model or external AI API.

## Important

This is the foundation shell, not the finished AI assistant. Chat replies are placeholders. Model inference, durable conversation memory, voice, Android phone actions and plugin management are future milestones. Quick/Deep currently change the UI's placeholder response only. The workflow produces a debug APK, not a Play Store release. The app has not yet been device-tested.

## Build locally

Requires JDK 17, Android SDK 35 and Gradle 8.9:

```bash
gradle :app:assembleDebug
```
