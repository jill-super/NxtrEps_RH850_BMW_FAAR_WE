---
title: 'Omc — OmcClassic_ReleaseNotes'
description: 'Converted PDF document OmcClassic_ReleaseNotes.pdf from module Omc.'
sidebar:
  hidden: true
---

> **Source:** `OmcClassic_ReleaseNotes.pdf` (PDF, 122 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 5; title: -; author: -

## Converted content

### Page 1

Release Notes OmcClassic
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
5.2.0 2017-12-14 BAC-5455, BAC-6565, BAC-6717, BAC-6460
5.1.1 2017-10-12 BAC-6397, BAC-6041
5.1.0 2017-08-10 BAC-6210, BAC-6163, BAC-4161
5.0.0 2017-06-29
ReleaseNotes_OmcClassic, Version 5.2.0, Software Platforms Page 1 of 5

### Page 2

1 Module Description
The main objective of the OMC functionality is to maintain the current Operation Mode of an ECU.
2 Revisions and Modiﬁcations
Revision 5.2.0 [Released]
Item Description
CR ID: BAC-5455
CR Headline: Adapt code to be MISRA and improve code coverage
Description of Issues: Improve code to be MISRA conform. Improve unit test code
coverage.
Description of Changes: Improve code to be MISRA conform. Improve unit test code
coverage.
Changed Files: generate/meta/Omc_internal.arxml.pgen
src/Omc_ApplAdapter.c
src/Omc_StdDiagAdapter.c
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
Changed Files: doc/OmcClassic_IntegrationManual.pdf
generate/meta/Omc_internal.arxml.pgen
src/Omc_ApplAdapter.c
src/Omc_StdDiagAdapter.c
Compatibility:
Item Description
CR ID: BAC-6717
CR Headline: Improve requirement tracing
Description of Issues: Improve requirement tracing table.
Description of Changes: Improve requirement tracing table.
Changed Files: generate/meta/Omc_interfaces.arxml.pgen
doc/OmcClassic_IntegrationManual.pdf
doc/OmcClassic_RequirementsTable.pdf
ReleaseNotes_OmcClassic, Version 5.2.0, Software Platforms Page 2 of 5

### Page 3

Compatibility:
Item Description
CR ID: BAC-6460
CR Headline: Provide callback mechanism to establish intrinsic safety
Description of Issues: Provide a callback mechanism for StdDiag and the Application to
accept a mode change, and also to be informed if the mode
change is not completed.
Description of Changes: Improve the callback mechanismus to StdDiag and the Application.
Providing an extra interface to allow or disallow a mode change
using a callback. Also provide a callback to confirm a rollback if a
mode change is not completed.
Changed Files: generate/meta/Omc_interfaces.arxml.pgen
Compatibility:
Revision 5.1.1 [Released]
Item Description
CR ID: BAC-6397
CR Headline: OmcClassic: Omc_NvM.h may lead to multiple RTE Application
header file inclusions
Description of Issues: Omc_NvM.h needs to be included by the NvM as many others
includes files of differents SWCs, if each one includes
Rte_<SWCName>.h the NvM code can not be compiled. Only one
Rte_<SWC>.h can be included from a file.
Description of Changes: Omc_NvM.h inclusion of Rte_Omc.h has been replaced by
Rte_Omc_Type.h.
Changed Files: include/Omc_NvM.h
Compatibility:
Item Description
CR ID: BAC-6041
CR Headline: Omc: SERVER-ARGUMENT-IMPL-POLICY should be set to
USE-ARRAY-BASE-TYPE
Description of Issues: Arrays shall set SERVER-ARGUMENT-IMPL-POLICY to
USE-ARRAY-BASE-TYPE.
Description of Changes: Change the SERVER-ARGUMENT-IMPL-POLICY of
CS-Operation "ReadData" of CS-Interfaces
"DataServices_ExtendedOperatingMode" and
"DataServices_OperatingMode" to USE-ARRAY-BASE-TYPE.
Changed Files: generate/meta/Omc_ext_interfaces.arxml.pgen
Compatibility:
Revision 5.1.0 [Released]
Item Description
ReleaseNotes_OmcClassic, Version 5.2.0, Software Platforms Page 3 of 5

### Page 4

CR ID: BAC-6210
CR Headline: Improve Requirements Traceability
Description of Issues: Add requirements from IntegrationManual to RequirementsTable.
Description of Changes: Added requirements from IntegrationManual to
RequirementsTable.
Changed Files:
Compatibility:
Item Description
CR ID: BAC-6163
CR Headline: Omc: Version header for classic adapter is missing
Description of Issues: Omc Classic Adapter does not provide a version header file.
Description of Changes: Added version header file for classic adapter.
Changed Files: src/OmcClassic_Version.h
include/OmcClassic_Version.h
include/Omc_NvM.h
src/Omc_ErrMemAdapter.c
src/Omc_ConcAdapter.c
src/Omc_ApplAdapter.c
src/Omc_MgmtAdapter.c
include/Omc_Assert.h
src/Omc_NvMAdapter.c
src/Omc_StdDiagAdapter.c
src/Omc_UDSAdapter.c
Compatibility:
Item Description
CR ID: BAC-4161
CR Headline: Omc: Remove R-Port "LifeCycleLoopback", change P-Port
"LifeCycle" to PR-Port
Description of Issues: Remove R-Port "LifeCycleLoopback", change P-Port "LifeCycle"
to PR-Port.
Description of Changes: Removed R-Port "LifeCycleLoopback" and changed P-Port
"LifeCycle" to PR-Port.
Changed Files: generate/meta/Omc_internal.arxml.pgen
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
ReleaseNotes_OmcClassic, Version 5.2.0, Software Platforms Page 4 of 5

### Page 5

Compatibility:
ReleaseNotes_OmcClassic, Version 5.2.0, Software Platforms Page 5 of 5
