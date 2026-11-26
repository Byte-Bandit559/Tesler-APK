# TESLER Android Foundation

**Version:** 0.1.0  
**Package:** `com.tesler.ai`  
**Platform:** Android 8.0+ (API 26+)  
**UI:** Kotlin + Jetpack Compose

## What is included

- Native Android application skeleton.
- Dark TESLER interface.
- Quick and Deep mode selector (selection persists locally).
- Basic local chat UI shell.
- No internet permission and no external AI API.
- No model bundled yet.

## Important status

This is the **foundation shell**, not the finished AI assistant. The chat currently uses placeholder replies. The local language model, durable conversation memory, voice, Android phone actions and plugin manager are future milestones.

## Build

Open this folder in Android Studio with Android SDK 35 installed, allow Gradle sync, then:

- Build > Build Bundle(s) / APK(s) > Build APK(s)

Or from a machine with Gradle and Android SDK configured:

```bash
gradle :app:assembleDebug
```

APK output:

`app/build/outputs/apk/debug/app-debug.apk`

## Design decisions

- Kotlin and Jetpack Compose for native Android integration.
- Minimum SDK 26 to support a broad range of Android devices.
- No network permission in the foundation.
- Quick/Deep are currently UI modes; model routing is not implemented yet.
- Avoid placing a large model in the APK. Add model files as a separate, versioned asset/download package only after measuring RAM and storage on target devices.

## Next milestones

1. Add a model interface (`InferenceEngine`) and connect a small local quantized model.
2. Add persistent chat history and user-approved memory.
3. Add Android capability bridge with explicit permissions and confirmation for sensitive actions.
4. Add voice input/output.
5. Add plugin manifest, discovery and enable/disable controls.
6. Profile on Samsung Galaxy A12 (RAM, latency, battery, storage).
