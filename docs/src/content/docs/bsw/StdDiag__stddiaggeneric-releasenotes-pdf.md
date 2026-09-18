---
title: 'StdDiag — StdDiagGeneric_ReleaseNotes'
description: 'Converted PDF document StdDiagGeneric_ReleaseNotes.pdf from module StdDiag.'
sidebar:
  hidden: true
---

> **Source:** `StdDiagGeneric_ReleaseNotes.pdf` (PDF, 124 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 5; title: -; author: -

## Converted content

### Page 1

Release Notes StdDiagGeneric
Project BMW AUTOSAR Core 4 Rel. 3 and adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-12-14
Version 5.3.0
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
5.3.0 2017-12-14 BAC-6628, BAC-6248
5.2.0 2017-11-09 BAC-6469, BAC-6249
5.1.1 2017-10-12 BAC-5176, BAC-6230, BAC-6241, BAC-6433
5.1.0 2017-08-10 BAC-6148, BAC-6134
5.0.0 2017-06-29
ReleaseNotes_StdDiagGeneric, Version 5.3.0, Software Platforms Page 1 of 5

### Page 2

1 Module Description
The main functionality of the StdDiag module is to handle the active session states ("subsessions") of the
default diagnostic session and the extended diagnostic session. It ensures that the programming
preparation process (i.e. the transition from the diagnostic default session via the extended diagnostic
session to the programming session) is only successful, if the diagnostic requests are received in the
correct sequence and all necessary preconditions are fulfilled. It also checks whether diagnostic requests
shall be rejected or allowed in the different session states.
The StdDiag module also provides diagnostic service handlers for - clearing the secondary error memory
- reading the active session state - reading the programming preconditions - reading the SGBD-Index -
diagnostic communication loopback functionality - handling Diagnostic Log and Trace settings - handling
IDRL basic functionality
2 Revisions and Modiﬁcations
Revision 5.3.0 [Released]
Item Description
CR ID: BAC-6628
CR Headline: Adapt generated code comment to new PAGe generator
Description of Issues: Name of IDRL Client in comment of StdDiag_DIDArray is not
generated correctly with latest PAGe version.
Description of Changes: Adapt generation of comment to latest PAGe version.
Changed Files: generate/src/StdDiag_Cfg.c.pgen
Compatibility:
Item Description
CR ID: BAC-6248
CR Headline: Provide callback mechanism to establish intrinsic safety
Description of Issues: Provide an asynchronous callback mechanism to establish intrinsic
safety for long running user callouts.
Description of Changes: Provided callback interfaces for long running applications.
Changed Files: include/StdDiag.h
src/StdDiag_ProgPreparation.c
Compatibility:
Revision 5.2.0 [Released]
Item Description
CR ID: BAC-6

### Page 3

Description of Changes: Corrected active session states depending on energy mode
settings.
Changed Files: src/StdDiag_ProgPreparation.c
Compatibility:
Item Description
CR ID: BAC-6249
CR Headline: Provide PostBuild configuration of SGBD-Index
Description of Issues: Parameter "StdDiagSgbdIndex" shall be post build selectable.
Description of Changes: Moved parameter "StdDiagSgbdIndex" to adapter part and add
post build support.
Changed Files: include/StdDiag.h
CMakeLists.txt
cfgdesc/StdDiag_paramdef.arxml
src/StdDiag_SgbdIndex.c
generate/include/StdDiag_Cfg.h.pgen
Compatibility:
Revision 5.1.1 [Released]
Item Description
CR ID: BAC-5176
CR Headline: BAC modules paramdef violate TPS_ECUC_06004
Description of Issues: According to AUTOSAR_TPS_ECUConfiguration
TPS_ECUC_06004 an AdminData field is required at the
beginning of every ECU Configuration Parameter Definition XML
file.
Description of Changes: Added AdminData field containing module version and release
date.
Changed Files: cfgdesc/StdDiag_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6230
CR Headline: Usage of IMPLEMENTATION-CONFIG-CLASSES in BMW
modules is invalid according to ASR4.2.2
Description of Issues: Elements IMPLEMENTATION-CONFIG-CLASSES containing
ECUC-IMPLEMENTATION-CONFIGURATION-CLASS are
deprecated.They shall be replaced by VALUE-CONFIG-
CLASSES/ECUC-VALUE-CONFIGURATION-CLASS and/or
MULTIPLICITY-CONFIG-CLASSES/ECUC-MULTIPLICITY-
CONFIGURATION-CLASS
Description of Changes: Replaced IMPLEMENTATION-CONFIG-CLASSES by
VALUE-CONFIG-CLASSES, added
MULTIPLICITY-CONFIG-CLASSES where necessary.
Changed Files: cfgdesc/StdDiag_paramdef.arxml
ReleaseNotes_StdDiagGeneric, Version 5.3.0, Software Platforms Page 3 of 5

### Page 4

Compatibility:
Item Description
CR ID: BAC-6241
CR Headline: StdDiag: wrong NegReponseCode for $10 02 in default session
Description of Issues: Diagnostic request to switch from default to programming session
is answered with wrong negative response code.
Description of Changes: Corrected negative response code from 0x7F
(ServiceNotSupportedInActiveSession) to 0x7E
(SubFunctionNotSupportedInActiveSession)
Changed Files: src/StdDiag_ProgPreparation.c
Compatibility:
Item Description
CR ID: BAC-6433
CR Headline: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Issues: Schema of parameter definition files and SWCDs should be
conform to AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Changes: Adapted parameter definition files and SWCDs to schema
AUTOSAR_4-3-0_STRICT_COMPACT.
Changed Files: cfgdesc/StdDiag_paramdef.arxml
Compatibility:
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6148
CR Headline: StdDiag: Programming Precondition Check shall not fail in case of
missing PWF status
Description of Issues: Programming Precondition Check fails if no PWF signal is available.
Description of Changes: Accept unknown PWF state as valid Programming Precondition.
Changed Files: src/StdDiag_ProgPreparation.c
include/StdDiag_StmAdapter.h
Compatibility:
Item Description
CR ID: BAC-6134
CR Headline: StdDiag: Svkaktuell fails in extendedSession.FlashModeActivated
Description of Issues: RDBI-Job fails with ConditionsNotCorrect in Status
ExtendedSession.FlashModeActivated.
Description of Changes: Allowed execution of all RDBI jobs in any state.
Changed Files: src/StdDiag_ProgPreparation.c
Compatibility:
ReleaseNotes_StdDiagGeneric, Version 5.3.0, Software Platforms Page 4 of 5

### Page 5

Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_StdDiagGeneric, Version 5.3.0, Software Platforms Page 5 of 5
