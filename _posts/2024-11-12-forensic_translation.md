---
layout: post
title: Forensic Translation Tools 
date: 2024-11-17 07:00:10
last_updated: 2024-11-17 07:00:10
description: Translation Tools
tags: forensic
categories: forensic
featured: false
---
draft

## Automatic Translation
[IPED Digital Forensic Tool]: https://github.com/sepinf-inc/IPED "IPED Digital Forensic Tool"
[IPED Digital Forensic Tool]
IPED is an open source software that can be used to process and analyze digital evidence, 
often seized at crime scenes by law enforcement or in a corporate investigation by private examiners.

New to IPED?
[IPED Starting Guide]: https://github.com/sepinf-inc/IPED/wiki/Beginner's-Start-Guide "IPED Starting Guide"
[IPED Starting Guide]

Main goals efficient data processing and stability
* Command line data processing for batch case creation 
* Multiplatform support, tested on Windows and Linux systems 
* Portable cases without installation, you can run them from removable drives 
* Integrated and intuitive analysis interface 
* High multithread performance and support for large cases: up to 400GB/h processing speed using modern hardware and 135 million items in a (multi) case as of 12/12/2019

Currently IPED uses the Sleuthkit Library only to decode disk images and file systems, 
so the same image formats are supported: 
* RAW/DD
* E01
* ISO9660
* AFF
* WHD
* VMDK
* EX01
* VHDX
* UDF(ISO)
* AD1 (AccessData) 
* UFDR (Cellebrite)

