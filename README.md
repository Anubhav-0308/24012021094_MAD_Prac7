# MAD Practical 7 – Person Data Management App

<img width="716" height="1600" alt="WhatsApp Image 2026-10-09 at 18 41 18" src="https://github.com/user-attachments/assets/3506176f-7617-4b91-98fb-afd6e38d0810" />

## Overview
This is an Android application developed in Kotlin for Mobile Application Development (MAD) Practical 7. It retrieves person records from a web API, displays them in a `RecyclerView`, and stores records locally in an SQLite database so the data can be loaded from the device.

## Features
- Fetches person data from a remote JSON API.
- Displays records using `RecyclerView` and a custom adapter.
- Saves and updates person records in a local SQLite database.
- Loads previously saved records from the local database.
- Supports deleting a person record from the list and database.
- Uses Kotlin coroutines for background work.

## Built With
- Kotlin
- Android Studio
- Android SDK (configured with compile SDK 36)
- AndroidX AppCompat and Core KTX
- Material Components
- RecyclerView
- SQLite
- JSON and Kotlin Coroutines

## Project Structure
```text
app/src/main/
├── AndroidManifest.xml
├── java/com/example/a24012021094_anubhav_prac7/
│   ├── MainActivity.kt       # Main screen and API/database coordination
│   ├── Person.kt             # Person data model
│   ├── PersonAdapter.kt      # RecyclerView adapter
│   ├── DatabaseHelper.kt     # Local SQLite database operations
│   ├── PersonDbTable.kt      # Database table definition
│   └── HttpRequest.kt        # HTTP request helper
└── res/
    ├── layout/activity_main.xml
    ├── layout/single_item.xml
    └── ...
```

## Requirements
- Android Studio with Android SDK 36 installed.
- A device or emulator supported by the app's configured minimum SDK (API 35).
- Internet access to retrieve remote person data.

## How to Run
1. Download or clone this repository.
2. Open the project folder in Android Studio.
3. Allow Gradle to sync and install any required SDK components.
4. Connect an Android device or start an emulator that meets the app's minimum SDK requirement.
5. Click **Run ▶** to build and launch the app.
6. Allow the app to access the internet if prompted by your environment. The app fetches data when it starts; use the floating action button to request the data again.

## Notes
- The API endpoint and authorization token are currently written directly in `MainActivity.kt`. For a public repository, move credentials to a safer configuration and rotate/revoke any exposed token. Do not commit secrets to GitHub.
- API availability and response format may change. If records do not load, check the internet connection and Logcat output.
- The project currently sets `minSdk = 35`, so older Android devices and emulators will not be able to install it unless that setting is changed appropriately.

## Author
**Anubhav Kanthariya**  
B.Tech – Mobile Application Development Practical 7
