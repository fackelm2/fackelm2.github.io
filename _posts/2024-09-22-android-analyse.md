---
layout: post
title: Android Analyse
date: 2024-09-22 20:00:10
last_updated: 2024-09-22 20:00:10
description: Android Analyse Definitions
tags: android forensic
categories: android
featured: false
---

draft

Der Hauptunterschied der beschriebenen Vorgehensweise liegt im methodischen Fokus: 

Während die dynamische Analyse und Verhaltensanalyse breiter auf das Verhalten und die Funktionsweise der App abzielen, 
liegt bei der experimentellen Validierung der Schwerpunkt spezifisch darauf, herauszufinden, 
welche Artefakte durch welche Benutzeraktionen erzeugt werden.

Zusammenfassend ist die experimentelle Validierung eine spezifische Form der dynamischen Analyse, 
die gezielt dazu dient, die Herkunft und Bedeutung von forensischen Artefakten zu verstehen.


### Experimentelle Artefaktanalyse / Experimentelle Validierung (forensische Verifikation) durch Reproduktion 

In der digitalen Forensik beschreibt dies den Prozess, bei dem bekannte Handlungen in einer kontrollierten Umgebung 
auf Testgeräten durchgeführt werden, um die resultierenden Artefakte mit denen aus der untersuchten Sicherung 
zu vergleichen.
Dies ermöglicht es, das Verhalten der App zu analysieren und spezifische Artefakte bestimmten Benutzeraktionen 
zuzuordnen. Diese Methode stellt sicher, dass die Interpretation der Artefakte auf fundierten, überprüfbaren 
Beobachtungen beruht, was vor allem im Kontext von Gerichtsgutachten von großer Bedeutung ist.

### Dynamische Analyse

Diese bezieht sich allgemein auf die Untersuchung eines Systems, einer App oder einer Software während ihrer Ausführung, 
um ihr Verhalten und die entstehenden Artefakte in Echtzeit zu beobachten. 
In der Forensik bedeutet dies, die App direkt auf einem Testgerät oder in einer Sandbox-Umgebung zu starten und 
zu überwachen, welche Aktionen die Software durchführt und welche Daten dabei generiert werden. 
Die dynamische Analyse ist oft ein Bestandteil der experimentellen Validierung, insbesondere wenn die App 
aktiv genutzt wird, um Artefakte zu erzeugen.

### Verhaltensanalyse

Diese geht einen Schritt weiter und fokussiert sich auf die detaillierte Beobachtung und Dokumentation der Aktionen, 
die eine Software oder App während der Laufzeit durchführt. Dabei wird untersucht, wie die App auf Eingaben reagiert, 
welche Netzwerkverbindungen aufgebaut werden, wie sie Daten speichert und welche Spuren auf dem Gerät hinterlassen 
werden. Verhaltensanalyse kann somit auch Aspekte der Sicherheit und der Funktionalität umfassen, 
nicht nur forensische Artefakte.






