---
title: 'Omc — OmcGeneric_ReleaseNotes'
description: 'Converted PDF document OmcGeneric_ReleaseNotes.pdf from module Omc.'
sidebar:
  hidden: true
---

> **Source:** `OmcGeneric_ReleaseNotes.pdf` (PDF, 120 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 3; title: -; author: -

## Converted content

### Page 1

Release Notes OmcGeneric
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
5.1.0 2017-12-14 BAC-6566, BAC-6565, BAC-6717
5.0.2 2017-10-12 BAC-6242
5.0.1 2017-08-10 BAC-6169
5.0.0 2017-06-29
ReleaseNotes_OmcGeneric, Version 5.1.0, Software Platforms Page 1 of 3

### Page 2

1 Module Description
The main objective of the OMC functionality is to maintain the current Operation Mode of an ECU.
2 Revisions and Modiﬁcations
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6566
CR Headline: Omc: Adapt code to be MISRA and improve code coverage
Description of Issues: Improve code to be MISRA conform. Improve unit test code
coverage.
Description of Changes: Improve code to be MISRA conform. Improve unit test code
coverage.
Changed Files: src/Omc.c
include/Omc.h
include/Omc_ApplAdapter.h
cfgdesc/Omc_paramdef.arxml
src/Omc_Data.c
Compatibility:
Item Description
CR ID: BAC-6565
CR Headline: Provide callback mechanism to establish intrinsic safety.
Description of Issues: Provide a callback mechanism for StdDiag and the Application to
accept a mode change, and also to be informed if the mode
change is not completed.
Description of Changes: Improve the callback mechanismus to StdDiag and the Application.
Providing an extra interface to allow or disallow a mode change
using a callback. Also provide a callback to confirm a rollback if a
mode change is not completed.
Changed Files: include/Omc_StdDiagAdapter.h
include/Omc.h
include/Omc_ApplAdapter.h
src/Omc.c
Compatibility:
Item Description
CR ID: BAC-6717
CR Headline: Improve requirement tracing
Description of Issues: Improve requirement tracing table.
Description of Changes: Improve requirement tracing table.
Changed Files: include/Omc_Data.h
ReleaseNotes_OmcGeneric, Version 5.1.0, Software Platforms Page 2 of 3

### Page 3

Compatibility:
Revision 5.0.2 [Released]
Item Description
CR ID: BAC-6242
CR Headline: Omc: wrong NegReponseCode for $31 01 10 03
Description of Issues: Requesting an invalid extended mode in normal mode ($31 01 10
03) shall return Request Out Of Range and not Conditions not
Correct.
Description of Changes: The order of following checks: * check if a extended mode change
is requested in normal mode * check if the range of the requested
extended mode is valid has been changed. First the range is
changed and if invalid Request out of Range is returned to the
tester.
Changed Files: src/Omc.c
Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6169
CR Headline: Omc: Compiler error due to comma at end of enum list
Description of Issues: Comma at end of enumeration list causes compiler error.
Description of Changes: Removed comma at end of enumeration list.
Changed Files: src/Omc.c
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_OmcGeneric, Version 5.1.0, Software Platforms Page 3 of 3
