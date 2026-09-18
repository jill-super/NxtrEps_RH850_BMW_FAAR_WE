---
title: 'DlogShared — DlogSharedGeneric_ReleaseNotes'
description: 'Converted PDF document DlogSharedGeneric_ReleaseNotes.pdf from module DlogShared.'
sidebar:
  hidden: true
---

> **Source:** `DlogSharedGeneric_ReleaseNotes.pdf` (PDF, 122 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 4; title: -; author: -

## Converted content

### Page 1

Release Notes DlogSharedGeneric
Project BMW AUTOSAR Core 4 Rel. 3 and adaptive BMW AUTOSAR Core Rel. 1
Author BMW AG
Release Date 2017-12-14
Version 5.0.3
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
5.0.3 2017-12-14 BAC-6711, BAC-6728, BAC-6702
5.0.2 2017-11-09 BAC-6368, BAC-6362, BAC-6422
5.0.1 2017-09-14 BAC-6223, BAC-5169
5.0.0 2017-06-29
ReleaseNotes_DlogSharedGeneric, Version 5.0.3, Software Platforms Page 1 of 4

### Page 2

1 Module Description
Part of the configuration of the Dlog module that is shared between Bootloader, Bootmanager and
Application.
2 Revisions and Modiﬁcations
Revision 5.0.3 [Released]
Item Description
CR ID: BAC-6711
CR Headline: missing MIN-MAX limits for parameter definitions
Description of Issues: Many integer parameters used for sizes and address values in Blu
and DlogShared do not have a MIN-MAX limit specified
Description of Changes: add missing min and max values in DlogShared_paramdef.arxml
Changed Files: cfgdesc/DlogShared_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6728
CR Headline: Fix limits of Flash Timing Parameters
Description of Issues: Fix limits of Flash Timing Parameters
Description of Changes: Fix limits of Flash Timing Parameters
Changed Files: cfgdesc/DlogShared_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6702
CR Headline: Dlog: SVK Backup MAX Limit wrong in autosar def file?
Description of Issues: According to BMW 61 places alltogether are supposed to be kept
clear for the logistics of SVK Backups. In the AutoSAR definition of
Dlog_Shared (DlogShared_paramdef.arxml) a maximum of 31
places is stated.
Description of Changes: increase max number of SVK backup from 31 to 61
Changed Files: cfgdesc/DlogShared_paramdef.arxml
Compatibility:
Revision 5.0.2 [Released]
Item Description
CR ID: BAC-6368
CR Headline: Remove obsolete configs for AuthCounter and MirrorSwe
Description of Issues: Remove obsolete configs for AuthCounter and MirrorSwe
Description of Changes: Remove obsolete configs for AuthCounter and MirrorSwe
ReleaseNotes_DlogSharedGeneric, Version 5.0.3, Software Platforms Page 2 of 4

### Page 3

Changed Files: cfgdesc/DlogShared_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6362
CR Headline: Adapt to new postbuild variant handling
Description of Issues: adapt to new postbuild variant handling
Description of Changes: adapt to new postbuild variant handling
Changed Files: cfgdesc/DlogShared_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-6422
CR Headline: Bs, Dlog, Pia: Schema of paramdefs, paramconfs and SWCDen
should be AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Issues: Schema of paramdefs, paramconfs and SWCDen should be
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Description of Changes: change arxml schema to
AUTOSAR_4-3-0_STRICT_COMPACT.xsd
Changed Files: cfgdesc/DlogShared_paramdef.arxml
Compatibility:
Revision 5.0.1 [Released]
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
Changed Files: cfgdesc/DlogShared_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-5169
CR Headline: Some (most?) BAC modules paramdef violate TPS_ECUC_06004
ReleaseNotes_DlogSharedGeneric, Version 5.0.3, Software Platforms Page 3 of 4

### Page 4

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
Changed Files: cfgdesc/DlogShared_paramdef.arxml
Compatibility:
Revision 5.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2021
Description of Issues: Initial Release for SP2021
Description of Changes: Initial Release for SP2021
Changed Files:
Compatibility:
ReleaseNotes_DlogSharedGeneric, Version 5.0.3, Software Platforms Page 4 of 4
