---
title: 'BUtil — BUtilClassic_ReleaseNotes'
description: 'Converted PDF document BUtilClassic_ReleaseNotes.pdf from module BUtil.'
sidebar:
  hidden: true
---

> **Source:** `BUtilClassic_ReleaseNotes.pdf` (PDF, 118 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 3; title: -; author: -

## Converted content

### Page 1

Release Notes BUtilClassic
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.1.1
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
5.1.1 2017-12-14 BAC-6676
5.1.0 2017-09-14 BAC-6290, BAC-6288
5.0.1 2017-08-10 BAC-6174
5.0.0 2017-06-29
ReleaseNotes_BUtilClassic, Version 5.1.1, Software Platforms Page 1 of 3

### Page 2

1 Module Description
2 Revisions and Modiﬁcations
Revision 5.1.1 [Released]
Item Description
CR ID: BAC-6676
CR Headline: BUtil: Version cross check between generic and adapter part
missing
Description of Issues: Version check and version cross check between generic and
adapter part is missing.
Description of Changes: add missing version checks
Changed Files: include/BUtil_UDSAdapterHelper.h
include/BUtilClassic_Version.h
src/BUtil_UDSAdapterHelper.c
Compatibility:
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6290
CR Headline: fix compiler warnings
Description of Issues: fix compiler warnings
Description of Changes: fix compiler warnings
Changed Files: src/BUtil_UDSAdapterHelper.c
Compatibility:
Item Description
CR ID: BAC-6288
CR Headline: add UDS prefix to generated ReadData and WriteData functions
Description of Issues: add UDS prefix to generated ReadData and WriteData functions
Description of Changes: add UDS prefix to generated ReadData and WriteData functions
Changed Files: generate/pageinclude/BUtil_UDSAdapterHelper.pgen
Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6174
CR Headline: #include "Dcm_Types.h" conflicts with Rte*.h
Description of Issues: #include "Dcm_Types.h" conflicts with Rte*.h
Description of Changes: include Dcm_Typs.h only in case no Rte header is included
Changed Files: include/BUtil_UDSAdapterHelper.h
Compatibility:
ReleaseNotes_BUtilClassic, Version 5.1.1, Software Platforms Page 2 of 3

### Page 3

Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_BUtilClassic, Version 5.1.1, Software Platforms Page 3 of 3
