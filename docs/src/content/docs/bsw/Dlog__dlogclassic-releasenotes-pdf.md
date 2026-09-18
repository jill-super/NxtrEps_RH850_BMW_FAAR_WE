---
title: 'Dlog — DlogClassic_ReleaseNotes'
description: 'Converted PDF document DlogClassic_ReleaseNotes.pdf from module Dlog.'
sidebar:
  hidden: true
---

> **Source:** `DlogClassic_ReleaseNotes.pdf` (PDF, 142 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 9; title: -; author: -

## Converted content

### Page 1

Release Notes DlogClassic
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.3.1
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
5.3.1 2017-12-14 BAC-6570, BAC-6575, BAC-6620, BAC-6728, BAC-6709,
BAC-6721, BAC-6731, BAC-6672
5.3.0 2017-11-09 BAC-6461, BAC-6363, BAC-6422, BAC-6362, BAC-6055
5.2.1 2017-10-12 BAC-6373
5.2.0 2017-09-14 BAC-6296, BAC-6223, BAC-6181, BAC-5169
5.1.0 2017-08-10 BAC-6172, BAC-6089, BAC-6082, BAC-6035
5.0.0 2017-06-29
ReleaseNotes_DlogClassic, Version 5.3.1, Software Platforms Page 1 of 9

### Page 2

1 Module Description
The DataLogistic is part of the BootManager, Bootloader and Application. It is needed for every ECU to •
get production information • identify software and hardware • check compatibility of hardware and
software • check compatibility of all software units (SWEs) • check at startup if the software is valid and
may be started
2 Revisions and Modiﬁcations
Revision 5.3.1 [Released]
Item Description
CR ID: BAC-6570
CR Headline: Update NvM configuration in integration manual
Description of Issues: Update NvM configuration in integration manual
Description of Changes: Update NvM configuration in integration manual
Changed Files: doc/DlogClassic_IntegrationManual.pdf
Compatibility:
Item Description
CR ID: BAC-6575
CR Headline: Update Sgbm-Entry in Dlog_Data after successfull flashing an swe
Description of Issues: actually only the Bm updates this table. Therefore an read csvk
direkt after CheckProgrammingDependencies does not show this
newly flashed swe.
Description of Changes: copy the SWE description from flash to RAM table in
Dlog_SetSweValidState if SWE is valid
Changed Files: src/Dlog_SweInit.c
include/Dlog_SweStatus.h
src/Dlog_SweStatus.c
Compatibility:
Item Description
CR ID: BAC-6620
CR Headline: Tidy up
Description of Issues: Tidy up: * fix compiler warnings * remove unused defines and
configuration switches * add missing config class specifications *
remove compiler abstraction
Description of Changes: Tidy up: * fix compiler warnings * remove unused defines and
configuration switches * add missing config class specifications *
remove compiler abstraction
Changed Files: generate/src/Dlog_HweTable.c.pgen
include/Dlog_Swe.h
generate/include/Dlog_UDSAdapterAdd.h.pgen
include/Dlog_User.h
ReleaseNotes_DlogClassic, Version 5.3.1, Software Platforms Page 

### Page 3

include/Dlog_TimingParameters.h
src/Dlog_UserAdapter.c
generate/src/Dlog_SweTable.c.pgen
generate/include/Dlog_PBCfg.h.pgen
generate/include/DlogClassic_Cfg.h.pgen
generate/pageinclude/Dlog_Help.pgen
generate/include/Dlog_Nvm.h.pgen
generate/src/Dlog_Nvm.c.pgen
generate/meta/Dlog_ext_interfaces.arxml.pgen
cfgdesc/DlogClassic_paramdef.arxml
generate/src/Dlog_UDSAdapter.c.pgen
include/Dlog_BluSweCheckSum.h
include/Dlog_Ecu.h
generate/meta/Dlog_internal.arxml.pgen
Compatibility:
Item Description
CR ID: BAC-6728
CR Headline: Fix limits of Flash Timing Parameters
Description of Issues: Fix limits of Flash Timing Parameters
Description of Changes: Fix limits of Flash Timing Parameters
Changed Files: src/Dlog_Swe.c
Compatibility:
Item Description
CR ID: BAC-6709
CR Headline: Dlog: Rename HWE Table structure element "sgmbId"
Description of Issues: In file "Dlog_HweTable.h" you find the HW Table structure. Within
you find several structures and type definitions like
"Dlog_HweInfoRomType". Included here is a uint8 element called
"sgmbId". It’s supposed to be named "SgbmId" like in SP2018
and in the Lastenheften (e.g. FP2_2426ff).
Description of Changes: fix typo: rename sgmbId to sgbmId
Changed Files: generate/src/Dlog_HweTable.c.pgen
generate/include/Dlog_HweTable.h.pgen
Compatibility:
Item Description
CR ID: BAC-6721
CR Headline: Dlog: handle BlockProtection DlogSvkHistory
Description of Issues: The NvMBlock DlogSvkHistory is write-protected. So
writeprotection must be unset before write and set after. Or
integrationmanual entry for this block must be corrected.
Description of Changes: set NvMBlockWriteProt to False for Svk History blocks in
integration manual
Changed Files: doc/DlogClassic_IntegrationManual.pdf
ReleaseNotes_DlogClassic, Version 5.3.1, Software Platforms Page 3

### Page 4

Compatibility:
Item Description
CR ID: BAC-6731
CR Headline: Dlog: SvkBackupSize wrong calculated in ext_interfaces
Description of Issues: Calculation uses old fingerprintlength. Use short fingerprint length
4.
Description of Changes: fix calculation of SvkBackupSize in Dlog_ext_interfaces.arxml.pgen
Changed Files: generate/meta/Dlog_ext_interfaces.arxml.pgen
Compatibility:
Item Description
CR ID: BAC-6672
CR Headline: Dlog - version info not checked at compile time
Description of Issues: Unlike for most other BAC modules the version information from
the CommonPublishedInformation container is not validated at
compile time in Dlog & DlogShared.
Description of Changes: add missing version checks
Changed Files: src/Dlog_UserAdapter.c
src/Dlog_NvMAdapter.c
generate/include/DlogClassic_Version.h.pgen
Compatibility:
Revision 5.3.0 [Released]
Item Description
CR ID: BAC-6461
CR Headline: DlogClassic: Dlog_Data shall not be initialized
Description of Issues: The problem is here that for some compilers (e.g. TASKING) the
*Dlog_Data* variable will be seen as an initialized variable an put
therefore to a *.data* section. As the other variables
*Dlog_SweStatus* and *Dlog_SweInfos* are uninitialized they will
be put into the *.bss* section. This makes it ugly to map it
accordingly to a shared section between Appl, BM and Btld.
Description of Changes: remove initialization of Dlog_Data
Changed Files: src/Dlog_SweStatus.c
Compatibility:
Item Description
CR ID: BAC-6363
CR Headline: New DLOG API to set/withdraw bootloader boot target
ReleaseNotes_DlogClassic, Version 5.3.1, Software Platforms Page 4 of 9

### Page 5

Description of Issues: For the ethernet parallel flash mode functionality (aka c3 flag),
EthDiagMM needs an API from Dlog to indicate, whether next boot
target should be bootloader and a corresponding API, to withdraw
this "wish". The C3/PFM flag is now (as of BAC4 Rel3)
persisted/stored by EthDiagMM itself, but IF set, the ECU shall
come up in Bootloader. The current idea is, that EthDiagMM
always calls Dlog with this new/to be intzroduced API, whenever
this PFM-value (and therefore the need to start up in bootloader)
changes.
Description of Changes: changed BootMode such that different users can request or
unrequest bootloader
Changed Files: include/Dlog_BootMode.h
src/Dlog_BootMode.c
Compatibility:
Item Description
CR ID: BAC-6422
CR Headline: Bs, Dlog, Pia: Schema of paramdefs, paramconfs and SWCDen
should be AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Issues: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Changes: change arxml schema to
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Changed Files: generate/meta/Dlog_internal.arxml.pgen
cfgdesc/DlogClassic_paramdef.arxml
generate/meta/Dlog_interfaces.arxml.pgen
generate/meta/Dlog_ext_interfaces.arxml.pgen
Compatibility:
Item Description
CR ID: BAC-6362
CR Headline: Adapt to new postbuild variant handling
Description of Issues: adapt to new postbuild variant handling
Description of Changes: adapt to new postbuild variant handling
Changed Files: generate/include/Dlog_PBCfg.h.pgen
generate/src/Dlog_PBCfg.c.pgen
Compatibility:
Item Description
CR ID: BAC-6055
CR Headline: Improve handling of DLOG_SWFK_DELSUP_AVAILABLE
Description of Issues: At the moment DLOG_SWFK_DELSUP_AVAILABLE is set to
STD_OFF.
Description of Changes: move DLOG_SWFK_DELSUP_AVAILABLE back to c

*Excerpt: first 8 of 9 pages shown.*
