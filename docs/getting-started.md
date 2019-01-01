## Setup
> do `npm install --global react-native` this will install react-native globally on your system

> download android studio from https://developer.android.com/studio/?hl=id

> create some emulator https://developer.android.com/studio/run/managing-avds?hl=id

## Installation
> `fork` mobile repository

> after forking you can do `clone` to your system

> do `npm install` or `yarn install`


## Run
> start some emulator

> do `react-native run-android` or `react-native run-ios`

# Structure

```text
.
└── android
    ├── build
    └── app
        ├── app
        ├── build
        └── src
    ├── build.gradle
    └── gradlew
├── ios
├── src
    ├── api
        ├── kegiatan.js
        ├── login.js
        ├── message.js
        ├── pekerjaan.js
        ├── profile.js
        ├── program.js
        └── progress.js
    ├── assets
        └── logo.png
    ├── components
        ├── AppHeader.js
        ├── Authentication.js
        ├── Form.js
        ├── Logo.js
        ├── Permission.js
        ├── Sidebar.js
        └── Toaster.js
    ├── screens
        ├── BaseScreen.js
        ├── ChangeNameScreen.js
        ├── HomeScreen.js
        ├── LoginScreen.js
        ├── PekerjaanDetailScreen.js
        ├── ProfileScreen.js
        ├── ProgressMessageScreen.js
        └── UploadProgressScreen.js
    └── Routes.js    
├── App.js
├── package.json
├── DB.js
└── index.js
    
```