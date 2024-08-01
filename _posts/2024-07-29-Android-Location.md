---
layout: post
title: Google Location Data
date: 2024-07-29 17:55:10
description: Google Location Data
tags: android google location
categories: android
featured: false
---

draft 

[export Location History]: https://android.stackexchange.com/questions/257663/how-can-i-export-my-location-history-now-that-this-data-is-only-stored-locally-o "https://android.stackexchange.com/questions/257663/how-can-i-export-my-location-history-now-that-this-data-is-only-stored-locally-o"
[export Location History]
(https://android.stackexchange.com/questions/257663/how-can-i-export-my-location-history-now-that-this-data-is-only-stored-locally-o)

Google Location Data

"How can I export my Location History now that this data is only stored locally on the phone?"

"Google has been migrating phones to only store Location History data locally on the phone. Once an account has been transitioned, you can no longer export the data using Google Takeout since it is no longer on Google servers."

"How can I export my Location History data after my account as been transitioned?"

"Go to the settings app, then 
Location->Location Services->Time Line->Export Timeline Data 
and pick a folder and filename to export to. 
Wait a little while and then go check the folder and a new JSON file with your complete location history should be there."

"Credit to vijaykes for finding this (I would have never found this new option on my own)..."

[Export Google Maps Timeline Data on Android]: https://www.reddit.com/r/GoogleMaps/comments/1chlsst/export_google_maps_timeline_data_on_android/la6n0k2/ "https://www.reddit.com/r/GoogleMaps/comments/1chlsst/export_google_maps_timeline_data_on_android/la6n0k2/"
[Export Google Maps Timeline Data on Android]
(https://www.reddit.com/r/GoogleMaps/comments/1chlsst/export_google_maps_timeline_data_on_android/la6n0k2)

On my Pixel 8 Pro, Android 14: Settings app, then Location->Location Services->Time Line->Export Timeline Data

I doubt it would exist as a regular json file. It would be in the form of some encrypted database dump. If you have access to another Android device and are confident in understanding Google's terminology, you can try the following. Set up a fresh device with the same Google ID, set up timeline backup correctly so as to not override the older one, download the backed up timeline in the new device, and export it from there. (I'm too scared of somehow corrupting/deleting timeline to try this.)
In storage settings, Google shows that Google Maps occupies some 7gb on my phone storage. Only Google knows what that huge data contains 😅

I have found that more recent data wasn't corrupted and was able to export a part of it. I didn't check how far I could go back before encountering corruption.
I also remembered I had a Google Takeout backup from earlier (before the switch) and the entire data for those periods is there. The JSON is formatted differently but the coordinates and timestamps are there. Each year is about 2mb.
