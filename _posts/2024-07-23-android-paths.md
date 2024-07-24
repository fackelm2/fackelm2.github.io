---
layout: post
title: Android Forensic - Android Path Description (Entwurf)
date: 2024-07-23 19:35:13
description: Android Path Description and links to references
tags: android forensic
categories: android
featured: true
---

Entwurf 

<a href="https://github.com/RealityNet/Android-Forensics-References">
https://github.com/RealityNet/Android-Forensics-References</a>

for example:
````markdown
/log/batterystats
    Cellebrite CTF 2021 - Heisenberg's Android
    https://www.stark4n6.com/2021/10/cellebrite-ctf-2021-heisenbergs-android.html
    Part 1: Walk-Through of Answers to the 2021 CTF – Investigating Heisenberg’s Android Device
    https://cellebrite.com/en/part-1-walk-through-of-answers-to-the-2021-ctf-investigating-heisenbergs-android-device/
    Artefacts of Android device power off due to depleted battery
    https://instatronic.com/artefacts-of-android-device-power-off-due-to-depleted-battery
````

ALEAPP https://github.com/abrignoni/ALEAPP
Android Logs Events And Protobuf Parser

Autopsy Plugin
Android extraction and analysis framework with an integrated Autopsy Module. Dump easily user data from a device and generate powerful reports for Autopsy or external applications.
https://github.com/labcif/FAMA


Android Forensic Bash Script (extract data from Android Smartphone bash script)
<a href="https://github.com/RealityNet/android_triage">https://github.com/RealityNet/android_triage</a>

Excel Attack Vector (TODO)
https://github.com/RealityNet/attack-coverages

Teleparser (Telegram Parser) 2020
https://github.com/RealityNet/teleparser

Amdroid Forensic
https://blog.digital-forensics.it/
- Dissecting the Android WiFiConfigStore.xml for forensic analysis
-  A first look at Android 14 forensics
- Analysis of Android settings during a forensic investigation
- Has the user ever used the XYZ application? aka traces of application execution on mobile devices


https://github.com/orgs/nowsecure/repositories?q=mirror%3Afalse+fork%3Afalse+archived%3Afalse


SQLite Queries
https://github.com/kacos2000/Queries?tab=readme-ov-file

Google Drive
- Query Google Drive's snapshot.db found at the '\AppData\Local\Google\Drive\user@' folder . 
- Query Google Drive's cloud_graph.db found at the '\AppData\Local\Google\Drive\user@\cloud_graph' folder 

Android
- Android 7 Calllog.db (Call history)
- Android 7 Contacts2.db (Contacts)
- Android 9 Contacts2.db (Call history)
- Android logs.db (Samsung Calls/messages)

example Logs_db.sql:
````markdown
-- sec = (Samsung Electronics Corporation)
-- \data\com.sec.android.provider.logsproviders\logs.db

Select 
	logs._id as 'id',
	logs.geocoded_location||' ('||logs.countryiso||')' as 'Location',
	logs.name,
	logs.number,
	case logs.numbertype 
		when 1 then 'Home'
		when 2 then 'Mobile'
		when 3 then 'Work'
		when 4 then 'Fax_Work'
		when 5 then 'Fax_Home'
		when 6 then 'Pager'
		when 7 then 'Other'
		when 8 then 'Callback'
		when 9 then 'Car'
		when 10 then 'Company_Main'
		when 11 then 'ISDN'
		when 12 then 'Main'
		when 13 then 'Other_Fax'
		when 14 then 'Radio'
		when 15 then 'Telex'
		when 16 then 'TTY_TDD'
		when 17 then 'Work_Mobile'
		when 18 then 'Work_Pager'
		when 19 then 'Assistant'
		when 20 then 'MMS'
		else logs.numbertype
		end as 'numbertype',
	case logs.presentation
		when 1 then 'allowed' --Number is allowed to display for caller id
		when 2 then 'restricted' --Number is blocked by user
		when 3 then 'unknown'  --Number is not specified or unknown by network
		when 4 then 'pay phone' --Number is a pay phone
		else logs.presentation
		end as 'CallerID',	
	datetime(logs.date/1000, 'unixepoch') as 'lDate',
	case 
		when logs.duration != 0
		then Time(logs.duration, 'unixepoch') 
		end as 'Duration',--The duration of the call in seconds
	case logs.type
		when 1 then 'incoming' --incoming calls
		when 2 then 'outgoing' --outgoing calls
		when 3 then 'missed' --missed calls
		when 4 then 'voicemail' --Call log type for voicemails
		when 5 then 'rejected' --rejected by direct user action
		when 6 then 'blocked' --calls blocked automatically
		when 7 then 'answered externally' --call which was answered on another device
		else logs.type
	end as 'type',	
	case 
		when logs.logtype in (100)
		then 'Call ('||logs.logtype||')'
		when logs.logtype in (300)
		then 'SMS ('||logs.logtype||')'
		when logs.logtype in (400)
		then 'Email ('||logs.logtype||')'
		else 'Other ('||logs.logtype||')'
		end as 'logtype',
	logs.messageid,		
	case logs.is_read
		when 0 then 'No'
		when 1 then 'Yes'
		end as 'IsRead',
	logs.m_subject as 'MessageSubject',
	logs.m_content as 'MessageContent',
	case logs."new"
		when 1 then 'Yes'
		end as 'New',
	logs.contactid,
	logs.raw_contact_id,
	logs.lookup_uri,
	logs.photo_id,
	logs.account_name||' ('||logs.account_id||')' as 'Account'
from logs
order by lDate desc
````

calllog_db.sql
````markdown
-- references: 
-- https://developer.android.com/reference/android/provider/CallLog.Calls.html
-- https://developer.android.com/reference/android/provider/ContactsContract.CommonDataKinds.Phone
--
--
-- Costas Katsavounidis © 06/2019 

SELECT
calls._id,
number, --The phone number as the user entered it.
case presentation
	when 1 then 'allowed' --Number is allowed to display for caller id
	when 2 then 'restricted' --Number is blocked by user
	when 3 then 'unknown'  --Number is not specified or unknown by network
	when 4 then 'pay phone' --Number is a pay phone
	else presentation
	end as 'CallerID',
case calls.new -- Whether or not the call has been acknowledged
	when 1 then 'yes'
	else ''
	end as 'New',
case type
	when 1 then 'incoming' --incoming calls
	when 2 then 'outgoing' --outgoing calls
	when 3 then 'missed' --missed calls
	when 4 then 'voicemail' --Call log type for voicemails
	when 5 then 'rejected' --rejected by direct user action
	when 6 then 'blocked' --calls blocked automatically
	when 7 then 'answered externally' --call which was answered on another device
	else type
	end as 'type',
-- ISREAD >> Unlike the NEW field, which requires the user to have acknowledged the existence of the entry, 
-- this implies the user has interacted with the entry. 
case is_read -- Whether this item has been read or otherwise consumed by the user. 
	when 1 then 'yes'
	else ''
	end as 'is read',
case features
	when 0 then 'None'
	when 1 then 'Call had Video'
	when 2 then 'Call was pulled externally'
	when 4 then 'HD Call'
	when 8 then 'Call was WIFI call'
	when 32 then 'Call was on RTT at some point'
	else features
	end as 'features',
operator||' ('||countryiso||')' as 'Operator',
geocoded_location, --The string represents a city, state, or country associated with the number associated with this call 
matched_number,
case numbertype --cached number type (Home, Work, etc) associated with the phone number
	when 1 then 'Home'
	when 2 then 'Mobile'
	when 3 then 'Work'
	when 4 then 'Fax_Work'
	when 5 then 'Fax_Home'
	when 6 then 'Pager'
	when 7 then 'Other'
	when 8 then 'Callback'
	when 9 then 'Car'
	when 10 then 'Company_Main'
	when 11 then 'ISDN'
	when 12 then 'Main'
	when 13 then 'Other_Fax'
	when 14 then 'Radio'
	when 15 then 'Telex'
	when 16 then 'TTY_TDD'
	when 17 then 'Work_Mobile'
	when 18 then 'Work_Pager'
	when 19 then 'Assistant'
	when 20 then 'MMS'
	else numbertype
	end as 'numbertype',
formatted_number,
post_dial_digits, --post-dial portion of a dialed number
name,
time(duration,'unixepoch') as 'duration', --The duration of the call in seconds 
datetime(date/1000, 'unixepoch','localtime') as 'call_date', --The date the call occured, in milliseconds since the epoch 
datetime(last_modified/1000, 'unixepoch','localtime') as 'lastmodified',--The date the row is last inserted, updated, or marked as deleted, in milliseconds since the epoch
photo_id,
photo_uri,
via_number, -- the via number indicates which of the numbers associated with the SIM was called
phone_account_address, --The identifier for the account used to place or receive the call
subscription_id as 'sid', --The identifier for the account used to place or receive the call,
case phone_account_hidden 
	when 0 then 'No'
	when 1 then 'Yes'
	end as 'hidden',
subscription_component_name as 'component',
calls._data as 'data',
case has_content
	when 1 then 'Yes'
	end as 'has content',
data_usage,
source_package,	
transcription, --only be populated for call log entries of type VOICEMAIL_TYPE that have valid transcriptions
mime_type,
case dirty
	when 1 then 'yes'
	end as 'dirty',
case deleted 
	when 0 then 'no' 
	when 1 then 'yes' 
	end as 'deleted'
from calls
order by calls._id desc

````

ADB Chat
ADB Chat is a LangChain Agent-based chat application that allows the user to execute Android Debug Bridge commands 
using a natural language chat interface.
https://github.com/jgordley/chat-adb



Messegner Signal 
https://github.com/AvillaDaniel/Signal-Forensics


apkqf (APK Quick Forensics) is an Android application to simplify the acquisition of relevant forensic data from 
Android devices. It is inspired on androidqf.
https://github.com/penserbjorne/apkqf


AndroidForensics

LiME, Volatility and custom Python wrapper script for android forensic analysis
Description
This project contains files and custom scripts to extract processes from Android devices using LiME and Volatility. 
The main file androidforensics.py can be run using the command python androidforensics.py
https://github.com/devopscrazy/AndroidForensics

Mobile Investigation Tools 
https://github.com/salvinmirza/Mobile-App-forensic-tools-analysis

VALFE08 ( Vishwa's Android Log File Extractor )
https://github.com/code-reaper08/VALFE08

OpenMF is an open source forensic tool for Android smartphones that helps digital forensic investigators 
throughout the life cycle of digital forensic investigation.
https://github.com/c2siorg/OpenMF


ADB: Dump Memory 
https://github.com/aishee/andump


App Gmail
gmail-android-forensic-analysis
https://github.com/paologrossetti/gmail-android-forensic-analysis


https://github.com/paologrossetti/Cryptot00l
This project aims to learn notions about the most important encryption algorithms. Thanks to Python library pycryptodome, simple examples involving the following algorithm have been defined:
- AES
- RSA 
- Salsa20 
- Chacha20


SecCheats is a collection of cheat sheets for various topics in security.
https://github.com/paologrossetti/SecCheats?tab=readme-ov-file



Databases Diagrams related to the Running applications of the paper "Digital Footprints on the Run: 
A Forensic Examination of Android Running Workout Applications" 
https://github.com/labcif/Running-Databases
- Nike Run
- Pumatrac
- Runkeeper



