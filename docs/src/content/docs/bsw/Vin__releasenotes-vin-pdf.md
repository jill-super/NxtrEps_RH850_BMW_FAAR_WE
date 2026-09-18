---
title: 'Vin — ReleaseNotes_Vin'
description: 'Converted PDF document ReleaseNotes_Vin.pdf from module Vin.'
sidebar:
  hidden: true
---

> **Source:** `ReleaseNotes_Vin.pdf` (PDF, 167 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 12; title: -; author: -

## Converted content

### Page 1

Release Notes Vin
Project BMW AUTOSAR Core 4 Rel. 2
Author BMW AG
Release Date 2017-02-23
Version 3.5.0
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
3.5.0 2017-02-23 BAC-5764, BAC-5691
3.4.2 2016-10-27 BAC-5544, BAC-5437
3.4.1 2016-08-25 BAC-5426, BAC-5407, BAC-5399, BAC-5286, BAC-5198
3.4.0 2016-03-17 BAC-5049, BAC-5031, BAC-4928
3.3.0 2015-12-11 BAC-4763, BAC-4756, BAC-4702, BAC-4629, BAC-4562
3.2.0 2015-07-10 BAC-4471, BAC-4409, BAC-4349, BAC-4345, BAC-4335,
BAC-4266, BAC-4265, BAC-4230, BAC-4163, BAC-4129,
BAC-3558
3.1.0 2015-03-13 BAC-4108, BAC-3980, BAC-3927, BAC-3868, BAC-3861,
BAC-3822, BAC-3658
3.0.0 2014-10-29
ReleaseNotes_Vin, Version 3.5.0, Software Platforms Page 1 of 12

### Page 2

1 Package Enumeration Scheme
Every package carries a 3-digit version number. The following table explains how compatibility between
versions can be determined from the version number:
Changed Version Example Compatibility
Patch Version 1.0.0 → 1.0.1 A defect has been fixed. Versions are fully
compatible.
Minor Version 1.0.0 → 1.1.0 API of package changed or a new feature was
added. Versions may not be compatible. If the new
package is used, other packages may be changed
as well.
Major Version 1.0.0 → 2.0.0 Indicates the BAC4 Release, in which the module
is delivered. Major Version 2 of a module refers to
BAC4 Rel. 1. Major Version 3 of a module refers to
BAC4 Rel. 2.
2 Package Description
The Vin module is used to request the VIN over the bus, set the qualifier and hand it over to application
software components.
This package is maintained by BMW AUTOSAR Core 4 Support, via ASCENT Jira
(https://asc.bmwgroup.net/jira/browse/BSUP or https://asc.bmw.com/jira/browse/BSUP) or telephone
hotline (+49-89-382-32233).
3 Revisions and Modiﬁcations
3.1 Revision 3.5.0 [Released]
Item Description
CR ID: BAC-5764
CR Headline: Vin: Inter-ECU communication with
SYNCHRONOUS-SERVER-CALL-POINT considered harmful
Description of Issues: The RUNNABLE-ENTITY "Vin_SIAChallenge" uses a
SYNCHRONOUS-SERVER-CALL-POINT
"scp_generateAuthenticationCo" with TIMEOUT "0.0" for
inter-ECU communication. This may cause the executing task to
wait for ever, making it necessary to map the invoking
DATA-RECEIVED-EVENT "dre_Challenge" to its own exclusive
extended task, because other events mapped to the same task
would never get executed if the communication is not finished.
Please check for alternatives.
ReleaseNotes_Vin, Version 3.5.0, Software Platforms Page 2 of 12

### Page 3

Description of Changes: use asynchronous server call point for
ChassisNumberAuthentication/generateAuthenticationCode
Changed Files: generate/swcd/Vin_internal.arxml.tt
src/Vin_SIAdapter.c
Compatibility:
Item Description
CR ID: BAC-5691
CR Headline: Signed message is requested only once
Description of Issues: Signed message is requested only once
Description of Changes: request MAC multiple times before going into error state
Changed Files: generate/include/Vin_Cfg.h.tt
src/Vin_Ssv.c
Compatibility:
3.2 Revision 3.4.2 [Released]
Item Description
CR ID: BAC-5544
CR Headline: Do not request MAC/Counterbase before reception of the VIN
Description of Issues: Do not request MAC/Counterbase before reception of the VIN
Description of Changes: Do not request MAC/Counterbase before reception of the VIN
Changed Files: src/Vin.c
Compatibility:
Item Description
CR ID: BAC-5437
CR Headline: Vin IntegrationManual: NvMNvBlockLength might depend on
compiler
Description of Issues: The values for NvMNvBlockLength given in the IntegrationManuals
might be incorrect (depending on compiler optimisation).
Description of Changes: Add a note on NVM block length in integration manual
Changed Files: doc/IntegrationManual_Vin.pdf
Compatibility:
3.3 Revision 3.4.1 [Released]
Item Description
CR ID: BAC-5426
CR Headline: VIN: Integration Manual: NvMBlockWriteProt true
Description of Issues: In Integration Manual you can find:
NvMBlockWriteProt true
but Vin module cannot handle this
Description of Changes: fix NVM configuration
Changed Files: doc/IntegrationManual_Vin.pdf
ReleaseNotes_Vin, Version 3.5.0, Software Platforms Page 3 of 12

### Page 4

Compatibility:
Item Description
CR ID: BAC-5407
CR Headline: VIN: missing memory mapping of the code in Vin_Dlog.c and
Vin_SIAdapter.c.
Description of Issues: Missing memory mapping of the code in Vin_Dlog.c and
Vin_SIAdapter.c.
Description of Changes: Add missing memory mapping.
Changed Files: src/Vin_Dlog.c
src/Vin_SIAdapter.c
Compatibility:
Item Description
CR ID: BAC-5399
CR Headline: VIN: Vin_CurrentVin.Vin not initalized in VinInit
Description of Issues: As Vin_CurrentVin.Vin is not initialized during c-startup (
Vin_START_SEC_VAR_NO_INIT_UNSPECIFIED) and not
initialized in Vin_init, a reset does not clear the containing last
received VIN. At next startup (without power-loss) the variable still
contains the VIN. Therefore the reception of the bus-vin via
Vin_ReceiveFromCom is ignored and Vin_NotifyVinReceived() is
not called.
A call of Vin_ReceiveFromCom before Vin_Init also leads to this
problem.
Description of Changes: Always handle received VIN, if no VIN has been received before.
Changed Files: src/Vin_Com.c
Compatibility:
Item Description
CR ID: BAC-5286
CR Headline: Vin: Memcopy from struct to array
Description of Issues: Using memcopy to copy data from an struct to an array is not
allowed.
Description of Changes: Copy single elements of struct to array instead of using memcpy.
Changed Files: src/Vin_Com.c
Compatibility:
Item Description
CR ID: BAC-5198
CR Headline: Please remove UUIDs
Description of Issues: remove UUIDs in arxml files
Description of Changes: remove UUIDs in arxml files
Changed Files: generate/swcd/Vin_internal.arxml.tt
Compatibility:
ReleaseNotes_Vin, Version 3.5.0, Software Platforms Page 4 of 12

### Page 5

3.4 Revision 3.4.0 [Released]
Item Description
CR ID: BAC-5049
CR Headline: Vin: Write frequency of NVM blocks shall be specified in integration
manual
Description of Issues: For correct configuration/wearing estimation of flash, the write
frequency of BAC modules for their specified NvM blocks shall be
specified. Although most of the time NO exact number can be
given as it is ECU, use case, environment (customer behaviour)
specific a rough information should be given, that allows the
integrator to make a conclusion on that.
Description of Changes: Specify write frequency of NVM blocks in integration manual.
Changed Files: doc/IntegrationManual_Vin.pdf
Compatibility:
Item Description
CR ID: BAC-5031
CR Headline: Use getter method to get the VIN in case it is not delivered upon
subscription
Description of Issues: Use getter method to get the VIN in case it is not delivered upon
subscription on Ethernet.
Description of Changes: Use getter method to get the VIN in case it is not delivered upon
subscription on Ethernet.
Changed Files: autosar/Asr40/Vin_paramdef.arxml
generate/include/Vin_Cfg.h.tt
generate/make/Vin_Cfg.mak.tt
generate/swcd/Vin_internal.arxml.tt
generate/verify/Vin.autoverify.tt
src/Vin_SIAdapter.c
swcd/Vin_interfaces.arxml
Compatibility:
Item Description
CR ID: BAC-4928
CR Headline: Challenge shall not be reversed on Ethernet
Description of Issues: Challenge shall not be reversed on Ethernet
Description of Changes: do not reverse challenge on Ethernet
Changed Files: src/Vin_Ssv.c
Compatibility:
3.5 Revision 3.3.0 [Released]
Item Description
CR ID: BAC-4763
CR Headline: Vin: Naming of Rte_Write function is wrong
ReleaseNotes_Vin, Version 3.5.0, Software Platforms Page 5 of 12

### Page 6

Description of Issues: The name of function Rte_Write_Vin_SSVErrorCode_ErrorCode is
w

*Excerpt: first 8 of 12 pages shown.*
