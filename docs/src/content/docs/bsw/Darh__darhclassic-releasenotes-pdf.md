---
title: 'Darh — DarhClassic_ReleaseNotes'
description: 'Converted PDF document DarhClassic_ReleaseNotes.pdf from module Darh.'
sidebar:
  hidden: true
---

> **Source:** `DarhClassic_ReleaseNotes.pdf` (PDF, 119 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 3; title: -; author: -

## Converted content

### Page 1

Release Notes DarhClassic
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.1.0
Status Release
Hotline +49 89 382 - 32233
Contact bac@bmw.de
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
5.0.2 2017-11-09 BAC-6506
5.0.1 2017-10-12 BAC-6345, BAC-6196
5.0.0 2017-06-29
ReleaseNotes_DarhClassic, Version 5.1.0, Software Platforms Page 1 of 3

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
Changed Files: doc/DarhClassic_IntegrationManual.pdf
src/Darh_ApplAdapter.c
generate/meta/Darh_ext_interfaces.arxml.pgen
generate/meta/Darh_internal.arxml.pgen
Compatibility:
Revision 5.0.2 [Released]
Item Description
CR ID: BAC-6506
CR Headline: Adapt pgen templates to PAGe v1.1.0
Description of Issues: Adapt pgen files to PAGe v1.1.0.
Description of Changes: Adapted pgen files to PAGe v1.1.0.
Changed Files: generate/meta/Darh_ext_interfaces.arxml.pgen
generate/include/DarhClassic_Cfg.h.pgen
generate/meta/Darh_internal.arxml.pgen
Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6345
CR Headline: Darh: Dem_EventIdType has to be uint16
ReleaseNotes_DarhClassic, Version 5.1.0, Software Platforms Page 2 of 3

### Page 3

Description of Issues: Dem_EventIdType is defined in AUTOSAR as uint16 and not
uint32.
Description of Changes: Dem_EventIdType has been changed to uint16.
Changed Files: generate/meta/Darh_ext_interfaces.arxml.pgen
src/Darh_ApplAdapter.c
Compatibility:
Item Description
CR ID: BAC-6196
CR Headline: Darh: Implementation of Darh_SetRoeSuspendedHandler()
missing
Description of Issues: The runnable SetRoeSuspended was not implemented in code.
Description of Changes: The runnable SetRoeSuspended with the Symbol
Darh_SetRoeSuspendedHandler has been implemented.
Changed Files: src/Darh_ApplAdapter.c
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_DarhClassic, Version 5.1.0, Software Platforms Page 3 of 3
