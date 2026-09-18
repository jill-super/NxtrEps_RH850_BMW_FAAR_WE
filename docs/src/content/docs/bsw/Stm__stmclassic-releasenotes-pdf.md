---
title: 'Stm — StmClassic_ReleaseNotes'
description: 'Converted PDF document StmClassic_ReleaseNotes.pdf from module Stm.'
sidebar:
  hidden: true
---

> **Source:** `StmClassic_ReleaseNotes.pdf` (PDF, 124 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 5; title: -; author: -

## Converted content

### Page 1

Release Notes StmClassic
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.2.0
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
5.2.0 2017-12-14 BAC-6522, BAC-6523, BAC-6524, BAC-6255, BAC-6307
5.1.1 2017-11-09 BAC-6246, BAC-6436
5.1.0 2017-10-12 BAC-6247, BAC-6202, BAC-6429
5.0.0 2017-06-29
ReleaseNotes_StmClassic, Version 5.2.0, Software Platforms Page 1 of 5

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
CR ID: BAC-6522
CR Headline: Add AdminData field to paramdef
Description of Issues: AdminData field is missing in the paramdef files.
Description of Changes: Adding AdminData field to paramdef files.
Changed Files: cfgdesc/StmClassic_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6523
CR Headline: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Issues: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd.
Description of Changes: Assuring that the Schema of paramdefs, paramconfs and SWCDen
is compatible with AUTOSAR_4-3-0_STRICT_COMPACT.xsd.
Changed Files: generate/meta/Stm_interfaces.arxml.pgen
meta/Stm_ext_interfaces.arxml
cfgdesc/StmClassic_paramdef.arxml
generate/meta/Stm_internal.arxml.pgen
Compatibility:
Item Description
CR ID: BAC-6524
CR Headline: Separate parameter definition from generic into classic/adaptive
Description of Issues: Separate parameter definition from generic into classic/adaptive.
Description of Changes: Separating the parameter definition from the Stm generic into the
Stm classic/adaptive adapter.
Changed Files: generate/include/StmClass

### Page 3

CMakeLists.txt
generate/meta/Stm_interfaces.arxml.pgen
generate/include/Stm_Cfg.h.pgen
cfgdesc/StmClassic_paramdef.arxml
generate/include/StmClassic_PBCfg.h.pgen
Compatibility:
Item Description
CR ID: BAC-6255
CR Headline: Create TEX based integration manuals
Description of Issues: Create TEX based integration manuals.
Description of Changes: Creating TEX based integration manuals.
Changed Files: CMakeLists.txt
doc/StmClassic_IntegrationManual.pdf
Compatibility:
Item Description
CR ID: BAC-6307
CR Headline: StmClassic: Compiler warnings - Stm_v5.0.0 - mgcc_v4.5.1
Description of Issues: Compiler warnings - Stm_v5.0.0 - mgcc_v4.5.1
Description of Changes: Fixing Compiler warnings.
Changed Files: generate/include/StmClassic_Cfg.h.pgen
src/Stm_TimerAdapter.c
include/Stm_Timer.h
src/Stm_ComAdapter.c
Compatibility:
Revision 5.1.1 [Released]
Item Description
CR ID: BAC-6246
CR Headline: Add Requirement Traceability
Description of Issues: Requirements Tracing incomplete
Description of Changes: Added Requirements Traceability
Changed Files: src/Stm_ErrMemAdapter.c
src/Stm_MgmtAdapter.c
generate/include/StmClassic_Cfg.h.pgen
src/Stm_ComAdapter.c
doc/StmClassic_RequirementsTable.pdf
src/Stm_TimerAdapter.c
Compatibility:
Item Description
CR ID: BAC-6436
CR Headline: Stm version checks incorrect
Description of Issues: Incorrect version check macro usage.
ReleaseNotes_StmClassic, Version 5.2.0, Software Platforms Page 3 of 5

### Page 4

Description of Changes: Corrected usage.
Changed Files: include/StmClassic_Version.h
src/Stm_ErrMemAdapter.c
src/Stm_MgmtAdapter.c
generate/include/StmClassic_Cfg.h.pgen
generate/src/StmClassic_PBCfg.c.pgen
include/Stm_Com.h
src/Stm_ComAdapter.c
src/Stm_TimerAdapter.c
include/Stm_Timer.h
include/Stm_Mgmt.h
generate/include/StmClassic_PBCfg.h.pgen
Compatibility:
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6247
CR Headline: Wrong file header in Stm_ext_interfaces.arxml
Description of Issues: File Headers were in wrong format.
Description of Changes: Corrected all file headers
Changed Files: src/Stm_ErrMemAdapter.c
generate/include/StmClassic_Cfg.h.pgen
generate/src/StmClassic_PBCfg.c.pgen
include/Stm_Com.h
src/Stm_TimerAdapter.c
meta/Stm_ext_interfaces.arxml
generate/meta/Stm_internal.arxml.pgen
include/Stm_Timer.h
generate/meta/Stm_interfaces.arxml.pgen
generate/include/StmClassic_PBCfg.h.pgen
Compatibility:
Item Description
CR ID: BAC-6202
CR Headline: Remove SP2015/2015 suffixes from VEHICLE STATE
Description of Issues: Editorial changes.
Description of Changes: Removing the SP2015/2015 suffixes from VEHICLE STATE.
Changed Files: src/Stm_MgmtAdapter.c
generate/include/StmClassic_Cfg.h.pgen
generate/src/StmClassic_PBCfg.c.pgen
src/Stm_ComAdapter.c
generate/meta/Stm_internal.arxml.pgen
generate/meta/Stm_interfaces.arxml.pgen
include/Stm_Mgmt.h
ReleaseNotes_StmClassic, Version 5.2.0, Software Platforms Page 4 of 5

### Page 5

generate/include/StmClassic_PBCfg.h.pgen
Compatibility:
Item Description
CR ID: BAC-6429
CR Headline: Stm references parameters with wrong names in pgen files
Description of Issues: Stm references parameter "stmVehicleStateEnabled" with lower
case first letter, which is wrong, in several *.pgen files.
Description of Changes: Fixed parameter name.
Changed Files: generate/include/StmClassic_Cfg.h.pgen
generate/meta/Stm_internal.arxml.pgen
generate/src/StmClassic_PBCfg.c.pgen
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_StmClassic, Version 5.2.0, Software Platforms Page 5 of 5
