---
title: 'Darh — DarhGeneric_ReleaseNotes'
description: 'Converted PDF document DarhGeneric_ReleaseNotes.pdf from module Darh.'
sidebar:
  hidden: true
---

> **Source:** `DarhGeneric_ReleaseNotes.pdf` (PDF, 117 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 2; title: -; author: -

## Converted content

### Page 1

Release Notes DarhGeneric
Project BMW AUTOSAR Core 4 Rel. 3 and adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-12-14
Version 5.1.0
Status Release
Hotline +49 89 382 - 32233 (classic) / +49 89 382 - 22522 (adaptive)
Contact bac@bmw.de (classic) / abac@bmw.de (adaptive)
https://asc.bmw.com/jira/browse/BSUP (extern)
https://asc.bmwgroup.net/jira/browse/BSUP (intern)
Company
Bayerische
Motoren Werke
Aktiengesellschaft
Postal address
BMW AG
80788 München
Office address
Forschungs- und
Innovationszentrum
(FIZ)
Hufelandstr. 1
80937 München
Telephone
Switchboard
+49 89 382-0
Internet
www.bmwgroup.com
Revision History
Version Date Issues
5.1.0 2017-12-14 BAC-6651
5.0.1 2017-10-12 BAC-6245
5.0.0 2017-06-29
ReleaseNotes_DarhGeneric, Version 5.1.0, Software Platforms Page 1 of 2

### Page 2

1 Module Description
The main objective of the Darh functionality is to send errors that occurred locally in the ECU and are
reported to the Dem to a central master over the system bus. The idea is to collect errors of the individual
ECUs in the vehicle in one central place to allow later analysis of error correlations between the different
ECUs.
For this purpose, errors are sent to the master containing timestamp information. This allows deducing
the order in which errors occurred in the complete system and helps to find out the original reason of a
complex causal loop.
2 Revisions and Modiﬁcations
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6651
CR Headline: Darh: only 1 DTC shall be transmitted at a time
Description of Issues: Darh transmit one DTC each time.
Description of Changes: Due to an update on the LH and the BNE the Darh will transmit
only one DTC and timestamp each time.
Changed Files: src/Darh_QueueHandler.c
Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6245
CR Headline: Darh: Improve Requirements Traceability
Description of Issues: Fix reference to Lastenheft and add requirements from
IntegrationManual to RequirementsTable.
Description of Changes: Fixed LH reference and added requirements from
IntegrationManual to RequirementsTable.
Changed Files: doc/DarhGeneric_RequirementsTable.pdf
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_DarhGeneric, Version 5.1.0, Software Platforms Page 2 of 2
