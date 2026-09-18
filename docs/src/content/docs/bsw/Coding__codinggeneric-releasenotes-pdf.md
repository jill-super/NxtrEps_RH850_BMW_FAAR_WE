---
title: 'Coding — CodingGeneric_ReleaseNotes'
description: 'Converted PDF document CodingGeneric_ReleaseNotes.pdf from module Coding.'
sidebar:
  hidden: true
---

> **Source:** `CodingGeneric_ReleaseNotes.pdf` (PDF, 125 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 6; title: -; author: -

## Converted content

### Page 1

Release Notes CodingGeneric
Project BMW AUTOSAR Core 4 Rel. 3 and adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-12-14
Version 5.2.1
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
5.2.1 2017-12-14 BAC-6660, BAC-6704, BAC-6585, BAC-6736, BAC-6192
5.2.0 2017-11-09 BAC-6434, BAC-6350
5.1.0 2017-10-12 BAC-6402
5.0.1 2017-09-14 BAC-6302, BAC-6239, BAC-6224, BAC-6073, BAC-6003,
BAC-5170
5.0.0 2017-06-29
ReleaseNotes_CodingGeneric, Version 5.2.1, Software Platforms Page 1 of 6

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
Changed Files: generate/include/Coding_Cfg.h.pgen
doc/CodingGeneric_RequirementsTable.pdf
template/include/Coding_MemMap.h.sample
generate/src/Coding_Function.c.pgen
generate/include/Coding_Version.h.pgen
generate/include/Coding_Function.h.pgen
generate/src/Coding_Cfg.c.pgen
include/Coding_CryptoAdapter.h
generate/pageinclude/Coding_Functions.pgen
generate/pageinclude/Coding_Function_Types.pgen
src/Coding.c
include/Coding.h
Compatibility:
Item Description
CR ID: BAC-6704
CR Headline: Activation of signature verification (RSA)
Description of Issues: Changed Coding adapter to fit to the provided Crypto-Lib (RSA).
Description of Changes: Changed Coding adapter to fit to the provided Crypto-Lib (RSA).
Changed Files: generate/pageinclude/Coding_Functions.pgen
generate/src/Coding_Function.c.pgen
Compatibility:
Item Description
CR ID: BAC-6585
CR Headline: Rework Coding_paramdef.arxml
ReleaseNotes_CodingGeneric, Version 5.2.1, Software Platforms Page 2 of 6

### Page 3

Description of Issues: Add missing configuration parameters, provide human readable
Coding function value input field and support tool based
implementation type range check.
Description of Changes: Added missing configuration parameters ’lowerlimit’ and
’upperlimit’. Use choice container for supported implementation
data types. Updated PAGe include files to convert human readable
Coding function values to Coding internal machine code.
Changed Files: generate/pageinclude/Coding_Function_Types.pgen
cfgdesc/Coding_paramdef.arxml
generate/pageinclude/Coding_Functions.pgen
Compatibility:
Item Description
CR ID: BAC-6736
CR Headline: Fix optional production error CEUD compile error
Description of Issues: Deactivation of optional production error leads to compile error.
Description of Changes: Add missing preprocessor directives.
Changed Files: src/Coding.c
Compatibility:
Item Description
CR ID: BAC-6192
CR Headline: Identical function names in different coding areas lead to
generation of duplicate event names
Description of Issues: Add Coding configuration plausibility check.
Description of Changes: Check uniqueness of all Coding function names in Coding
configuration.
Changed Files: generate/pageinclude/Coding_Functions.pgen
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
Changed Files: cfgdesc/Coding_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6350
ReleaseNotes_CodingGeneric, Version 5.2.1, Software Platform

### Page 4

CR Headline: RoutineSignal Arrays must be configured with
VARIABLE_LENGTH
Description of Issues: Routine signal arrays must be configured with
VARIABLE_LENGTH.
Description of Changes: Coding generic has to support an additional function parameter
’dataLength’ and Coding adapter has to support configuration with
VARIABLE_LENGTH.
Changed Files: src/Coding.c
include/Coding.h
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
Changed Files: generate/include/Coding_Cfg.h.pgen
cfgdesc/Coding_paramdef.arxml
include/Coding_CryptoAdapter.h
generate/pageinclude/Coding_Functions.pgen
generate/pageinclude/Coding_Function_Types.pgen
src/Coding.c
Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6302
CR Headline: Add look up table for type conversion
Description of Issues: Provide look up table (adaptive platform and ara implementation
data types) for PAGe.
Description of Changes: Added look up table for adaptive platform and ara implementation
data types in page include file.
Changed Files: generate/pageinclude/Coding_Functions.pgen
Compatibility:
Item Description
CR ID: BAC-6239
CR Headline: Improve requirements traceability
Description of Issues: Improve generation of documents.
Description of Changes: Replace special character and add reference information.
ReleaseNotes_CodingGeneric, Version 5.2.1, Software Platforms Page 4 of 6

### Page 5

Changed Files: doc/Coding_RequirementsTable.pdf
Compatibility:
Item Description
CR ID: BAC-6224
CR Headline: PublishedInformation of BMW modules is not modeled according
to ASR4.2.2
Description of Issues: Removed depricated ImplementationConfigClass from
PublishedInformation and added ValueConfigClass instead.
Description of Changes: File content was updated.
Changed Files: cfgdesc/Coding_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6073
CR Headline: Stop timeout monitoring during module shutdown
Description of Issues: Stop timeout monitoring (Coding data qualification) during
shutdown.
Description of Changes: Added call: Coding_Timer_CancelTimer() in Coding_Shutdown()
(sync branch) and in
Coding_NvMFinishedCallbackWriteCodingData() (async branch).
Changed Files: src/Coding.c
Compatibility:
Item Description
CR ID: BAC-6003
CR Headline: Transformation rule must respect signedness of nvRam type
Description of Issues: The Coding transformation rule mechanism does not consider that
the Coding data are stored in an uint8 array when the user
application requests an sint8 Coding value.
Description of Changes: Add missing type cast when Coding data are extracted from uint8
array.
Changed Files: generate/src/Coding_Function.c.pgen
Compatibility:
Item Description
CR ID: BAC-5170
CR Headline: Modules paramdef violates TPS_ECUC_06004
Description of Issues: AdminData filed in ECU configuration parameter definition is
required.
Description of Changes: Added missing AdminData field.
Changed Files: cfgdesc/Coding_paramdef.arxml
Compatibility:
Revision 5.0.0 [Released]
ReleaseNotes_CodingGeneric, Version 5.2.1, Software Platforms Page 5 of 6

### Page 6

Item Description
CR ID:
CR Hea
