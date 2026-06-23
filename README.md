# Auto APK Builder Demo 🚀

This is a minimal Android project designed to demonstrate automatic APK building using GitHub Actions.

## Project Overview
- **Language:** Kotlin
- **Build System:** Gradle
- **CI/CD:** GitHub Actions

## How it works
Every time you push code to the `main` branch or create a new tag starting with `v` (e.g., `v1.0`), GitHub Actions will:
1. Set up a Java 17 environment.
2. Build the project using `./gradlew assembleDebug`.
3. Upload the resulting APK as a build artifact.
4. If a tag was pushed, it will automatically create a **GitHub Release** and attach the APK.

## How to get the APK
1. **From Actions:** Go to the "Actions" tab in this repository, click on the latest workflow run, and scroll down to "Artifacts".
2. **From Releases:** If a tag was created, go to the "Releases" section on the right side of the repository page to find the direct download link.

## How to trigger a Release
To trigger an automatic release with the APK, run these commands in your terminal:
```bash
git tag v1.0
git push origin v1.0
```

## Local Development
To build the project locally, ensure you have JDK 17 installed and run:
```bash
./gradlew assembleDebug
```
The APK will be located at `app/build/outputs/apk/debug/app-debug.apk`.
