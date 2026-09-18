---
title: 'Coding — CodingClassic_ReleaseNotes'
description: 'Converted PDF document CodingClassic_ReleaseNotes.pdf from module Coding.'
sidebar:
  hidden: true
---

> **Source:** `CodingClassic_ReleaseNotes.pdf` (PDF, 124 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 5; title: -; author: -

## Converted content

### Page 1

Release Notes CodingClassic
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.2.1
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
5.2.1 2017-12-14 BAC-6660, BAC-6704, BAC-6561, BAC-6585
5.2.0 2017-11-09 BAC-6434, BAC-6350
5.1.0 2017-10-12 BAC-6402
5.0.1 2017-09-14 BAC-6250, BAC-6239, BAC-6224, BAC-5170
5.0.0 2017-06-29
ReleaseNotes_CodingClassic, Version 5.2.1, Software Platforms Page 1 of 5

### Page 2

1 Module Description
The Coding system consists of a Coding module that is part of the ECU application and the Coder.
Almost in the same manner as the Bootloader programs the ROM of an ECU, the Coding module codes
the NV memory of an ECU with vehicle specific data derived from the vehicle description document e.g.
type key, extra equipment, country specifics, year of model/construction stage, additional comments or
service upgrade options.
2 Revisions and Modiﬁcations
Revision 5.2.1 [Released]
Item Description
CR ID: BAC-6660
CR Headline: Correct Misra- and Metric-violations
Description of Issues: Correct Misra- and Metric-violations and compiler warnings.
Description of Changes: Correct Misra- and Metric-violations and compiler warnings.
Changed Files: src/Coding_UDSAdapter.c
src/Coding_TimerAdapter.c
generate/include/CodingClassic_Cfg.h.pgen
template/include/Coding_MemMap.h.sample
generate/meta/Coding_internal.arxml.pgen
include/Coding_Assert.h
generate/meta/Coding_ext_interfaces.arxml.pgen
src/Coding_ErrMemAdapter.c
src/Coding_CryptoAdapter.c
doc/CodingClassic_RequirementsTable.pdf
generate/include/CodingClassic_Version.h.pgen
doc/CodingClassic_IntegrationManual.pdf
generate/meta/Coding_interfaces.arxml.pgen
doc/CodingClassic_UserManual.pdf
Compatibility:
Item Description
CR ID: BAC-6704
CR Headline: Activation of signature verification (RSA)
Description of Issues: Changed Coding adapter to fit to the provided Crypto-Lib (RSA).
Description of Changes: Changed Coding adapter to fit to the provided Crypto-Lib (RSA).
Changed Files: src/Coding_CryptoAdapter.c
Compatibility:
Item Description
CR ID: BAC-6561
ReleaseNotes_CodingClassic, Version 5.2.1, Software Platforms Page 2 of 5

### Page 3

CR Headline: Wrong description of event mapping "Coding_TimerMain" in
IntegrationManual
Description of Issues: Fix description of event mapping "Coding_TimerMain" in
Integration Manual.
Description of Changes: Changed description from "Mode Switch Event" to "Timing Event".
Changed Files: doc/CodingClassic_IntegrationManual.pdf
Compatibility:
Item Description
CR ID: BAC-6585
CR Headline: Rework Coding_paramdef.arxml
Description of Issues: Add missing configuration parameters, provide human readable
Coding function value input field and support tool based
implementation type range check.
Description of Changes: Added missing configuration parameters ’lowerlimit’ and
’upperlimit’. Use choice container for supported implementation
data types. Updated PAGe include files to convert human readable
Coding function values to Coding internal machine code.
Changed Files: doc/CodingClassic_IntegrationManual.pdf
Compatibility:
Revision 5.2.0 [Released]
Item Description
CR ID: BAC-6434
CR Headline: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Issues: Schema of parameter definition files and SWCDs should be
conform to AUTOSAR_4-3-0_STRICT_COMPACT.xsd.
Description of Changes: Adapted parameter definition files and SWCDs to schema
AUTOSAR_4-3-0_STRICT_COMPACT.
Changed Files: cfgdesc/CodingClassic_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6350
CR Headline: RoutineSignal Arrays must be configured with
VARIABLE_LENGTH
Description of Issues: Routine signal arrays must be configured with
VARIABLE_LENGTH.
Description of Changes: Coding generic has to support an additional function parameter
’dataLength’ and Coding adapter has to support configuration with
VARIABLE_LENGTH.
Changed Files: src/Coding_UDSAdapter.c
CMakeLists.

### Page 4

Compatibility:
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6402
CR Headline: Activation of signature verification
Description of Issues: Customize the function calls according to specification. Support
the provided Crypto-Lib.
Description of Changes: Removed unnecessary function call from Coding module.
Changed Coding adapter to fit to the provided Crypto-Lib on one
side and to fullfill the specification requirements on the other side.
Changed Files: generate/meta/Coding_ext_interfaces.arxml.pgen
generate/meta/Coding_internal.arxml.pgen
src/Coding_CryptoAdapter.c
Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6250
CR Headline: CodingClassic_MemMap.h.sample should be
Coding_MemMap.h.sample
Description of Issues: Sample file has wrong file name.
Description of Changes: Corrected file name.
Changed Files: template/include/Coding_MemMap.h.sample
Compatibility:
Item Description
CR ID: BAC-6239
CR Headline: Improve requirements traceability
Description of Issues: Improve generation of documents.
Description of Changes: Replace special character and add reference information.
Changed Files: doc/Coding_RequirementsTable.pdf
Compatibility:
Item Description
CR ID: BAC-6224
CR Headline: PublishedInformation of BMW modules is not modeled according
to ASR4.2.2
Description of Issues: Removed depricated ImplementationConfigClass from
PublishedInformation and added ValueConfigClass instead.
Description of Changes: File content was updated.
Changed Files: cfgdesc/CodingClassic_paramdef.arxml
Compatibility:
ReleaseNotes_CodingClassic, Version 5.2.1, Software Platforms Page 4 of 5

### Page 5

Item Description
CR ID: BAC-5170
CR Headline: Modules paramdef violates TPS_ECUC_06004
Description of Issues: AdminData filed in ECU configuration parameter definition is
required.
Description of Changes: Added missing AdminData field.
Changed Files: cfgdesc/CodingClassic_paramdef.arxml
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_CodingClassic, Version 5.2.1, Software Platforms Page 5 of 5
