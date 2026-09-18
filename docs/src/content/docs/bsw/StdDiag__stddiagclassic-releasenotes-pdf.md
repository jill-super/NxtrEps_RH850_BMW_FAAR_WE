---
title: 'StdDiag — StdDiagClassic_ReleaseNotes'
description: 'Converted PDF document StdDiagClassic_ReleaseNotes.pdf from module StdDiag.'
sidebar:
  hidden: true
---

> **Source:** `StdDiagClassic_ReleaseNotes.pdf` (PDF, 127 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 6; title: -; author: -

## Converted content

### Page 1

Release Notes StdDiagClassic
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.4.0
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
5.4.0 2017-12-14 BAC-6630, BAC-6257, BAC-6699, BAC-6248
5.3.0 2017-11-09 BAC-6506, BAC-6249
5.2.0 2017-10-12 BAC-6413, BAC-6347, BAC-5176, BAC-6339, BAC-6433,
BAC-6230
5.1.0 2017-08-10 BAC-6162, BAC-6148
5.0.0 2017-06-29
ReleaseNotes_StdDiagClassic, Version 5.4.0, Software Platforms Page 1 of 6

### Page 2

1 Module Description
This package contains the adapter for a classic AUTOSAR platform for the StdDiagGeneric package. The
StdDiag module is modeled as an AUTOSAR software component residing above the RTE.
2 Revisions and Modiﬁcations
Revision 5.4.0 [Released]
Item Description
CR ID: BAC-6630
CR Headline: StdDiagClassic - *.pgen templates inconsistent with paramdef
Description of Issues: Optional configuration container "StdDiagUserDefinedMemory" is
treated as mandatory if parameter
"StdDiagClearSecondaryErrorMemory" is enabled, which may
cause misleading error messages.
Description of Changes: Create proper error message if configuration dependencies are
violated.
Changed Files: generate/meta/StdDiag_ext_interfaces.arxml.pgen
generate/pageinclude/StdDiag_GetIdrlConfig.pgen
generate/include/StdDiagClassic_Cfg.h.pgen
Compatibility:
Item Description
CR ID: BAC-6257
CR Headline: Provide feature "Application Data Transfer (ADT)"
Description of Issues: Provide dispatcher for common diagnostic requests of functionality
"Application Data Transfer" (ADT) (german:
"Applikationsdatenübertragung", ADÜ).
Description of Changes: Provided dispatcher for RoutineControl "Upload/Download
Pre/Post-Processing" (RID 0x7000) and diagnostic services
"RequestDownload" (0x34), "RequestUpload" (0x35),
"TransferData" (0x36) and "RequestTransferExit" (0x37). Provided
configuration parameters for ADT memory objects.
Changed Files: CMakeLists.txt
cfgdesc/StdDiagClassic_paramdef.arxml
doc/StdDiagClassic_IntegrationManual.pdf
generate/include/StdDiagClassic_Cfg.h.pgen
generate/meta/StdDiag_bswmd.arxml.pgen
generate/meta/StdDiag_ext_interfaces.arxml.pgen
generate/meta/StdDiag_internal.arxml.pgen
generate/meta/StdDiag_interfaces.arxml.pgen
generate/pageinclude/StdDiag_GetAdtConfig.pgen
generate/src/StdD

### Page 3

include/StdDiag_DcmTypes.h
src/StdDiag_Adt.c
src/StdDiag_AdtInternal.h
src/StdDiag_AdtUploadDownload.c
Compatibility:
Item Description
CR ID: BAC-6699
CR Headline: Remove compiler abstraction from source code
Description of Issues: Remove AUTOSAR compiler abstraction from source code.
Description of Changes: Removed compiler abstraction.
Changed Files: generate/src/StdDiagClassic_Cfg.c.pgen
src/StdDiag_IDRLAdapter.c
include/StdDiag_IDRLAdapter.h
Compatibility:
Item Description
CR ID: BAC-6248
CR Headline: Provide callback mechanism to establish intrinsic safety
Description of Issues: Provide an asynchronous callback mechanism to establish intrinsic
safety for long running user callouts.
Description of Changes: Provided callback interfaces for long running applications.
Changed Files: src/StdDiagClassic.c
src/StdDiag_AppAdapter.c
generate/meta/StdDiag_ext_interfaces.arxml.pgen
generate/meta/StdDiag_interfaces.arxml.pgen
doc/StdDiagClassic_IntegrationManual.pdf
generate/meta/StdDiag_internal.arxml.pgen
Compatibility:
Revision 5.3.0 [Released]
Item Description
CR ID: BAC-6506
CR Headline: Adapt pgen templates to PAGe v1.1.0
Description of Issues: Adapt pgen files to PAGe v1.1.0.
Description of Changes: Adapted pgen files to PAGe v1.1.0.
Changed Files: generate/meta/StdDiag_internal.arxml.pgen
Compatibility:
Item Description
CR ID: BAC-6249
CR Headline: Provide PostBuild configuration of SGBD-Index
Description of Issues: Parameter "StdDiagSgbdIndex" shall be post build selectable.
Description of Changes: Moved parameter "StdDiagSgbdIndex" to adapter part and add
post build support.
ReleaseNotes_StdDiagClassic, Version 5.4.0, Software Platforms Page 3 of 6

### Page 4

Changed Files: src/StdDiagClassic.c
generate/include/StdDiagClassic_PBCfg.h.pgen
cfgdesc/StdDiagClassic_paramdef.arxml
generate/src/StdDiagClassic_PBCfg.c.pgen
CMakeLists.txt
doc/StdDiagClassic_IntegrationManual.pdf
Compatibility:
Revision 5.2.0 [Released]
Item Description
CR ID: BAC-6413
CR Headline: StdDiag: Remove SP2015/2015 suffixes from VEHICLE STATE
Description of Issues: Remove suffixes "SP2015" from interfaces provided by Stm to be
compatible with current Stm release.
Description of Changes: Removed suffixes "SP2015" from all Stm interfaces and types.
Changed Files: src/StdDiag_StmAdapter.c
generate/meta/StdDiag_ext_interfaces.arxml.pgen
generate/meta/StdDiag_internal.arxml.pgen
Compatibility:
Item Description
CR ID: BAC-6347
CR Headline: StdDiag: Use of DcmGetSecurityLevel
Description of Issues: Remove unused server call point to operation "GetSecurityLevel"
Description of Changes: Removed all fragments from SWCD related to operation
"GetSecurityLevel".
Changed Files: generate/meta/StdDiag_ext_interfaces.arxml.pgen
generate/meta/StdDiag_internal.arxml.pgen
Compatibility:
Item Description
CR ID: BAC-5176
CR Headline: BAC modules paramdef violate TPS_ECUC_06004
Description of Issues: According to AUTOSAR_TPS_ECUConfiguration
TPS_ECUC_06004 an AdminData field is required at the
beginning of every ECU Configuration Parameter Definition XML
file.
Description of Changes: Added AdminData field containing module version and release
date.
Changed Files: cfgdesc/StdDiagClassic_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6339
CR Headline: Compiler warning due to undefined identifier
ReleaseNotes_StdDiagClassic, Version 5.4.0, Software Platforms Page 4 of 6

### Page 5

Description of Issues: Compiler raises warning due to undefined identifier
’STDDIAG_DEV_ERROR_DETECT’
Description of Changes: Fixed compiler warning.
Changed Files: src/StdDiagClassic.c
include/StdDiag_AssertAdapter.h
src/StdDiag_ErrMemAdapter.c
Compatibility:
Item Description
CR ID: BAC-6433
CR Headline: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Issues: Schema of parameter definition files and SWCDs should be
conform to AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Changes: Adapted parameter definition files and SWCDs to schema
AUTOSAR_4-3-0_STRICT_COMPACT.
Changed Files: generate/meta/StdDiag_interfaces.arxml.pgen
cfgdesc/StdDiagClassic_paramdef.arxml
generate/meta/StdDiag_ext_interfaces.arxml.pgen
generate/meta/StdDiag_internal.arxml.pgen
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
Changed Files: cfgdesc/StdDiagClassic_paramdef.arxml
Compatibility:
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6162
CR Headline: StdDiag: Wrong cross version check for classic adapter
Description of Issues: StdDiagClassic_Version.h uses wrong cross version check of
generic part.
Description of Changes: Correct cross version check in classic adapter.
ReleaseNotes_StdDiagClassic, Version 5.4.0, Software Pla

### Page 6

Changed Files: generate/include/StdDiagClassic_Version.h.pgen
Compatibility:
Item Description
CR ID: BA
