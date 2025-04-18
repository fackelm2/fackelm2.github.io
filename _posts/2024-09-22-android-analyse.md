---
layout: post
title: Android Analyse
date: 2024-09-22 20:00:10
last_updated: 2024-09-22 20:00:10
description: Android Analyse Definitions
tags: android forensics
categories: android
featured: false
---

draft - english - Translated with DeepL.com (free version)

The main difference between the two approaches lies in the methodological focus. While dynamic analysis and
behavioral analysis take a broader approach that comprehensively examines the behavior and functioning of the app,
experimental validation focuses specifically on identifying the artifacts generated by user actions.

In summary, experimental validation can be described as a specific form of dynamic analysis that aims to understand
the origin and meaning of forensic artifacts.

### Experimental artifact analysis / Experimental validation (forensic verification) through reproduction

In digital forensics, this describes the process by which known actions are performed in a controlled environment
on test devices in order to compare the resulting artifacts with those from the examined backup.
compared.
This makes it possible to analyze the behavior of the app and assign specific artifacts to specific user actions.
to specific user actions. This method ensures that the interpretation of the artifacts is based on well-founded, verifiable
verifiable observations, which is particularly important in the context of court reports.

Translated with DeepL.com (free version)

### Dynamic analysis

Dynamic analysis is a research method that involves observing a system, an application or software during its execution.
or software during its execution.
The aim is to record the behavior and analyze the resulting artefacts in real time.
In forensics, the app is launched directly on a test device or in a sandbox environment,
whereupon the actions performed and data generated are monitored.
In this context, dynamic analysis is an important part of experimental validation,
especially when the app is actively used to generate artifacts.

### Behavioral analysis

Behavioral analysis goes one step further and focuses on the detailed observation and documentation of the actions
of the actions that a software or app performs during runtime.
It examines how the app reacts to inputs, which network connections are established,
how it stores data and what traces are left behind on the device.
Behavioral analysis can therefore also include aspects of security and functionality,
not just forensic artifacts.

---

draft - german

Der wesentliche Unterschied zwischen den beiden Vorgehensweisen liegt im methodischen Fokus. Während die dynamische
Analyse und Verhaltensanalyse einen breiteren Ansatz verfolgen, der das Verhalten und die Funktionsweise der App
umfassend untersucht, konzentriert sich die experimentelle Validierung spezifisch darauf, die durch Benutzeraktionen
erzeugten Artefakte zu identifizieren.

Zusammenfassend kann die experimentelle Validierung als eine spezifische Form der dynamischen Analyse bezeichnet werden,
die darauf abzielt, die Herkunft und Bedeutung von forensischen Artefakten zu verstehen.

### Experimentelle Validierung (forensische Verifikation durch Reproduktion)

Die experimentelle Validierung führt eine bekannte Handlung in einer kontrollierten Umgebung auf Testgeräten durch,
um die resultierenden Artefakte mit denen aus der untersuchten Sicherung zu vergleichen.
Dies ermöglicht es, das Verhalten der App zu analysieren und spezifische Artefakte
bestimmten Benutzeraktionen zuzuordnen.
Diese Methode stellt sicher, dass die Interpretation der Artefakte auf fundierten, überprüfbaren Beobachtungen beruht,
was vor allem im Kontext von Gerichtsgutachten von großer Bedeutung ist.

### Dynamische Analyse

Die dynamische Analyse bezeichnet eine Untersuchungsmethode, welche die Beobachtung eines Systems, einer Applikation
oder einer Software während ihrer Ausführung zum Gegenstand hat.
Ziel ist die Erfassung des Verhaltens sowie die Analyse der entstehenden Artefakte in Echtzeit.
In der Forensik erfolgt der Start der App direkt auf einem Testgerät oder in einer Sandbox-Umgebung,
woraufhin eine Überwachung der durchgeführten Aktionen und generierten Daten stattfindet.
Die dynamische Analyse stellt in diesem Kontext einen wichtigen Bestandteil der experimentellen Validierung dar,
insbesondere bei einer aktiven Nutzung der App zur Artefakt-Erzeugung.

### Verhaltensanalyse

Die Verhaltensanalyse geht einen Schritt weiter und fokussiert sich auf die detaillierte Beobachtung und Dokumentation
der Aktionen, die eine Software oder App während der Laufzeit durchführt.
Dabei wird untersucht, wie die App auf Eingaben reagiert, welche Netzwerkverbindungen aufgebaut werden,
wie sie Daten speichert und welche Spuren auf dem Gerät hinterlassen werden.
Die Verhaltensanalyse kann somit auch Aspekte der Sicherheit und der Funktionalität umfassen,
nicht nur forensische Artefakte.
