---
title: 'Dlog — DlogGeneric_ReleaseNotes'
description: 'Converted PDF document DlogGeneric_ReleaseNotes.pdf from module Dlog.'
sidebar:
  hidden: true
---

> **Source:** `DlogGeneric_ReleaseNotes.pdf` (PDF, 132 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 5; title: -; author: -

## Converted content

### Page 1

Release Notes DlogGeneric
Project BMW AUTOSAR Core 4 Rel. 3 and adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-12-14
Version 5.1.1
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
5.1.1 2017-12-14 BAC-6672, BAC-6726
5.1.0 2017-11-09 BAC-6266, BAC-6422, BAC-6055
5.0.2 2017-09-14 BAC-6223, BAC-6213, BAC-6181, BAC-5169
5.0.1 2017-08-10 BAC-6172, BAC-6089
5.0.0 2017-06-29
ReleaseNotes_DlogGeneric, Version 5.1.1, Software Platforms Page 1 of 5

### Page 2

1 Module Description
The DataLogistic is part of the BootManager, Bootloader and Application. It is needed for every ECU to •
get production information • identify software and hardware • check compatibility of hardware and
software • check compatibility of all software units (SWEs) • check at startup if the software is valid and
may be started
2 Revisions and Modiﬁcations
Revision 5.1.1 [Released]
Item Description
CR ID: BAC-6672
CR Headline: Dlog - version info not checked at compile time
Description of Issues: Unlike for most other BAC modules the version information from
the CommonPublishedInformation container is not validated at
compile time in Dlog & DlogShared.
Description of Changes: add missing version checks
Changed Files: include/Dlog_UDSAdapter.h
include/Dlog_NvMAdapter.h
include/Dlog_SvkGen.h
src/Dlog_SweGen.c
include/Dlog_CodingAdapter.h
include/Dlog_SweGen.h
include/Dlog_Data.h
src/Dlog_SvkGen.c
generate/include/Dlog_Cfg.h.pgen
include/Dlog_UserAdapter.h
Compatibility:
Item Description
CR ID: BAC-6726
CR Headline: Do not write History after first start after debug flash
Description of Issues: Do not write History after first start after debug flash, i.e. when the
NvM block is not readable.
Description of Changes: Do not write History after first start after debug flash, i.e. when the
NvM block is not readable.
Changed Files: src/Dlog_SvkGen.c
Compatibility:
Revision 5.1.0 [Released]
Item Description
CR ID: BAC-6266
ReleaseNotes_DlogGeneric, Version 5.1.1, Software Platforms Page 2 of 5

### Page 3

CR Headline: Invalid SWFK with alternative SWFK
Description of Issues: after deleting the last SWFK of an group which must contain at
least one SWFK an invalid entry must display when read
SVK_AKTUELL.
Description of Changes: output default entry for missing SWFK in
DLOG_SWEGROUP_ONEOBLIGATORY
Changed Files: src/Dlog_SvkGen.c
Compatibility:
Item Description
CR ID: BAC-6422
CR Headline: Bs, Dlog, Pia: Schema of paramdefs, paramconfs and SWCDen
should be AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Issues: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Changes: change arxml schema to
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Changed Files: cfgdesc/Dlog_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6055
CR Headline: Improve handling of DLOG_SWFK_DELSUP_AVAILABLE
Description of Issues: At the moment DLOG_SWFK_DELSUP_AVAILABLE is set to
STD_OFF.
Description of Changes: move DLOG_SWFK_DELSUP_AVAILABLE back to classic since
in adaptive it will be a postbuild parameter
Changed Files: generate/include/Dlog_Cfg.h.pgen
Compatibility:
Revision 5.0.2 [Released]
Item Description
CR ID: BAC-6223
CR Headline: Usage of IMPLEMENTATION-CONFIG-CLASSES is deprecated
and shall be replaced by VALUE-CONFIG-CLASSES according to
ASR4.2.2
Description of Issues: TPS_ECUC_06051 is removed from spec. In schema
AUTOSAR_4-2-2.xsd IMPLEMENTATION-CONFIG-CLASSES is
marked as deprecated. That means: IMPLEMENTATION-
CONFIG-CLASSES/IMPLEMENTATION-CONFIG-CLASS has to
be replaed by
VALUE-CONFIG-CLASSES/VALUE-CONFIG-CLASS entirely
within paramdefs!
Description of Changes: fix config classes in paramdef.arxml file
Changed Files: cfgdesc/Dlog_paramdef.arxml
ReleaseNotes_DlogGeneric, Version 5.1.1, Software Platforms Page 3 of 5

### Page 4

Compatibility:
Item Description
CR ID: BAC-6213
CR Headline: Write Svk History after reprogramming
Description of Issues: Write Svk History after reprogramming
Description of Changes: Write Svk History after reprogramming
Changed Files: src/Dlog_SvkGen.c
include/Dlog_SvkGen.h
Compatibility:
Item Description
CR ID: BAC-6181
CR Headline: Tidy up
Description of Issues: Tidy up: - remove dependency to Srv in comment - remove
remains of VirtualCPU - remove remains of RSU - remove remains
of write fingerprint - remove dead code - fix file headers - fix
compiler warnings
Description of Changes: Tidy up: - remove dependency to Srv in comment - remove
remains of VirtualCPU - remove remains of RSU - remove remains
of write fingerprint - remove dead code - fix file headers - fix
compiler warnings
Changed Files: src/Dlog_SvkGen.c
src/Dlog_EcuGen.c
CMakeLists.txt
include/Dlog_EcuGen.h
include/Dlog_SvkGen.h
Compatibility:
Item Description
CR ID: BAC-5169
CR Headline: Some (most?) BAC modules paramdef violate TPS_ECUC_06004
Description of Issues: According to AUTOSAR TPS_ECUConfiguration there is the
following requirement:
[TPS_ECUC_06004] AdminData field in ECU Configuration
Parameter Definition XML file d An AdminData field is required at
the beginning of every ECU Configuration Parameter Definition
XML file (regardless whether it is the StMD or the VSMD file) to
allow the setting of AdminData for the whole XML File. c()
Most of our modules fail to define the AdminData Element (just
saw it in Darh - and here the element contains mixed info to be
fixed). It is somehow weired as we then will define version info
within CommonPublishedInformation AND AdminData - but as it is
formally required, we have to follow it.
Description of Changes: add AdminData to paramdef file
Changed Files: cf

### Page 5

Compatibility:
Revision 5.0.1 [Released]
Item Description
CR ID: BAC-6172
CR Headline: Tidy up
Description of Issues: Tidy up: - remove remains of first start flag - remove remains of
prog counter - fix compiler warnings
Description of Changes: Tidy up: - remove remains of first start flag - remove remains of
prog counter - fix compiler warnings
Changed Files: src/Dlog_SvkGen.c
Compatibility:
Item Description
CR ID: BAC-6089
CR Headline: Bm/Dlog inconsistent defines Blu does not start
Description of Issues: Bm/Dlog inconsistent defines Blu does not start
Description of Changes: return consistent application for programming dependency state in
case of BLU
Changed Files: include/Dlog_Data.h
src/Dlog_SvkGen.c
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_DlogGeneric, Version 5.1.1, Software Platforms Page 5 of 5
