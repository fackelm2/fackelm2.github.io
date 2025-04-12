---
layout: post
title: Android Dumpsys
date: 2024-09-10 18:00:10
last_updated: 2024-09-10 18:00:10
description: Android Dumpsys
tags: android forensic
categories: forensic
featured: false
---

draft

Example (Get all Databases, Diskstats (of package name), ..)

```
dumpsys dbinfo -v
dumpsys diskstats
dumpsys notifications
dumpsys notifications --noredact
dumpsys package
dumpsys usagestats
dumpsys vibrator
dumpsys wifi

```

[Android Dumpsys]: https://developer.android.com/tools/dumpsys?hl=de "https://developer.android.com/tools/dumpsys?hl=de"

[Android Dumpsys]

[Android Dumpsys Analysis]: https://ccdcoe.org/uploads/2021/03/Android-Dumpsys-Analysis-to-Indicate-Driver-Distraction.pdf "https://ccdcoe.org/uploads/2021/03/Android-Dumpsys-Analysis-to-Indicate-Driver-Distraction.pdf"

[Android Dumpsys Analysis]

[Android Dumpsys Analysis 1]: https://ccdcoe.org/library/publications/android-dumpsys-analysis-to-indicate-driver-distraction/ "https://ccdcoe.org/library/publications/android-dumpsys-analysis-to-indicate-driver-distraction/"

[Android Dumpsys Analysis 1]

[Stackoverflow dumpsys]: https://stackoverflow.com/questions/11201659/whats-the-android-adb-shell-dumpsys-tool-and-what-are-its-benefits "https://stackoverflow.com/questions/11201659/whats-the-android-adb-shell-dumpsys-tool-and-what-are-its-benefits"

[Stackoverflow dumpsys]

[Android Debugging using dumpsys]: https://medium.com/make-android/android-debugging-using-dumpsys-9bf1de695dcc "https://medium.com/make-android/android-debugging-using-dumpsys-9bf1de695dcc"

[Android Debugging using dumpsys]

[dumpsys commands]: https://www.repeato.app/demystifying-adb-shells-dumpsys-command-and-its-benefits-for-android-development/ "https://www.repeato.app/demystifying-adb-shells-dumpsys-command-and-its-benefits-for-android-development/"

[dumpsys commands]
