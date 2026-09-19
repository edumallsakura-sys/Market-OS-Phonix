ALPHAFLOW OS v1.1.7 — STANDALONE BUNDLE HOTFIX

IMPORTANT: v1.1.6 produced an installable Debug APK but it did not contain
assets/index.android.bundle, so the installed app required Metro and showed the
red "Unable to load script" screen.

Recommended upload:
1) Extract THIS ONECLICK ZIP locally.
2) Replace these two paths in the GitHub repository:
   .github/workflows/build-apk.yml
   projects/ALPHAFLOW_OS_SOURCE.zip
3) Run workflow:
   Build ALPHAFLOW OS v1.1.7 APK - STANDALONE BUNDLE HOTFIX
4) Download artifact:
   ALPHAFLOW-OS-v1.1.7-STANDALONE-APK
5) Install ALPHAFLOW-OS-v1.1.7-standalone.apk.

Safety net:
The source itself forces JS bundling even for Debug, so an older workflow that
still chooses assembleDebug should no longer produce a Metro-dependent APK.
