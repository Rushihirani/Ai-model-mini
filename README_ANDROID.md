# Electro AI — Android Edition V1

This is an Android WebView wrapper around the Electro AI V1 web prototype.

## What this build does
- Creates a native Android launcher app named Electro AI.
- Opens the included responsive interface full-screen.
- Includes Unified, Compare and Auto-pilot interface modes.
- The current interface uses local demo responses. It does **not** yet call live ChatGPT, Claude or Perplexity APIs.

## Important limitation
This package is Android source code, not a compiled APK. A real APK must be built with Android SDK + Gradle. This environment does not have the Android SDK/Gradle build toolchain installed, so it cannot honestly provide a compiled APK binary here.

## Build APK in GitHub Actions (phone-friendly, cloud build)
1. Create a private GitHub repository named `electro-ai-android`.
2. Upload all files and folders from this project ZIP to the repository, keeping the folder structure.
3. Open the repository's **Actions** tab.
4. Select **Build Electro AI APK** and press **Run workflow** (or push to `main`).
5. When the workflow finishes, open its run and download the `Electro-AI-debug-APK` artifact.
6. Extract the downloaded artifact and tap `app-debug.apk` on your Android phone to install it. Android may ask you to allow installation from that browser/file manager; only allow it for this APK you built from your own repository.

## Security and next steps
- Never put provider API keys in `index.html`, Kotlin, or a public repository.
- Live AI must be connected through a secure backend that stores keys server-side.
- This debug APK is for testing. A release APK/AAB needs proper signing before distribution.
