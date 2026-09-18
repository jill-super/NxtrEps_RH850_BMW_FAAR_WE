---
title: 'BmwBacSuprt — releasenotes'
description: 'Converted PDF document releasenotes.pdf from module BmwBacSuprt.'
sidebar:
  hidden: true
---

> **Source:** `releasenotes.pdf` (PDF, 54 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 7; title: Release-Notes; author: Antony Rolf, (Rolf.Antony@partner.bmw.de)

## Converted content

### Page 1

Release Notes 
Version 3.11.0 vom 07.11.2017 
 Neue Signatur- (ecdsa, rsassa-pss) und Hashfunktionen (SHA3) für SP2021. 
 Unterstützung von Multischlüsseldateien (*.keys) für SP2021. 
 Kommando SIGN mit neuem Parameter keyname zur Auswahl eines 
Schlüssels aus einer Multischlüsseldatei. 
 
Version 3.10.0 vom 31.03.2017 
 Neuer Parameter POINTER für das Kommando 
CHECKSUM_TABLE_BLOCK. 
 
Version 3.9.0 vom 25.07.2014 
 Erweiterung SWE-Verschlüsselung. 
 Neues Kommando SET_SESSION_KEY_ADDRESS_STORAGE. 
 
Version 3.8.0 vom 05.06.2013 
 Die verschiedenen SWE-Generator Modi können jetzt auch über Menüpunkt 
Ansicht ausgewählt werden. 
 Menüpunkt Konfiguration ersetzt durch entsprechende Buttons im Modus 
Config-Editor. 
 Bugfix: Hexadezimale Schlüssellängen in der Konfigurationsdatei wurden 
nicht mehr berücksichtigt. 
 
Version 3.7.0 vom 09.04.2013 
 Englische Onlinehilfe überarbeitet. 
 Neues Kommando CHECKSUM_TABLE_TO_EDCH_TABLE. 
 
Version 3.6.0 vom 05.11.2012 
 TD_Pro441::8091 - Hash-Signatur scheitert wegen EA-Header-Comments: 
Fehlende Zeilenchecksumme ergänzt. 
 Korrekturen am Compress Modus. 
 Performance und Speicherbedarf des Viewers bei der Anzeige von BSW 
Dateien optimiert. 
 Bugfix: Wenn BSW-Datei existiert und schreibgeschützt ist (z.B. VCS), gab es 
eine Exception. 
 
Version 3.5.2 vom 18.10.2012 
 TD_Pro441::8102 - Modul "Hash-Sign" :: SIGNATURE_HASH_MODE: Invalid 
hash mode (bei sha1). 
 
Version 3.5.1 vom 09.10.2012

### Page 2

 TD_Pro441::8024 - SWE-Generator bleibt im Batchmode hängen, wenn kein 
Hashfile vorhanden ist. 
 Korrekturen am Header-Editor. 
 Korrekturen am Compress Batchmodus. 
 
Version 3.5.0 vom 24.08.2012 
 TD_Pro441::CR1422 - Umstellung auf Visual Studio 2010 -> Leicht 
veränderte GUI. 
 TD_Pro441::CR1308 - Kommando CREATE_DESCRIPTION_TABLE 
variabel. 
- Neues BN2020 Kommando SET_SIGNATURE_ADDRESS <address> 
(optional). 
- Neues BN2020 Kommando SET_DIF_ADDRESS <address> (optional). 
 TD_Pro441::KÄ1380 - Signatur-Status im Hash-Editor automatisch auf 
"signed" setzen wenn Signatur generiert wurde. 
 TD_Pro441::KÄ1379 - Buttons "Next Block" und "Prev Block" im Modul 
Viewer tauschen. 
 Diverse Optimierungen am SWE-Viewer. 
 Bugfix: CARB Zeilenchecksumme fehlte im MSR-File bei Hash-Sign und 
Signierung. 
 
Version 3.4.0 vom 29.06.2012 
 TD_Pro441::KÄ1291 - Mehrere Checksummentabellen pro 
Konfigurationsdatei erlauben. 
Für interne Checksumme und CARB-Checksumme können verschiedene 
Tabellen aufgebaut werden. 
 TD_Pro441::7329 - Parameter wird abgeschnitten 
Es wurde bemängelt, dass Parameter (Dateinamen), die im Modul 
"Generator" über den "Add..."-Button hinzugefügt werden, nach 63 Zeichen 
abgeschnitten werden -> Fehlermeldung anzeigen wenn Dateiname 
abgeschnitten wurde. 
 TD_Pro441::CR1304 - Neue Prozessklasse SWFK integriert. 
 Version der XML Schemadatei der Hashliste auf V02.03.00 gesetzt 
 Bugfix: Command CREATE_DESCRIPTION_TABLE: Adresse in 
Fehlermeldung nicht korrekt. 
 
Version 3.3.0 vom 30.01.2012 
 BN2020 Signatur- / Hashlibrary SigLibNT durch Open Source Bibliothek 
PolarSSL V1.0.0 ersetzt. 
 BN2020 Hashwertberechnung (MD5) um folgende Algorithmen erweitert: 
SHA1, SHA256, SHA384, SHA512. 
 
Version 3.2.0 vom 23.09.2011 
 TD_Pro441::QC5156: Kompri

### Page 3

PAF Kompression komplett überarbeitet um den hohen Speicherbedarf 
zusätzlich zum NRV-Kompressor zu reduzieren. 
 TD_Pro441::QC5763: Show Output-File im Modul Compress/Convert 
funktioniert nicht. 
 TD_Pro441::QC6248: Falsche Interpretation der Referenzenanzahl in 
"CREATE_HEADER_COMMENTS_FROM_DIF EA". 
 TD_Pro441::QC6120: Reproduzierbarer Absturz des SWE-Generators mit 
Config-File für drei SWEn. 
 TD_Pro441::QC6098: Prozessklasse HWAP wird beim Kommando 
"CREATE_HEADER_COMMENTS_FROM_DIF EA" als UNKNOWN 
ausgegeben. 
 TD_Pro441::QC6103: Bug in READ_DIF_FROM_MEMORY wenn Länge=0. 
 TD_Pro441::QC6854: Batchmodus BN2000: Enthält Configfile Path die 
Zeichenkette "..-C.." dann wird diese als Option Compress (-C) interpretiert. 
 Bugfix VDLE: Letzter Eintrag der Ladetabelle am Ende des PBF-Files fehlte 
(kein Problem wenn AIF vorhanden ist). 
 
Version 3.1.1 (inkl. PafMaker) vom 06.04.2011 
 Neues Feature: Bei der Kompression / Konvertierung von BN2020 MSR-
Dateien ins BIN-Format, werden die BIN Dateien gemäß Muster 
gwtb_XXXXXXXX.bin.XXX_XXX_XXX benamt. Dies ist unabhängig vom 
Namen der MSR-Datei. Das Gleiche gilt für die erzeugte XML-Datei. Die 
Namen der Dateien in den BSW Archiven bleiben bei der Konvertierung ins 
BSW-Format unverändert und entsprechen dem Dateinamen der Input MSR-
Datei. 
 
Version 3.1.0 (inkl. PafMaker) vom 21.03.2011 
 Neues Feature: Neue Prozessklasse GWTB (0x04) integriert. 
 Neues Feature: BN2020 Kompression erweitert um binären Output statt 
verpackt in BSW (Dialog und Batchmodus). 
 Bugfix: Problem mit Schreiben der Hashsignatur ans Ende der *.msr Datei 
behoben. 
 Bugfix: Fehler mit Adressen > 0x80000000 behoben. 
 
Version 3.0.1 (inkl. PafMaker) vom 04.11.2010 
 Bugfix: Probleme mit BN2020 Adresse 0xFFFFFFFF bei Kommandos 
BLOCK,

### Page 4

 Achtung: BN2000 Hash-Signierung unterstützt keine SGs mit 
Multisignaturen! 
 
Version 2.11.0 vom 24.04.2009 
 Neues Feature: Mit dem optionalen Parameter "Kompression erzwingen", 
kann die Kompression erzwungen werden, auch wenn die vorgegebenen 
Kompressionsrate nicht erreicht werden konnte. Siehe Kompression und 
Bedienung BatchModus Kompression/Konvertierung. 
 
Version 2.10.0 vom 04.12.2008 
 Neues Feature: Beim Einlesen aus Intel-, Srec- und Paf-Files wird die 
Zeilenchecksumme überprüft. 
 Neues Feature: Kommando READ_TYPENUMBER_FROM_MEMORY liest 
die Typenumber aus einem zuvor eingelesenem Datenbereich aus und 
schreibt diese in den Header. 
 Neue Prozessklassen NAVD und ENTD weren unterstützt. 
 
Version 2.9.2 vom 25.07.2008 
 Bugfix für die Berechnung von CHECKSUM_CARB_FROM_DATA 
 
Version 2.9.1 vom 12.06.2008 
 Achtung: Für die FLUP- und BLUP-SWEn ändert das Kommando 
CREATE_DESCRIPTION_TABLE die Prozessklassen Identifier. 
 
Version 2.9.0 vom 07.04.2008 
 Neuer Parameter type im Kommando CHECKSUM_TABLE_TO_MEMORY 
 Neuer Parameter type im Kommando CHECKSUM_TABLE_TO_CARB 
 Bugfix Fehlermeldung bei der Angabe von readonly Hash-Dateien oder 
absolutem Pfad im Kommando CREATE_HASH_FILE 
 Für den Parameter type im Kommando SET_TARGET_BOOTLOADER ist 
zusätzlich die Option "flsl" möglich. 
 Signaturinfo im Block-Kommentar bei der Generierung von SWE'n entfernt. 
 
Version 2.8.0 vom 29.02.2008 
 Kommando CREATE_HASH_FILE um Option "SWE_NAME" erweitert 
 Batch-Betrieb für den Hash-Merger 
 Unterstützung neuer Prozessklassen SWUP, BLUP und FLUP 
 Batch-Betrieb für das Paf2Swe-Modul 
 Neues Menü Extras für Tools 
 Kompressions und Signaturinformationen in die Blocktitel bei der Darstellung 
von bsw-Dateien übernommen 
 Sicherung der Optionen im Kompr

### Page 5

 Das Kommando CHECKSUM_CARB_FROM_HASH erhält die neuen 
Parameter mode, format und address 
 
Version 2.7.1 vom 28.09.2007 
 Bugfix in der Validierung von SGBM-IDs 
 Bugfix zur Unterstüztung mehrerer Parameter im Batch-Mode 
 Bugfix für die Unterstützung des Batch-Parameters "-gui off" 
 
Version 2.7.0 vom 14.09.2007 
 Neue Tool-Funktion Hash Editor als Ersatz für das Hash-Tool. 
 Anpassung von Log-Meldungen in der Kompression. 
 
Version 2.6.1 vom 27.07.2007 
 Neues XML-Schema für die Hash-Signierung. 
 Entfernung des Zeitstempels in binären Softwareeinheiten. 
 
Version 2.6.0 vom 13.07.2007 
 Der Viewer kann auch BSW-Dateien anzeigen. 
 Bei der Konvertierung in BSW-Dateien wird für nicht komprimierte Blöcke 
(Unterschreitung der Effizienzgrenze, Komprimierung nicht angewählt) der 
Kompressionsalgorithmus auf "UNKNOWN" gesetzt 
 Unterstützung eines neuen Schemas für die Hash-Signierung. 
 
Version 2.5.0 vom 22.05.2007 
 Neues Kommando READ_DIF_FROM_MEMORY für das Einlesen von des 
Development Info Fields aus einem Datenblock 
 Geände
