---
layout: post
title: Analyse Android Samsung
date: 2024-11-10 07:00:10
last_updated: 2024-11-10 07:00:10
description: Analyse Android Samsung Device
tags: android forensics samsung
categories: android
featured: false
---

draft

## Android Forensics - Samsung

[Analyse Samsuing Rubin / Pass]: https://cellebrite.com/en/physical-analyzer-7-58-updated-android-artifacts-and-support/ "Samsung Rubin / Pass"

[Analyse Samsuing Rubin / Pass]

## Samsung Rubin

- unique Samsung source file
- contains records of
  - visited locations
  - device events ("on" or "off")
  - device connectivity

/data/data/com.samsung.android.rubin.app/databases/inferenceengine_logging.db/inferenceengine_logging.db.decrypted

## Samsung Pass

The Samsung Password Manager

- store passwords for applications
- often unlocked with the biometric unlock set on the device
