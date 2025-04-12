---
layout: post
title: Android Timestamps
date: 2024-11-12 09:00:10
last_updated: 2024-11-12 09:00:10
description: Android Timestamps
tags: android forensic
categories: android
featured: false
---

draft

## Android Timestamps

Almost all timestamps will be recorded in UTC and it is up to the tool to apply the appropriate time zone offset.
These timestamps are relatively easy to handle as it doesn’t
matter where the device was at the time the record was made.

- UNIX (Number of seconds since Jan 1st 1970 UTC)
- UNIX Millisecond (Number of milliseconds since Jan 1st 1970 UTC)
- MAC Absolute (Number of seconds since Jan 1st 2001 UTC)
- MAC Nanoseconds (Number of Nano-seconds since Jan 1st 2001 UTC)
- Google Chrome (Number of Microseconds since Jan 1st 1601 UTC)
- Unix timestamps represent the number of seconds that have elapsed since January 1, 1970 (the Unix epoch) and are widely used in many operating systems and file formats.
- Webkit/Chrome timestamps are based on the number of microseconds since January 1, 1601, and are primarily found in browser-related data.
- Cocoa timestamps, also known as “Mac absolute time,” that are used in macOS and iOS systems, represent the number of seconds since January 1, 2001.

Quellen:

[https://cellebrite.com/en/glossary/timestamp-mobile-device-forensics/]: https://cellebrite.com/en/glossary/timestamp-mobile-device-forensics/ "https://cellebrite.com/en/glossary/timestamp-mobile-device-forensics/"
[https://cellebrite.com/en/glossary/timestamp-mobile-device-forensics/]: https://cellebrite.com/en/glossary/timestamp-mobile-device-forensics/ "https://cellebrite.com/en/glossary/timestamp-mobile-device-forensics/"
[https://www.forensicmag.com/3425-Featured-Article-List/614592-Decoding-Time-Leveraging-Timestamps-in-Digital-Forensic-Investigations/]: https://www.forensicmag.com/3425-Featured-Article-List/614592-Decoding-Time-Leveraging-Timestamps-in-Digital-Forensic-Investigations/ "https://www.forensicmag.com/3425-Featured-Article-List/614592-Decoding-Time-Leveraging-Timestamps-in-Digital-Forensic-Investigations/"

- [https://cellebrite.com/en/glossary/timestamp-mobile-device-forensics/]
- [https://www.forensicmag.com/3425-Featured-Article-List/614592-Decoding-Time-Leveraging-Timestamps-in-Digital-Forensic-Investigations/]
- [https://cellebrite.com/en/glossary/timestamp-mobile-device-forensics/]

[https://www.youtube.com/watch?v=RYI-grgwQI8]: https://www.youtube.com/watch?v=RYI-grgwQI8 "https://www.youtube.com/watch?v=RYI-grgwQI8"
[https://www.youtube.com/watch?v=cPUpt6_crVM]: https://www.youtube.com/watch?v=cPUpt6_crVM "https://www.youtube.com/watch?v=cPUpt6_crVM"

- Using Built-in Keyword Search Inside Content Within Cellebrite Physical Analyzer: [https://www.youtube.com/watch?v=RYI-grgwQI8]
- How to Verify Timestamps in Cellebrite Physical Analyzer for Digital Investigations: [https://www.youtube.com/watch?v=cPUpt6_crVM]

## Problems

[https://abrignoni.blogspot.com/2020/03/trust-but-verify-formats-timestamps-and.html]: https://abrignoni.blogspot.com/2020/03/trust-but-verify-formats-timestamps-and.html "https://abrignoni.blogspot.com/2020/03/trust-but-verify-formats-timestamps-and.html"

- [https://abrignoni.blogspot.com/2020/03/trust-but-verify-formats-timestamps-and.html]

## Timestamps Bluetooth Connections

[https://cellebrite.com/en/how-android-bluetooth-connections-can-determine-if-the-hands-of-a-driver-were-on-the-wheel-during-an-accident/]: https://cellebrite.com/en/how-android-bluetooth-connections-can-determine-if-the-hands-of-a-driver-were-on-the-wheel-during-an-accident/ "https://cellebrite.com/en/how-android-bluetooth-connections-can-determine-if-the-hands-of-a-driver-were-on-the-wheel-during-an-accident/"

- [https://cellebrite.com/en/how-android-bluetooth-connections-can-determine-if-the-hands-of-a-driver-were-on-the-wheel-during-an-accident/]
