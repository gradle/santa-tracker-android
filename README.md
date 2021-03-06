Google Santa Tracker for Android 🎅🤶
================================

## About

This repo is a fork of the [Google Santa Tracker app for Android](https://github.com/google/santa-tracker-android).  This for was created to as a companion sample to demonstrate some of the tips and tricks on how to speed up your Android Gradle builds.

## How to use this repo
Check out this repo and switch to the agp-3.5.0 branch. This branch contains the pre-optimized build configurations. See [Getting the first build working section](#firstbuild).

Best way to observe the build performance in this branch is to use the [Gradle profiler] (https://github.com/gradle/gradle-profiler). You should familiarize yourself with the Gradle profiler before proceeding. Their repo contains excellent documentation.

Once you have observed the build performance of this branch in various scenarios (see `performance.scenarios`), you can switch to agp-3.0.0 branch to observe the optimized build performance by running the same set of build scenarios in `performance.scenarios` file. You can search throughout the project for "Tip" to find the build config tip to achieve the build time improvements.

![Village Screenshot](docs/village.png)


## Getting the first build working<a name="firstbuild"></a>

First up, Santa Tracker is powered by [Firebase][firebase], so you'll need to enable it
on your Google account over at the [Firebase console][fire-console]. Once you're in the
console, follow these steps:

 * Create a new project
 * Add Firebase to your Android app
 * Package name: `com.google.android.apps.santatracker.debug`
 * Debug signing certificate can be blank, or follow the instructions in the tooltip to find yours.
 * Save the `google-services.json` file to the `santa-tracker/` directory

Now you should be able to plug your phone in (or fire up an emulator) and run:

    ./gradlew santa-tracker:installDebug

Alternatively, import the source code into Android Studio (File, Import Project).

Note: You'll need Android SDK version 28. If you're unsure about this, use
Android Studio and tick the appropriate boxes in the SDK Manager.

## License

All image and audio files (including *.png, *.jpg, *.svg, *.mp3, *.wav, *.ogg, *.m4a, *.webp) are
licensed under the CC-BY-NC license. All other files are licensed under the Apache 2 license.
See the LICENSE file for details.

    Copyright 2019 Google LLC

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        https://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


[play-store]: https://play.google.com/store/apps/details?id=com.google.android.apps.santatracker
[santa-web]: http://g.co/santatracker
[firebase]: https://firebase.google.com/
[fire-console]: https://firebase.google.com/console/
