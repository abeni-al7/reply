# Reply

An email client UI with sample data that adapts its layout to the window width: bottom navigation on phones, a navigation rail on medium screens and a permanent drawer with list-and-detail view on large screens.

Built while following Google's [Android Basics with Compose](https://developer.android.com/courses/android-basics-compose/course) course (the "Reply" adaptive-layouts codelab).

## Features

- Inbox, Drafts, Sent and Spam mailboxes with locally provided sample emails and accounts
- Tap an email to open its details; system Back returns to the list
- Mailbox-specific action buttons (e.g. Reply, Reply All, Delete) that show a toast
- Compact: bottom `NavigationBar`; Medium: `NavigationRail`; Expanded: `PermanentNavigationDrawer` with email list and details side by side

## Built with

- Kotlin, Jetpack Compose, Material 3, Material Icons Extended
- `material3-window-size-class` (`calculateWindowSizeClass`) for adaptive layouts
- `ViewModel` with `StateFlow<ReplyUiState>`, `BackHandler`
- Instrumented tests for each window size and for state restoration across configuration changes (`StateRestorationTester`)
- Min SDK 24, target/compile SDK 35

## Run it

1. Open the project folder in Android Studio and let Gradle sync.
2. Run the `app` configuration on an emulator or device (Android 7.0 / API 24 or newer).

Or, with a device or emulator connected:

```sh
./gradlew installDebug
```

Instrumented UI tests (needs a device or emulator): `./gradlew connectedAndroidTest`
