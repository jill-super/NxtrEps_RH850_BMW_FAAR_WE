---
title: 'Srv — ReleaseNotes_Srv'
description: 'Converted PDF document ReleaseNotes_Srv.pdf from module Srv.'
sidebar:
  hidden: true
---

> **Source:** `ReleaseNotes_Srv.pdf` (PDF, 134 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 3; title: -; author: -

## Converted content

### Page 1

Release Notes Srv
Project BMW AUTOSAR Core 4 Rel. 2
Author BMW AG
Release Date 2015-12-11
Version 3.1.0
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
3.1.0 2015-12-11 BAC-4692
3.0.1 2015-03-13 BAC-3938, BAC-3651
3.0.0 2014-10-29
ReleaseNotes_Srv, Version 3.1.0, Platform Software Page 1 of 3

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
The Srv (Service) module contains some general purpose functions commonly used by other modules
like Dlog, Prog and Bm. It is used in Application, Bootloader and Bootmanager.
This package is maintained by BMW AUTOSAR Core 4 Support, via ASCENT Jira
(https://asc.bmwgroup.net/jira/browse/BSUP or https://asc.bmw.com/jira/browse/BSUP) or telephone
hotline (+49-89-382-32233).
3 Revisions and Modiﬁcations
3.1 Revision 3.1.0 [Released]
Item Description
CR ID: BAC-4692
CR Headline: Srv: Adapt ECUC and SWCD schema to 4.2.2
Description of Issues: Adapt ECUC schema to 4.2.2
Description of Changes: Adapt ECUC schema to 4.2.2
Changed Files: autosar/Asr40/Srv_paramdef.arxml
Compatibility:
3.2 Revision 3.0.1 [Released]
Item Description
CR ID: BAC-3938
CR Headline: Srv: Set Parameters’ ConfigClass from container
CommonPublishedInformation to PUBLISHED-INFORMATION
ReleaseNotes_Srv, Version 3.1.0, Platform Software Page 2 of 3

### Page 3

Description of Issues: Although the module’s version is checked during pre-compile
there’s no need to have this parameter configurable to the user.
Therefore, all modules should have the ConfigClass from the
parameters SwMajorVersion, SwMinorVersion and
SwPatchVersion set to PUBLISHED-INFORMATION.
Description of Changes: set config class of CommonPublishedInformation to
PUBLISHED-INFORMATION
Changed Files: autosar/Asr40/Srv_paramdef.arxml
Compatibility:
Item Description
CR ID: BAC-3651
CR Headline: Srv: Adapt makefiles to EA requirements
Description of Issues: Adapt makefiles to EA requirements
Description of Changes: Adapt makefiles to EA requirements
Changed Files: generate/verify/Srv.autoverify.tt
make/Srv_defs.mak
Compatibility:
3.3 Revision 3.0.0 [Released]
Item Description
CR ID:
CR Headline: Initial Release for SP2018
Description of Issues: Initial Release for SP2018
Description of Changes: Initial Release for SP2018
Changed Files:
Compatibility:
ReleaseNotes_Srv, Version 3.1.0, Platform Software Page 3 of 3
