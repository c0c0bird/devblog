---
layout: [post, post-xml]              # Pflichtfeld. Nicht ändern!
title:  "Geheimnisse in Azure" # Pflichtfeld. Bitte einen Titel für den Blog Post angeben.
date:   2024-01-26 15:00              # Pflichtfeld. Format "YYYY-MM-DD HH:MM". Muss für Veröffentlichung in der Vergangenheit liegen. (Für Preview egal)
modified_date: 2024-01-26 15:00       # Optional. Muss angegeben werden, wenn eine bestehende Datei geändert wird.
author_ids: [cjohn]            # Pflichtfeld. Es muss in der "authors.yml" einen Eintrag mit diesen Namen geben.
categories: [Architektur]                # Pflichtfeld. Maximal eine der angegebenen Kategorien verwenden.
tags: [Azure, Applications, Microsoft, Cloud] # Bitte auf Großschreibung achten.
---

In einem Microsoft-Umfeld muss ein Service sich vor einem anderen authentifizieren.
Was auf den ersten Blick eine alltägliche Aufgabe ist, erfordert im Detail einige Umwege.

# Das Umfeld

In einem Projekt sollte ein Hintergrunddienst sich an mehreren OPC-Servern ([Open Platform Communication](2023-09-08-open-platform-communication.md)) anmelden, die Zustände der Maschinen überwachen und auftretende Fehler an eine Message Queue schicken.
Einige OPC-Server forderten eine Anmeldung mit Name und Passwort, andere benötigten ein zuvor hinterlegtes Zertifikat.
Die Zugangsdaten sollten zentral verwaltet, also nicht lokal auf dem Anwendungsserver gespeichert werden.

In einem Azure-Umfeld gehören alle Passwörter in einen "Key Vault", das ist ein Azure-Service zum sicheren Speichern von Geheimnissen.
Wie sie von dort zu der Anwendung gelangen, die sie benötigt, kommt ganz darauf an in welchem Kontext diese läuft.

# Typische Szenarien

Moderne Anwendungen werden oft als Docker-Container ausgerollt, andere laufen direkt auf einer virtuellen Maschine.
Wenn die Anwendung direkt in Azure gehostet wird, liegt wieder ein anderer Fall vor.

## Docker

## On-Premise

## Azure

## Offline



# Fazit

...
