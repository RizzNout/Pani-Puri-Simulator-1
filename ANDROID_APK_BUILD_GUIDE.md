# Pani Puri Simulator 3D — Android APK build

This package keeps the existing React/Vite/Three.js game source and adds a cloud Android APK build workflow.

## Build an APK from an Android phone

1. Download and extract this ZIP on your phone (or upload the ZIP contents to a new GitHub repository).
2. On GitHub, create a new repository and upload the extracted project files. Make sure `.github/workflows/android-apk.yml` is included. GitHub's mobile website may require the desktop-site view for uploading folders; uploading via Git is easier if available.
3. Open the repository's **Actions** tab.
4. Select **Build Android APK** and tap **Run workflow**. Alternatively, pushing to `main` or `master` triggers the workflow.
5. When the run succeeds, open that run, scroll to **Artifacts**, and download `pani-puri-simulator-debug-apk`.
6. Extract the artifact ZIP; it contains `app-debug.apk`. Open it on your Android phone and approve installation from that source if Android asks.

## Notes

- The workflow builds a **debug APK** for testing. It is not a signed release APK for Play Store publishing.
- The workflow applies landscape orientation to the main Android activity.
- This build package has not been run in a real Android SDK environment here. The first cloud build may reveal dependency or compatibility issues that need fixing.
- If the game depends on environment variables or API keys, configure required values securely in GitHub Actions Secrets; do not commit secrets to the repository.
- Never upload Google passwords, private tokens, or API keys into chat or a public repository.
