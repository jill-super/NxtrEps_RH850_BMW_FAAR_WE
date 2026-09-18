---
title: 'SysTime — SysTimeClassic_ReleaseNotes'
description: 'Converted PDF document SysTimeClassic_ReleaseNotes.pdf from module SysTime.'
sidebar:
  hidden: true
---

> **Source:** `SysTimeClassic_ReleaseNotes.pdf` (PDF, 121 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 4; title: -; author: -

## Converted content

### Page 1

Release Notes SysTimeClassic
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.0.3
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
5.0.3 2017-12-14 BAC-6695
5.0.2 2017-10-12 BAC-5176, BAC-6230, BAC-6433
5.0.1 2017-08-10 BAC-6204, BAC-6200
5.0.0 2017-06-29
ReleaseNotes_SysTimeClassic, Version 5.0.3, Software Platforms Page 1 of 4

### Page 2

1 Module Description
This package contains the adapter for a classic AUTOSAR platform for the SysTimeGeneric package. The
System Time Client is modeled as an AUTOSAR software component (SWC) residing above the RTE.
2 Revisions and Modiﬁcations
Revision 5.0.3 [Released]
Item Description
CR ID: BAC-6695
CR Headline: Fix MISRA violations
Description of Issues: SysTime has MISRA violations.
Description of Changes: Fixed MISRA violations where reasonable.
Changed Files: src/SysTime_ConcAdapter.c
src/SysTimeClassic.c
src/SysTime_TimerAdapter.c
include/SysTime_AssertAdapter.h
Compatibility:
Revision 5.0.2 [Released]
Item Description
CR ID: BAC-5176
CR Headline: BAC modules paramdef violate TPS_ECUC_06004
Description of Issues: According to AUTOSAR_TPS_ECUConfiguration
TPS_ECUC_06004 an AdminData field is required at the
beginning of every ECU Configuration Parameter Definition XML
file.
Description of Changes: Added AdminData field containing module version and release
date.
Changed Files: cfgdesc/SysTimeClassic_paramdef.arxml
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
ReleaseNotes_SysTimeClassic, Version 5.0.3, Software Platforms Page 2 of 4

### Page 3

Description of Changes: Replaced IMPLEMENTATION-CONFIG-CLASSES by
VALUE-CONFIG-CLASSES, added
MULTIPLICITY-CONFIG-CLASSES where necessary.
Changed Files: cfgdesc/SysTimeClassic_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6433
CR Headline: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Issues: Schema of parameter definition files and SWCDs should be
conform to AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Changes: Adapted parameter definition files and SWCDs to schema
AUTOSAR_4-3-0_STRICT_COMPACT.
Changed Files: cfgdesc/SysTimeClassic_paramdef.arxml
generate/meta/SysTime_ext_interfaces.arxml.pgen
generate/meta/SysTime_internal.arxml.pgen
generate/meta/SysTime_interfaces.arxml.pgen
Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6204
CR Headline: SysTime: Wrong cross version check for classic adapter
Description of Issues: SysTimeClassic_Version.h uses wrong cross version check of
generic part.
Description of Changes: Correct cross version check in classic adapter.
Changed Files: generate/include/SysTimeClassic_Version.h.pgen
Compatibility:
Item Description
CR ID: BAC-6200
CR Headline: Improve Requirements Traceability
Description of Issues: Add requirements from IntegrationManual to RequirementsTable.
Description of Changes: Added requirements from IntegrationManual to
RequirementsTable.
Changed Files:
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
ReleaseNotes_SysTimeClassic, Version 5.0.3, Software Platforms Page 3 of 4

### Page 4

Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_SysTimeClassic, Version 5.0.3, Software Platforms Page 4 of 4
