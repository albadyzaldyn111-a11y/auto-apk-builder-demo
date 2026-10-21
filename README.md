# Auto APK Builder Demo

A compact Android/Kotlin demonstration of automated APK builds with GitHub Actions.

## What it demonstrates

- Android project setup with Gradle.
- Reproducible debug builds on CI.
- Java 17 and Android toolchain configuration.
- Artifact upload for workflow runs.
- Optional release creation when a version tag is pushed.

## Build locally

```bash
git clone https://github.com/albadyzaldyn111-a11y/auto-apk-builder-demo.git
cd auto-apk-builder-demo
./gradlew assembleDebug
```

## Continuous integration

Pushes to `main` and tags beginning with `v` can trigger the GitHub Actions workflow. The workflow builds the APK and publishes it as an artifact; tagged builds can also be attached to a GitHub Release.

## Project status

Small educational and portfolio project focused on Android CI/CD automation rather than a full production application.
