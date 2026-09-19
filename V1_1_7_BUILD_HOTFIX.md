# ALPHAFLOW OS v1.1.7 — Standalone bundle hotfix

Verified failure in the user's v1.1.6 APK:
- APK size: about 189 MB.
- `assets/index.android.bundle`: MISSING.
- Result: installed app opened React Native's red `Unable to load script` screen.

v1.1.7 fixes this in two layers:
1. Expo prebuild config plugin forces JS bundling for Debug variants as a safety net.
2. GitHub Actions prefers Release and validates the final APK contains
   `assets/index.android.bundle` before upload.

The workflow refuses to publish another APK with a missing JS bundle.
No functional module was removed.
