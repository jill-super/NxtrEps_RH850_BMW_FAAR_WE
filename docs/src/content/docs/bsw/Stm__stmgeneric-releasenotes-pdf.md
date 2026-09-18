---
title: 'Stm — StmGeneric_ReleaseNotes'
description: 'Converted PDF document StmGeneric_ReleaseNotes.pdf from module Stm.'
sidebar:
  hidden: true
---

> **Source:** `StmGeneric_ReleaseNotes.pdf` (PDF, 119 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 3; title: -; author: -

## Converted content

### Page 1

Release Notes StmGeneric
Project BMW AUTOSAR Core 4 Rel. 3 and adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-12-14
Version 5.2.0
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
5.2.0 2017-12-14 BAC-6524
5.1.1 2017-11-09 BAC-6246
5.1.0 2017-10-12 BAC-6254, BAC-6202, BAC-6247
5.0.0 2017-06-29
ReleaseNotes_StmGeneric, Version 5.2.0, Software Platforms Page 1 of 3

### Page 2

1 Module Description
The main objective of the STM functionality is to listen to certain vehicle wide states that are
communicated on the system busses and maintain these states for the local ECU. This means: - Make
these states available as modes to other software components - React on some changes of these states
(for instance setting Dem enableconditions) - React on timeouts of these communicated states (set
default values, reporterror events accordingly) The STM module is modeled as an AUTOSAR software
component (SWC) residing above the RTE.
2 Revisions and Modiﬁcations
Revision 5.2.0 [Released]
Item Description
CR ID: BAC-6524
CR Headline: Separate parameter definition from generic into classic/adaptive
Description of Issues: Separate parameter definition from generic into classic/adaptive.
Description of Changes: Separating the parameter definition from the Stm generic into the
Stm classic/adaptive adapter.
Changed Files: include/Stm_Version.h
include/Stm_MgmtAdapter.h
cfgdesc/Stm_paramdef.arxml
include/Stm_ErrMemAdapter.h
CMakeLists.txt
include/Stm.h
Compatibility:
Revision 5.1.1 [Released]
Item Description
CR ID: BAC-6246
CR Headline: Add Requirement Traceability
Description of Issues: Requirements Tracing incomplete
Description of Changes: Added Requirements Traceability
Changed Files: doc/StmGeneric_RequirementsTable.pdf
src/Stm.c
Compatibility:
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6254
CR Headline: Stm: Usage of IMPLEMENTATION-CONFIG-CLASSES is
deprecated and shall be replaced by VALUE-CONFIG-CLASSES
according to ASR4.2.2
ReleaseNotes_StmGeneric, Version 5.2.0, Software Platforms Page 2 of 3

### Page 3

Description of Issues: Usage of Tag IMPLEMENTATION-CONFIG-CLASS is
deprecated.
Description of Changes: Updated parameter definition to comply with AUTOSAR schema.
Changed Files: cfgdesc/Stm_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6202
CR Headline: Remove SP2015/2015 suffixes from VEHICLE STATE
Description of Issues: Editorial changes.
Description of Changes: Removing the SP2015/2015 suffixes from VEHICLE STATE.
Changed Files: cfgdesc/Stm_paramdef.arxml
src/Stm.c
Compatibility:
Item Description
CR ID: BAC-6247
CR Headline: Wrong file header in Stm_ext_interfaces.arxml
Description of Issues: File Headers were in wrong format.
Description of Changes: Corrected all file headers
Changed Files: include/Stm_MgmtAdapter.h
include/Stm_ErrMemAdapter.h
generate/include/Stm_Version.h.pgen
include/Stm.h
generate/include/Stm_Cfg.h.pgen
template/include/Stm_MemMap.h.sample
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_StmGeneric, Version 5.2.0, Software Platforms Page 3 of 3
