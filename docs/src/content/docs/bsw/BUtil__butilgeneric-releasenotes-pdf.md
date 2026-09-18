---
title: 'BUtil — BUtilGeneric_ReleaseNotes'
description: 'Converted PDF document BUtilGeneric_ReleaseNotes.pdf from module BUtil.'
sidebar:
  hidden: true
---

> **Source:** `BUtilGeneric_ReleaseNotes.pdf` (PDF, 119 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 3; title: -; author: -

## Converted content

### Page 1

Release Notes BUtilGeneric
Project BMW AUTOSAR Core 4 Rel. 3 and adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-12-14
Version 5.0.3
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
5.0.3 2017-12-14 BAC-6676, BAC-6573
5.0.2 2017-10-12 BAC-6382, BAC-6343
5.0.1 2017-09-14 BAC-6299
5.0.0 2017-06-29
ReleaseNotes_BUtilGeneric, Version 5.0.3, Software Platforms Page 1 of 3

### Page 2

1 Module Description
2 Revisions and Modiﬁcations
Revision 5.0.3 [Released]
Item Description
CR ID: BAC-6676
CR Headline: BUtil: Version cross check between generic and adapter part
missing
Description of Issues: Version check and version cross check between generic and
adapter part is missing.
Description of Changes: add missing version checks
Changed Files: include/BUtil/TimerTypes.h
include/BUtil/GenericNvMTypes.h
include/BUtil/GenericErrMemTypes.h
include/BUtil_Algorithm.h
include/BUtil/GenericUDSTypes.h
Compatibility:
Item Description
CR ID: BAC-6573
CR Headline: nrc wrongBlockSequenceCounter missing in GenericUDSTypes.h
Description of Issues: nrc wrongBlockSequenceCounter missing in GenericUDSTypes.h
Description of Changes: add missing
UDS_DIAG_E_WRONGBLOCKSEQUENCECOUNTER
Changed Files: include/BUtil/GenericUDSTypes.h
Compatibility:
Revision 5.0.2 [Released]
Item Description
CR ID: BAC-6382
CR Headline: Fix file headers
Description of Issues: fix file headers
Description of Changes: fix file headers
Changed Files: include/BUtil_Assert.h
include/BUtil_Version.h
include/BUtil_BitArray.h
Compatibility:
Item Description
CR ID: BAC-6343
CR Headline: Add missing Get64Bit Macros
Description of Issues: Add missing Get64Bit Macros (follow-up to BAC-6299)
ReleaseNotes_BUtilGeneric, Version 5.0.3, Software Platforms Page 2 of 3

### Page 3

Description of Changes: add 64 bit put and get macros
Changed Files: include/BUtil_ByteMask.h
Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6299
CR Headline: Add missing macros for 64 bit support
Description of Issues: 64 bit support is missing.
Description of Changes: Add 64 bit macros.
Changed Files: include/BUtil_ByteMask.h
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_BUtilGeneric, Version 5.0.3, Software Platforms Page 3 of 3
